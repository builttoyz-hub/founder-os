# Automotive Knowledge Graph — Schema Oficial

## Propósito

Este documento define el schema canónico del Automotive Knowledge Graph (AKG) de PITS MARKET. El AKG es el activo técnico diferencial más importante de la plataforma. Define la ontología exacta de entidades, relaciones y atributos que hacen posible la búsqueda por compatibilidad técnica.

> **Regla de oro:** Ningún dato de vehículo entra a la base de datos de producción sin haber pasado primero por este schema. El AKG es la fuente de verdad. La DB es la implementación.

---

## Entidades del Knowledge Graph

```
MAKE ──1:N──► MODEL ──1:N──► MODEL_YEAR ──N:M──► ENGINE
                │                                     │
                │                                     │
             PLATFORM                           ENGINE_FAMILY
                │                                     │
                └────────────── COMPATIBILITY ────────┘
                                     │
                                     ▼
                              PART_CATEGORY
                              (lo que se puede vender)
```

---

## Entidad 1: MAKE (Marca)

| Campo | Tipo | Requerido | Descripción |
|-------|------|-----------|-------------|
| `id` | INTEGER (auto) | ✓ | ID interno secuencial |
| `slug` | TEXT UNIQUE | ✓ | kebab-case: `bmw`, `volkswagen`, `honda-motor` |
| `name` | TEXT | ✓ | Nombre oficial: `BMW`, `Volkswagen`, `Honda` |
| `name_aliases` | TEXT[] | ✗ | Nombres alternativos: `["VW"]` para Volkswagen |
| `country_origin` | TEXT | ✓ | ISO 3166-1: `DE`, `JP`, `US`, `KR`, `CN` |
| `region_group` | ENUM | ✓ | `EUROPEAN`, `JAPANESE`, `AMERICAN`, `KOREAN`, `CHINESE` |
| `is_luxury` | BOOLEAN | ✓ | Segmento premium (BMW, Audi, Mercedes) |
| `is_active_colombia` | BOOLEAN | ✓ | Actualmente en el mercado colombiano |
| `display_order` | SMALLINT | ✓ | Orden en UI (más populares primero) |
| `logo_url` | TEXT | ✗ | URL del logo SVG en CDN |

**Marcas activas en Colombia (tuning relevante):**
BMW · Audi · Volkswagen · Mercedes-Benz · Honda · Toyota · Mazda · Subaru · Mitsubishi · Ford · Chevrolet · Nissan · Hyundai · Kia · Seat · Renault · Peugeot · Jeep · Dodge · Porsche

---

## Entidad 2: MODEL (Modelo)

| Campo | Tipo | Requerido | Descripción |
|-------|------|-----------|-------------|
| `id` | INTEGER (auto) | ✓ | ID interno |
| `make_id` | INTEGER → MAKE | ✓ | FK a la marca |
| `slug` | TEXT UNIQUE | ✓ | `bmw-serie-1-e82`, `audi-s3-8p` |
| `name` | TEXT | ✓ | Nombre completo: `Serie 1 E82` |
| `name_short` | TEXT | ✓ | Nombre corto: `E82`, `S3 8P` |
| `name_aliases` | TEXT[] | ✗ | Aliases de la comunidad: `["135i", "128i", "120i"]` |
| `generation_code` | TEXT | ✓ | Código de generación: `E82`, `8P`, `GE8`, `GRB` |
| `platform_code` | TEXT | ✗ | Plataforma compartida: `E8x`, `PQ35`, `MQB-A0` |
| `body_style` | ENUM | ✓ | `SEDAN`, `COUPE`, `HATCHBACK`, `WAGON`, `SUV`, `PICKUP`, `CONVERTIBLE`, `VAN` |
| `doors` | SMALLINT | ✗ | Número de puertas: 2, 3, 4, 5 |
| `year_intro_colombia` | SMALLINT | ✗ | Primer año de disponibilidad en Colombia |
| `year_end_colombia` | SMALLINT | ✗ | Último año. NULL si sigue disponible |
| `is_jdm_available` | BOOLEAN | ✓ | Si existe versión JDM en el mercado colombiano |
| `is_usdm_available` | BOOLEAN | ✓ | Si existe versión USDM en Colombia |
| `tuning_popularity` | ENUM | ✓ | `NONE`, `LOW`, `MEDIUM`, `HIGH`, `ICONIC` |
| `data_confidence` | ENUM | ✓ | `VERIFIED`, `COMMUNITY`, `UNVERIFIED` |
| `notes` | TEXT | ✗ | Notas específicas del modelo para Colombia |

