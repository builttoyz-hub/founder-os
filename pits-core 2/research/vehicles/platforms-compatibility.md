# Platforms & Cross-Compatibility — Guía de Compatibilidades Cruzadas

> Las plataformas son el superpoder del Automotive Knowledge Graph. Una pieza compatible con la plataforma PQ35 sirve para Golf 5 GTI, Audi A3 8P, Seat León II y Skoda Octavia II. Este documento define esas relaciones.

---

## VOLKSWAGEN GROUP — Plataformas Principales

### PQ35 (2002–2013)
**Nombre completo:** Plataforma Transversal de Segunda Generación del Grupo VW
**Arquitectura:** FWD / AWD (4Motion)
**Wheelbase:** 2578 mm

| Modelo | Marca | Años | Motores PQ35 | Tuning relevante |
|--------|-------|------|--------------|-----------------|
| Golf 5 GTI / R32 | Volkswagen | 2003–2009 | EA113 BPY, VR6-3.2 AXZ | EA113 = el rey del tuning VAG en Colombia |
| Golf 5 GTD | Volkswagen | 2004–2009 | 2.0 TDI BMN | Diesel tuning |
| Jetta A5 / Gli | Volkswagen | 2005–2011 | EA113 BPY | Popular en Colombia |
| A3 8P / S3 8P | Audi | 2003–2013 | EA113 BPY/BWA, EA888 Gen1 CDN | S3 8P K04 = referencia Colombia |
| TT 8J Mk1 | Audi | 2006–2014 | EA113 BWA, EA888 CDN | |
| León II Cupra / FR | Seat | 2005–2012 | EA113 BWA | |
| Octavia RS II | Skoda | 2004–2013 | EA113 BWA | |

**Piezas con compatibilidad cruzada PQ35:**
- FMIC (front-mount intercooler): tamaño y ubicación idénticos en todos
- Downpipe/cat-back: con adaptadores menores entre marcas
- Coilovers: mismo shock mount y spring perch — 100% intercambiable
- Big brake kits: mismos offset y PCD 5x112 en todos
- Short shifter: mismo shift linkage

**CRÍTICO PQ35:** La generación del motor determina qué turbo aplica:
- EA113 (BPY/BWA): K03 de fábrica → K04 es el upgrade estándar
- EA888 Gen1 (CDN): K03 de fábrica → K04 compatible
- EA888 Gen3 (IS20/IS38 en MQB, NO en PQ35): no confundir

---

### MQB (2012–presente)
**Nombre completo:** Modular Transverse Matrix (Matriz Transversal Modular)
**Arquitectura:** FWD / AWD (4Motion, Haldex Gen5)
**Wheelbase:** Flexible 2620–2686 mm

| Modelo | Marca | Años | Motor principal | Tuning relevante |
|--------|-------|------|----------------|-----------------|
| Golf 7 GTI | Volkswagen | 2013–2020 | EA888 Gen3 IS20 | IS38 swap = referencia |
| Golf 7 R | Volkswagen | 2014–2020 | EA888 Gen3 IS38 | ECU tune crítico |
| Golf 7.5 GTI | Volkswagen | 2017–2021 | EA888 Gen3 IS20+ | |
| Golf 7.5 R | Volkswagen | 2017–2021 | EA888 Gen3 IS38 | |
| Golf 8 GTI | Volkswagen | 2021–presente | EA888 Gen3 IS38+ | MQB-EVO |
| A3 8V / S3 8V | Audi | 2012–2020 | EA888 Gen3 IS20/IS38 | |
| RS3 8V | Audi | 2017–2020 | EA839 5cil DAZA | 5 cil ≠ 4 cil |
| TT 8S | Audi | 2014–2023 | EA888 Gen3 IS38 | |
| León III Cupra | Seat | 2013–2020 | EA888 Gen3 IS20 | |

**Piezas MQB con cross-compatibility:**
- IS38 turbo: bolt-on en cualquier MQB con EA888 Gen3 (GTI→R swap)
- Coilovers: mismo mount design. KW V3 para Golf 7 = mismo para A3 8V
- Big brake kits: PCD 5x112, mismo offset. Frenos S3 8V en GTI 7 = bolt-on
- Intercooler FMIC: mismo tamaño y ubicación en todos los MQB EA888
- ECU tuning: APR, Revo, 034 Motorsport son compatibles entre marcas MQB

**CRÍTICO MQB vs MQB-EVO (Golf 8):**
- Golf 8 usa MQB-EVO. Coilovers del Golf 7 NO son bolt-on directos
- El sistema DCC (amortiguadores adaptativos) requiere verificación
- Algunos colectores de admisión son compatibles, verificar por part number

