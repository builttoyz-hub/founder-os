# Knowledge Graph — Arquitectura de Escalabilidad

## El Problema de Escala

A 1 millón de publicaciones, las queries de compatibilidad automotriz se convierten en el cuello de botella técnico más crítico del sistema. Este documento define las estrategias de escalabilidad del AKG desde el día 1.

---

## Análisis de Cardinalidad

```
MAKES:          ~50 marcas activas (estable)
MODELS:         ~800 modelos en Colombia (crece ~50/año)
ENGINE_CODES:   ~600 códigos únicos (crece ~30/año)
COMPAT_PAIRS:   ~4,000 combinaciones modelo+motor (crece ~200/año)
PLATFORMS:      ~80 plataformas (muy estable)
CATEGORIES:     ~100 categorías+subcategorías (muy estable)
LISTINGS:       0 → 1M+ (crece rápido)
```

**Conclusión:** Las tablas del AKG son pequeñas y estables. La tabla `listings` es la que escala masivamente. El diseño debe optimizarse para queries que cruzan `listings` con el AKG.

---

## Estrategia de Índices para 1M de Listings

### Índices Críticos (Tier 1 — crear en el MVP)

```sql
-- Búsqueda por compatibilidad directa (más frecuente)
CREATE INDEX CONCURRENTLY idx_listings_compat_primary 
  ON listings (marca_vehiculo, status, is_featured DESC, created_at DESC)
  WHERE status = 'active';

-- Búsqueda por motorización (segunda más frecuente)
CREATE INDEX CONCURRENTLY idx_listings_motorizaciones_gin 
  ON listings USING GIN (motorizaciones)
  WHERE status = 'active';

-- Búsqueda full-text (tercera más frecuente)
CREATE INDEX CONCURRENTLY idx_listings_search_gin 
  ON listings USING GIN (search_vector)
  WHERE status = 'active';

-- Combinado categoría + estado (para sidebar filters)
CREATE INDEX CONCURRENTLY idx_listings_cat_city_price 
  ON listings (categoria, ciudad, precio)
  WHERE status = 'active';

-- AI tags para búsqueda semántica futura
CREATE INDEX CONCURRENTLY idx_listings_ai_tags_gin 
  ON listings USING GIN (ai_tags)
  WHERE status = 'active';
```

**Por qué `WHERE status = 'active'`:** Los índices parciales son más pequeños y más rápidos. En producción, el 80% de las queries son para listings activos.

### Índices del AKG (Tier 2 — crear en el MVP, pequeños y rápidos)

```sql
-- Cross-platform compatibility lookup
CREATE UNIQUE INDEX idx_platforms_code ON platforms (code);
CREATE INDEX idx_models_platform ON models (platform_code) WHERE platform_code IS NOT NULL;

-- Engine family lookup
CREATE INDEX idx_engines_family ON engines (family, manufacturer);
CREATE INDEX idx_engines_aspiration ON engines (aspiration, fuel_type);

-- Compatibility table (la más consultada del AKG)
CREATE UNIQUE INDEX idx_compat_model_engine_year 
  ON model_engine_compat (model_id, engine_id, year_from);
CREATE INDEX idx_compat_engine_id ON model_engine_compat (engine_id);
CREATE INDEX idx_compat_platform ON models (platform_code, make_id);
```

---

## Query Patterns y Sus Optimizaciones

### Pattern 1: "Mostrar piezas para mi BMW 135i E82 N55 2012"

```
INPUT: make="BMW", model="E82 135i", year=2012, engine="N55B30"
QUERY FLOW:
  1. Lookup model_id por slug "bmw-serie-1-e82" → O(1) con UNIQUE index
  2. Verificar compat model_id + engine "N55B30" + year 2012 → O(1)
  3. SELECT listings WHERE:
       marca_vehiculo = 'BMW'
       AND (modelo_vehiculo ILIKE '%E82%' OR modelo_vehiculo ILIKE '%135i%')
       AND 'N55B30' = ANY(motorizaciones)
       AND status = 'active'
     → usa idx_listings_compat_primary + idx_listings_motorizaciones_gin
ESTIMATED TIME: < 10ms hasta 1M listings con estos índices
```

### Pattern 2: "Todas las piezas compatibles con plataforma PQ35"

```
INPUT: platform_code = "PQ35"
QUERY FLOW:
  1. SELECT model_id FROM models WHERE platform_code = 'PQ35' → ~15 filas
  2. SELECT marca_vehiculo, modelo_vehiculo FROM models WHERE id IN (...)
  3. SELECT listings WHERE (marca_vehiculo, modelo_vehiculo) IN (...)
     OR motorizaciones && '{EA113, EA888}'
     AND status = 'active'
OPTIMIZATION: Materializar lista de modelos PQ35 como constante en la app
ESTIMATED TIME: < 25ms hasta 1M listings
```

### Pattern 3: "Búsqueda de texto libre: turbo k04 s3 8p"

```
INPUT: search_text = "turbo k04 s3 8p"
QUERY FLOW:
  1. Typesense query (< 5ms) con typo tolerance
  2. FALLBACK: tsvector query sobre search_vector con ts_rank
     WHERE search_vector @@ plainto_tsquery('spanish', 'turbo k04 s3 8p')
     AND status = 'active'
     ORDER BY ts_rank(search_vector, query) DESC
     → usa idx_listings_search_gin
ESTIMATED TIME: < 15ms con Typesense, < 30ms con PostgreSQL FTS fallback
```

---

## Estrategia de Caché para el AKG

Las tablas del AKG son casi-inmutables (cambian < 50 veces/mes). Esto las hace candidatas perfectas para caché agresivo.

| Entidad | TTL Cache | Estrategia | Invalidación |
|---------|-----------|------------|-------------|
| `makes` completo | 24 horas | Redis SET + JSON | Manual al agregar marca |
| `models` por make_slug | 6 horas | Redis HSET | Manual al agregar modelo |
| `engines` por código | 24 horas | Redis SET | Manual al agregar motor |
| `compat` por model_id | 12 horas | Redis SET | Manual al cambiar compat |
| `platforms` completo | 7 días | Redis SET | Casi nunca cambia |
| `categories` completo | 7 días | Redis SET + React Query | Casi nunca cambia |

**Resultado:** El 99% de las queries de compatibilidad no tocan la DB — van directo al cache.

---

## Particionamiento Futuro de Listings

Cuando `listings` supere 5 millones de filas (estimado 2028+):

```
-- Partición por mes de creación (la más eficiente para queries recientes)
CREATE TABLE listings (
  ...
) PARTITION BY RANGE (created_at);

-- Particiones activas (queries frecuentes)
CREATE TABLE listings_2026_q3 PARTITION OF listings
  FOR VALUES FROM ('2026-07-01') TO ('2026-10-01');

-- Particiones archivadas (queries menos frecuentes, sin índices activos)
-- Las piezas vendidas de 2026 en 2028 son raramente buscadas
```

**Regla:** Listings con status='sold' o 'expired' de más de 6 meses → tabla de archivo. El marketplace siempre busca sobre listings activos y recientes.

---

## El AKG como API Pública (Fase V2)

El Knowledge Graph automotriz colombiano de PITS MARKET es potencialmente un producto en sí mismo. Otras plataformas (seguros, financieras, talleres) podrían pagar por acceso a:

- Tabla de compatibilidades para Colombia
- Precios de mercado por modelo/motorización (agregado anonimizado)
- Datos de tuning popularity por región

**Estrategia:** En V2, exponer endpoints GET del AKG en la API pública. El AKG se convierte en un asset monetizable independiente del marketplace.

