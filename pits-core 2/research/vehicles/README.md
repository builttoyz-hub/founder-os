# /research/vehicles — Automotive Knowledge Graph (AKG)

## ¿Qué es el AKG?

El Automotive Knowledge Graph (AKG) de PITS MARKET es el activo técnico diferencial más importante de la plataforma. Define la ontología exacta de marcas, modelos, motores, plataformas y categorías que hace posible la búsqueda técnica por compatibilidad — algo que ningún marketplace genérico colombiano puede replicar.

> **Ventaja competitiva:** AutoData, CARFAX y otras fuentes globales no tienen datos del mercado colombiano específicamente. Las versiones JDM importadas, los años exactos de disponibilidad en Colombia, los motores que llegaron vs los que no — ese conocimiento solo existe en la comunidad, y PITS MARKET lo está formalizando.

---

## Archivos del Knowledge Graph

| Archivo | Descripción | Estado |
|---------|-------------|--------|
| `KNOWLEDGE-GRAPH-SCHEMA.md` | Schema canónico de todas las entidades y sus relaciones | ✅ Completo |
| `engines-master.md` | Base de datos completa de códigos de motor relevantes para Colombia | ✅ Completo |
| `platforms-compatibility.md` | Plataformas compartidas y compatibilidades cruzadas (PQ35, MQB, E8x, etc.) | ✅ Completo |
| `models-colombia-bmw.md` | Todos los modelos BMW en Colombia con motorizaciones | ✅ Completo |
| `models-colombia-vag.md` | VW, Audi, Seat en Colombia | ✅ Completo |
| `models-colombia-jdm.md` | Honda, Subaru, Mitsubishi, Nissan, Toyota JDM/USDM en Colombia | ✅ Completo |
| `scalability-architecture.md` | Estrategia de índices y caché para 1M+ publicaciones | ✅ Completo |
| *(por crear)* `models-colombia-americanos.md` | Ford Mustang, Chevrolet Camaro, Dodge, Jeep | Pendiente |
| *(por crear)* `models-colombia-koreans.md` | Hyundai, Kia en Colombia | Pendiente |
| *(por crear)* `models-colombia-masivos.md` | Toyota Corolla, Mazda 3, modelos de alto volumen | Pendiente |

---

## Cómo Se Usa el AKG en la Plataforma

```
Usuario selecciona: BMW → E82 135i → 2012 → N55B30
                              ↓
         AKG verifica: ¿Existe esta combinación?
         models tabla → compat tabla → engines tabla
                              ↓
         Query a listings:
         WHERE marca_vehiculo = 'BMW'
         AND modelo_vehiculo ILIKE '%E82%'
         AND 'N55B30' = ANY(motorizaciones)
         AND status = 'active'
                              ↓
         Resultado: Piezas compatibles ordenadas por relevancia
```

---

## Niveles de Confianza de los Datos

| Nivel | Descripción | Cómo se logra |
|-------|-------------|---------------|
| `VERIFIED` | Doble verificación: fuente oficial + confirmación de la comunidad | Documentación técnica del fabricante + ≥2 expertos de la comunidad |
| `COMMUNITY` | Validado por la comunidad, sin fuente oficial accesible | ≥3 confirmaciones independientes de propietarios/mecánicos |
| `UNVERIFIED` | Datos de una sola fuente, pendiente de verificación | Solo entrada manual sin validación |

**Regla:** Solo datos `VERIFIED` o `COMMUNITY` entran a la base de datos de producción. `UNVERIFIED` permanece en el repositorio como documento de investigación.

---

## Cómo Contribuir al AKG

La ontología mejora con el conocimiento de la comunidad:

1. Abrir Issue con label `area: research` y título `[AKG] Agregar [Modelo/Motor] [Año]`
2. Incluir: modelo exacto, año disponible en Colombia, motorización con código oficial
3. Indicar la fuente: Build sheet, documentación oficial, o N confirmaciones de comunidad
4. Un mantenedor del AKG verifica y agrega al archivo correspondiente
5. La actualización en el AKG genera automáticamente una tarea para actualizar la DB de producción

---

## Convención de Nombres

```
[tipo]-[descripcion]-[region-si-aplica].md

Tipos: engines | models | platforms | categories | scalability | KNOWLEDGE-GRAPH-SCHEMA

Ejemplos:
  engines-master.md
  models-colombia-bmw.md
  models-colombia-vag.md
  platforms-compatibility.md
  scalability-architecture.md
```

---

*Este Knowledge Graph es open source para la comunidad. Es uno de los activos que publicamos para construir confianza con el ecosistema tuning colombiano y latinoamericano.*

*Mantenido por: PITS MARKET + Comunidad tuning Colombia*