---

### MLB (2012–presente)
**Nombre completo:** Modular Longitudinal Matrix
**Arquitectura:** RWD-biased AWD
**Para:** Audi A4 B9, A5 F5, Q5 FY, A6 C8

| Modelo | Marca | Años | Motor | HP Std |
|--------|-------|------|-------|--------|
| A4 B9 / S4 B9 | Audi | 2016–presente | EA839 3.0T DNUA | 354 |
| A5 F5 / S5 F5 | Audi | 2017–presente | EA839 3.0T | 354 |
| Q5 FY / SQ5 FY | Audi | 2017–presente | EA839 3.0T | 354 |

**Cross-compatibility MLB:**
- Downpipes EA839: compatible entre A4/A5/Q5 B9/F5/FY mismas generaciones
- Intercooler: misma ubicación en todos los MLB EA839
- ECU: APR Stage 1/2 para EA839 compatible entre plataformas MLB

---

## BMW — Plataformas y Generaciones

### E8x (2004–2013) — Plataforma Serie 1

| Modelo | Código | Años | Motor | Drive |
|--------|--------|------|-------|-------|
| 116i/118i/120i | E81/E87 | 2004–2012 | N43B20, N45B16, N46B20 | RWD |
| 120d | E81/E87 | 2004–2012 | M47N2, N47D20 | RWD |
| 130i | E81/E87 | 2005–2012 | N52B30 | RWD |
| 135i | E82/E88 | 2007–2013 | N54B30, N55B30 | RWD |
| 128i | E82/E88 | 2008–2013 | N52B30 | RWD |
| 1M Coupé | E82 | 2011–2012 | N54B30T0 (350hp) | RWD |

**CRÍTICO E8x Colombia:**
- E82 135i con N54 vs N55: son dos carros diferentes a efectos de tuning
- N54 (2007–2010): twin-turbo, HPFP failures conocidos, solenoide wastegate común
- N55 (2011–2013): single-scroll, más confiable, diferente turbo kit
- 1M usa N54 modificado (N54B30T0): no confundir con 135i N54 estándar

**Cross-compatibility E8x:**
- Coilovers: E82 y E87 comparten MISMO shock mount. KW para uno = KW para el otro
- LCA (Lower Control Arms): idénticos en toda la plataforma E8x
- Brake upgrade: idéntico en E82/E87/E88 (mismo hub y caliper offset)

---

### E9x (2005–2013) — Plataforma Serie 3

| Modelo | Código | Años | Motor | Drive |
|--------|--------|------|-------|-------|
| 318i/320i/323i | E90/E91 | 2005–2012 | N43B20, N46B20, N52B25 | RWD |
| 325i/328i | E90/E91 | 2005–2012 | N52B25, N52B30 | RWD/xDRIVE |
| 330i | E90/E91 | 2005–2012 | N52B30 | RWD |
| 335i | E90/E91/E92 | 2006–2012 | N54B30, N55B30 | RWD/xDRIVE |
| M3 | E90/E92/E93 | 2007–2013 | S65B40 (V8 NA) | RWD |

**CRÍTICO:** M3 E92 usa S65 V8 NA — completamente diferente. NINGUNA pieza de motor comparte con N54/N55.

---

### F2x/F3x (2011–2019)

| Modelo | Código | Años | Motor | Drive |
|--------|--------|------|-------|-------|
| 320i/328i/330i | F30/F31 | 2011–2018 | N20B20, B46B20, B48B20 | RWD/xDRIVE |
| 335i/340i | F30 | 2012–2018 | N55B30, B58B30 | RWD/xDRIVE |
| M3/M4 | F80/F82 | 2014–2020 | S55B30 | RWD |
| 135i/M135i | F20/F21 | 2011–2019 | N55B30, B48B20 | RWD |
| M2 | F87 | 2016–2021 | N55B30 (Comp: S55B30) | RWD |

---

## HONDA — Plataformas Relevantes Colombia

### EK/EG — Civic 5ta/6ta Gen (1992–2000)

| Modelo | Código | Motor de fábrica | Motor swap popular |
|--------|--------|-----------------|-------------------|
| Civic Si (JDM) | EK9 | B16B | B18C5, K20A swap |
| Civic Si (USDM) | EK4 | B16A2 | B18C, K-swap |
| Civic EG (hatch) | EG6 | B16A | B18C, K-swap |
| CRX | EG2 | B16A | B18C, K-swap |