---

## Entidad 3: ENGINE (Motor)

| Campo | Tipo | Requerido | Descripción |
|-------|------|-----------|-------------|
| `id` | INTEGER (auto) | ✓ | ID interno |
| `code` | TEXT UNIQUE | ✓ | Código oficial: `N55B30`, `EA113`, `K20A2` |
| `code_aliases` | TEXT[] | ✗ | Aliases conocidos: `["N55", "N55B30O0"]` |
| `manufacturer` | TEXT | ✓ | Fabricante: `BMW AG`, `Volkswagen AG`, `Honda Motor` |
| `family` | TEXT | ✓ | Familia de motores: `N-series`, `EA-series`, `K-series` |
| `displacement_cc` | INTEGER | ✓ | Cilindrada exacta: `1984`, `2979`, `1998` |
| `cylinders` | SMALLINT | ✓ | Número de cilindros: 3, 4, 6, 8 |
| `configuration` | ENUM | ✓ | `INLINE`, `V`, `FLAT`, `W`, `ROTARY` |
| `fuel_type` | ENUM | ✓ | `GASOLINE`, `DIESEL`, `HYBRID`, `ELECTRIC`, `FLEX` |
| `aspiration` | ENUM | ✓ | `NA`, `TURBO`, `TWIN_TURBO`, `SUPERCHARGED`, `TWINCHARGED` |
| `valvetrain` | TEXT | ✗ | `DOHC`, `SOHC`, `OHV`, `DOHC VTEC` |
| `power_hp_std` | SMALLINT | ✗ | HP de fábrica en versión estándar |
| `power_hp_max` | SMALLINT | ✗ | HP máximo en versión más potente de fábrica |
| `torque_nm_std` | SMALLINT | ✗ | Nm de fábrica |
| `redline_rpm` | INTEGER | ✗ | RPM de corte del motor |
| `bore_mm` | DECIMAL(5,2) | ✗ | Diámetro del cilindro en mm |
| `stroke_mm` | DECIMAL(5,2) | ✗ | Carrera en mm |
| `compression_ratio` | DECIMAL(4,2) | ✗ | Relación de compresión: `9.50` |
| `block_material` | ENUM | ✗ | `IRON`, `ALUMINUM`, `MAGNESIUM_ALLOY` |
| `head_material` | ENUM | ✗ | `IRON`, `ALUMINUM` |
| `obd_standard` | ENUM | ✗ | `OBD1`, `OBD2`, `EOBD`, `JOBD` |
| `ecu_type` | TEXT | ✗ | ECU de fábrica: `Siemens MSD87`, `Bosch ME17.9` |
| `tuning_potential` | ENUM | ✓ | `LOW`, `MEDIUM`, `HIGH`, `EXTREME` |
| `common_failures` | TEXT[] | ✗ | Fallas comunes conocidas: `["HPFP", "Injectors", "Wastegate rattle"]` |
| `data_confidence` | ENUM | ✓ | `VERIFIED`, `COMMUNITY`, `UNVERIFIED` |
| `notes` | TEXT | ✗ | Notas técnicas relevantes para la comunidad |

---

## Entidad 4: MODEL_ENGINE_COMPAT (Tabla de Compatibilidad)

La relación N:M entre modelos y motores. Esta tabla ES el Knowledge Graph.

| Campo | Tipo | Requerido | Descripción |
|-------|------|-----------|-------------|
| `id` | INTEGER (auto) | ✓ | ID interno |
| `model_id` | INTEGER → MODEL | ✓ | FK al modelo |
| `engine_id` | INTEGER → ENGINE | ✓ | FK al motor |
| `year_from` | SMALLINT | ✓ | Primer año de esta combinación |
| `year_to` | SMALLINT | ✗ | Último año. NULL si sigue en producción |
| `market` | ENUM[] | ✓ | `COLOMBIA`, `LATAM`, `USA`, `EUROPE`, `JDM`, `GLOBAL` |
| `trim_levels` | TEXT[] | ✗ | Versiones donde aplica: `["Sport", "M Performance"]`. Empty = todas |
| `is_factory` | BOOLEAN | ✓ | `true` si es combinación de fábrica, `false` si es swap documentado |
| `transmission_options` | ENUM[] | ✗ | `MANUAL_5`, `MANUAL_6`, `AUTO_6`, `DCT_7`, `CVT` |
| `drive_layout` | ENUM | ✗ | `FWD`, `RWD`, `AWD`, `4WD` |
| `ecu_tune_available` | BOOLEAN | ✗ | Si hay tune de ECU disponible comercialmente |
| `popular_tune_brands` | TEXT[] | ✗ | Marcas de tune populares: `["APR", "Revo", "MHD"]` |
| `data_confidence` | ENUM | ✓ | `VERIFIED`, `COMMUNITY`, `UNVERIFIED` |
| `source` | TEXT | ✗ | Fuente de verificación: `"BMW AG Build Sheet"`, `"Community verified x15"` |
| `notes` | TEXT | ✗ | Notas específicas de esta combinación |

---

## Entidad 5: PLATFORM (Plataforma Compartida)

Agrupa modelos que comparten arquitectura y por tanto comparten piezas.

| Campo | Tipo | Requerido | Descripción |
|-------|------|-----------|-------------|
| `id` | INTEGER (auto) | ✓ | ID interno |
| `code` | TEXT UNIQUE | ✓ | Código de plataforma: `PQ35`, `MQB`, `E8x`, `GRB` |
| `name` | TEXT | ✓ | Nombre completo: `PQ35 Platform`, `Modular Transverse Matrix` |
| `maker_group` | TEXT | ✓ | Grupo automotriz: `Volkswagen Group`, `BMW AG`, `Renault-Nissan` |
| `architecture` | ENUM | ✓ | `FWD`, `RWD`, `AWD`, `FLEXIBLE` |
| `wheelbase_range_mm` | TEXT | ✗ | Rango de wheelbase: `2578-2630` |
| `notes` | TEXT | ✗ | Notas técnicas de la plataforma |

---

## Entidad 6: PART_CATEGORY (Categorías de Piezas)

La taxonomía de lo que se puede vender. Relacionada con ENGINE y PLATFORM para filtrado de compatibilidad.

| Campo | Tipo | Requerido | Descripción |
|-------|------|-----------|-------------|
| `id` | INTEGER (auto) | ✓ | ID interno |
| `slug` | TEXT UNIQUE | ✓ | `turbos-sobrealimentacion`, `frenos`, `suspension` |
| `name` | TEXT | ✓ | Nombre display: `Turbos y Sobrealimentación` |
| `name_short` | TEXT | ✓ | Nombre corto para pills/badges: `Turbos` |
| `parent_id` | INTEGER → self | ✗ | NULL para categorías raíz, FK para subcategorías |
| `icon_name` | TEXT | ✗ | Nombre del ícono Lucide: `Zap`, `Disc`, `Settings2` |
| `emoji` | TEXT | ✗ | Emoji representativo: `🌪️`, `🔴`, `🔧` |
| `is_engine_specific` | BOOLEAN | ✓ | Si la pieza depende del motor específico |
| `is_universal` | BOOLEAN | ✓ | Si puede ser universal (sin compatibilidad de vehículo) |
| `requires_professional_install` | BOOLEAN | ✓ | Si requiere instalación profesional |
| `display_order` | SMALLINT | ✓ | Orden en UI |
| `is_active` | BOOLEAN | ✓ | Activa en el marketplace |