**Cross-compatibility EK/EG:**
- B-swap entre EK y EG: mismo mount pero diferente ECU harness
- K-swap en EG/EK: requiere hasport mount kit, diferente en cada chasis
- Suspensión: EK y EG NO comparten control arms ni knuckles

---

### EP3/DC5 — Civic/RSX Tipo R (2001–2006)

| Modelo | Código | Motor | Especial |
|--------|--------|-------|---------|
| Civic Type R (JDM) | EP3 | K20A | VTEC engagement más agresivo |
| Civic Si (USDM) | EP3 | K20A3 | Non-VTEC head |
| RSX Type-S | DC5 | K20A2 | USDM Type-S |
| RSX Type-R (JDM) | DC5 | K20A | JDM |
| Integra Type-R | DC5 | K20A | Solo JDM |

---

## SUBARU — Plataformas GC/GD/GR/VA

| Código | Modelo | Años | Motor | Notes |
|--------|--------|------|-------|-------|
| GC/GF | Impreza WRX/STI | 1992–2001 | EJ20T, EJ207 | JDM |
| GD/GG | Impreza WRX/STI | 2001–2007 | EJ255, EJ257 | Blob eye / Hawkeye |
| GRB | Impreza WRX STI | 2007–2014 | EJ257 | Hatchback |
| GRF | Impreza WRX | 2010–2014 | EJ255 | |
| VA | WRX/STI | 2014–2021 | FA20, EJ257 | WRX usa FA20; STI mantiene EJ257 |

---

## PART CATEGORIES — Taxonomía Oficial

### Nivel 1 — Categorías Raíz (14)

| ID | Slug | Nombre | Es motor-específico | Universal posible |
|----|------|--------|--------------------|--------------------|
| 01 | `induccion` | Inducción (Turbos, Compresores, Intercoolers) | ✓ | Parcial |
| 02 | `admision` | Admisión (Intakes, Filtros, Pipework) | ✓ | Sí (filtros) |
| 03 | `escape` | Escape (Downpipes, Cat-back, Headers) | ✓ | Parcial |
| 04 | `motor` | Motor y Drivetrain (Internos, Cajas, Embragues) | ✓ | No |
| 05 | `gestion-motor` | Gestión de Motor (ECU, Mapas, Sensores) | ✓ | No |
| 06 | `suspension` | Suspensión (Coilovers, Muelles, Arms) | Parcial | Parcial |
| 07 | `frenos` | Frenos (Discos, Pastillas, Kits, Pinzas) | No | Sí |
| 08 | `transmision` | Transmisión (Diferencial, LSD, Palancas) | ✓ | No |
| 09 | `ruedas` | Ruedas y Llantas (Rines, Neumáticos) | No | Sí |
| 10 | `carroceria` | Carrocería y Exterior (Body kits, Spoilers) | No | Sí |
| 11 | `interior` | Interior y Seguridad (Asientos, Jaulas, Volantes) | No | Sí |
| 12 | `electronica` | Electrónica (Gauges, Cámaras, Audio) | Parcial | Sí |
| 13 | `lubricantes` | Lubricantes y Fluidos | Parcial | Sí |
| 14 | `herramientas` | Herramientas y Diagnóstico | No | Sí |

### Nivel 2 — Subcategorías Clave

**01 — Inducción:**
- `turbos-reconstruidos` — Turbos usados reconstruidos
- `turbos-nuevos-aftermarket` — Turbos nuevos de aftermarket
- `turbos-oem` — Turbos originales
- `superchargers` — Compresores volumétricos
- `intercoolers-fmic` — Front-mount intercoolers
- `intercoolers-tmic` — Top-mount intercoolers
- `blow-off-valves` — BOV / DVs
- `wastegates` — Wastegates externos
- `boost-controllers` — Controladores de boost

**03 — Escape:**
- `downpipes` — Downpipes (con o sin cat)
- `upperpipes` — Upperpipes / test pipes
- `midpipes` — Midpipes
- `cat-back` — Cat-back completo
- `headers` — Colectores / Manifolds
- `resonadores` — Resonadores y back-boxes
- `silenciadores` — Silenciadores finales

**05 — Gestión de Motor:**
- `ecu-standalone` — ECU standalone (Link, Haltech, AEM)
- `piggyback` — Sistemas piggyback (JB4, COBB AP)
- `flash-tunes` — Licencias de tune (APR, Revo, MHD)
- `wideband` — Sondas wideband y controladores
- `data-logging` — Sistemas de datalogging

