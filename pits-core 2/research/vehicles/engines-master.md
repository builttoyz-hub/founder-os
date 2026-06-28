# Engines Master — Motores del Mercado Colombiano

> Fuente de verdad de todos los códigos de motor relevantes para el mercado de tuning colombiano.
> Confianza: VERIFIED = doble verificado con fuentes oficiales + comunidad. COMMUNITY = validado por comunidad. UNVERIFIED = pendiente.

---

## FAMILIA BMW N-Series (2006–presente)

| Código | Alias | CC | Cil. | Asp. | HP Std | HP Max | Tune | Confianza |
|--------|-------|-----|------|------|--------|--------|------|-----------|
| `N20B20` | N20 | 1997 | 4 | TURBO | 184 | 245 | MHD, JB4 | VERIFIED |
| `N26B20` | N26 | 1997 | 4 | TURBO | 245 | 245 | MHD (USA spec) | VERIFIED |
| `N43B20` | N43 | 1995 | 4 | NA | 143 | 156 | Limitado | VERIFIED |
| `N45B16` | N45 | 1596 | 4 | NA | 115 | 122 | Limitado | VERIFIED |
| `N46B20` | N46 | 1995 | 4 | NA | 143 | 170 | Limitado | VERIFIED |
| `N52B25` | N52 | 2497 | 6 | NA | 177 | 218 | Básico | VERIFIED |
| `N52B30` | N52, N52B30A | 2996 | 6 | NA | 258 | 272 | Básico | VERIFIED |
| `N54B30` | N54 | 2979 | 6 | TWIN_TURBO | 306 | 326 | MHD, JB4, Bootmod3 | VERIFIED |
| `N55B30` | N55, N55B30O0 | 2979 | 6 | TURBO | 306 | 340 | MHD, JB4, Bootmod3 | VERIFIED |
| `S55B30` | S55 | 2979 | 6 | TWIN_TURBO | 431 | 460 | Bootmod3, MHD | VERIFIED |
| `B46B20` | B46, B46A20B | 1998 | 4 | TURBO | 156 | 192 | Bootmod3, MHD | VERIFIED |
| `B48B20` | B48 | 1998 | 4 | TURBO | 184 | 252 | Bootmod3, MHD | VERIFIED |
| `B58B30` | B58 | 2998 | 6 | TURBO | 340 | 382 | Bootmod3, MHD | VERIFIED |

**Notas BMW N/B-Series:**
- N54 y N55 NO son intercambiables — tienen diferente bloque y sistema de admisión
- B48 reemplaza al N20 en modelos post-2017; turbo y intercooler NO son compatibles
- S55 (M3/M4) comparte block con N55 pero cabeza y sistema de inducción son diferentes
- N54 twin-scroll vs N55 single-scroll: downpipes NO son intercambiables entre sí

---

## FAMILIA BMW M-Series (clásicos en Colombia)

| Código | Alias | CC | Cil. | Asp. | HP Std | HP Max | Tune | Confianza |
|--------|-------|-----|------|------|--------|--------|------|-----------|
| `M20B20` | M20 | 1990 | 6 | NA | 125 | 130 | Mecánico | VERIFIED |
| `M20B25` | M20 | 2494 | 6 | NA | 170 | 177 | Mecánico | VERIFIED |
| `M50B25` | M50 | 2494 | 6 | NA | 192 | 192 | Aftermarket | VERIFIED |
| `M52B25` | M52 | 2494 | 6 | NA | 170 | 192 | Aftermarket | VERIFIED |
| `M52B28` | M52TU | 2793 | 6 | NA | 193 | 193 | Aftermarket | VERIFIED |
| `M54B25` | M54 | 2494 | 6 | NA | 192 | 192 | Aftermarket | VERIFIED |
| `M54B30` | M54 | 2979 | 6 | NA | 231 | 231 | Aftermarket | VERIFIED |
| `S54B32` | S54 | 3246 | 6 | NA | 343 | 364 | Aftermarket premium | VERIFIED |

---

## FAMILIA VOLKSWAGEN AG — EA-Series

| Código | Alias | CC | Cil. | Asp. | HP Std | HP Max | Aplicaciones | Confianza |
|--------|-------|-----|------|------|--------|--------|-------------|-----------|
| `EA111-1.4T` | 1.4 TSI CAV | 1390 | 4 | TWINCHARGED | 122 | 185 | Polo GTI, Golf 5 1.4 | VERIFIED |
| `EA113-2.0T` | EA113, BPY, BWA, AXX | 1984 | 4 | TURBO | 200 | 265 | Golf GTI 5, Audi A3 8P S-line, S3 8P primera gen | VERIFIED |
| `EA888-1` | EA888 Gen1, CDN, CDA | 1984 | 4 | TURBO | 200 | 265 | Golf GTI 6 (2009-2012), Audi A3 8P facelift | VERIFIED |
| `EA888-2` | EA888 Gen2, CEA, CJX | 1984 | 4 | TURBO | 211 | 265 | Golf GTI 7 base, A3 8V | VERIFIED |
| `EA888-3` | EA888 Gen3, IS20, IS38 | 1984 | 4 | TURBO | 220 | 310 | Golf GTI 7.5, Golf R 7, Audi S3 8V | VERIFIED |
| `EA839-3.0T` | EA839, DNUA, DJHA | 2995 | 6 | TURBO | 354 | 450 | Audi S4 B9, S5 F5, SQ5 FY | VERIFIED |
| `EA897-4.0T` | EA897 Gen1 | 3993 | 8 | TWIN_TURBO | 420 | 450 | Audi RS5 B8, RS4 B8, S8 D4 | COMMUNITY |

**CRÍTICO — EA113 vs EA888 NO son intercambiables:**
- EA113 (BPY/BWA/AXX): bloque diferente, no tiene cadena de distribución, correa
- EA888 Gen1 (CDN/CDA): introduce cadena. Turbo, intercooler y admisión incompatibles con EA113
- EA888 Gen2 vs Gen3: comparten block pero el IS38 del Gen3 NO es bolt-on en Gen2 sin modificaciones
- Turbo IS20 (Golf GTI 7) vs IS38 (Golf R 7): mismo conector pero mapa de ECU diferente

---

## FAMILIA VOLKSWAGEN AG — VR6 y W12

| Código | Alias | CC | Cil. | Asp. | HP Std | HP Max | Confianza |
|--------|-------|-----|------|------|--------|--------|-----------|
| `VR6-2.8` | VR6, AAA, AFP | 2792 | 6 | NA | 174 | 192 | VERIFIED |
| `VR6-3.2` | VR6 3.2, AXZ, BDB | 3189 | 6 | NA | 241 | 250 | VERIFIED |
| `VR6-3.6` | VR6 3.6, BHK, BWS | 3597 | 6 | NA | 280 | 300 | COMMUNITY |

---

## FAMILIA HONDA — K-Series (JDM/USDM en Colombia)

| Código | Alias | CC | Cil. | Asp. | HP Std | HP Max | VTEC | Confianza |
|--------|-------|-----|------|------|--------|--------|------|-----------|
| `K20A` | K20A JDM | 1998 | 4 | NA | 221 | 221 | i-VTEC | VERIFIED |
| `K20A2` | K20A2 USDM (RSX Type-S) | 1998 | 4 | NA | 200 | 210 | i-VTEC | VERIFIED |
| `K20A3` | K20A3 USDM (RSX base) | 1998 | 4 | NA | 160 | 160 | VTEC | VERIFIED |
| `K20C1` | K20C (Civic Type R FK8) | 1996 | 4 | TURBO | 306 | 320 | i-VTEC Turbo | VERIFIED |
| `K20Z3` | K20Z3 (Si) | 1998 | 4 | NA | 197 | 210 | i-VTEC | VERIFIED |
| `K24A` | K24A JDM | 2354 | 4 | NA | 160 | 200 | i-VTEC | VERIFIED |
| `K24A2` | K24A2 (Accord Euro R) | 2354 | 4 | NA | 200 | 210 | i-VTEC | VERIFIED |
| `K24Z7` | K24Z7 (Accord 8) | 2354 | 4 | NA | 177 | 201 | i-VTEC | VERIFIED |

**CRÍTICO — K-Series compatibility:**
- K20A (JDM DC5) y K20A2 (USDM DC5): diferentes mapas de VTEC. Ecu, intake, y header son intercambiables
- K20 vs K24: mismo block design, cabezas NO son intercambiables sin modifications
- K20C1 (Turbo FK8): completamente diferente. NO comparte piezas con K20A/A2
- Todas las K-series: VTEC solenoid location different entre generaciones — verificar antes de swap

---

## FAMILIA HONDA — B-Series y D-Series

| Código | Alias | CC | Cil. | Asp. | HP Std | HP Max | VTEC | Confianza |
|--------|-------|-----|------|------|--------|--------|------|-----------|
| `B16A` | B16A JDM (CR-X SiR) | 1595 | 4 | NA | 160 | 170 | VTEC | VERIFIED |
| `B16A2` | B16A2 USDM (Civic Si EK) | 1595 | 4 | NA | 160 | 160 | VTEC | VERIFIED |
| `B16B` | B16B (Civic Type R EK9) | 1595 | 4 | NA | 185 | 185 | VTEC | VERIFIED |
| `B18B1` | B18B (Integra LS) | 1797 | 4 | NA | 142 | 142 | Non-VTEC | VERIFIED |
| `B18C1` | B18C USDM (Integra GS-R) | 1797 | 4 | NA | 170 | 178 | VTEC | VERIFIED |
| `B18C5` | B18C (Integra Type R) | 1797 | 4 | NA | 195 | 200 | VTEC | VERIFIED |
| `D15B` | D15B JDM (VTEC) | 1493 | 4 | NA | 105 | 130 | VTEC | COMMUNITY |
| `D16A` | D16A (Civic EG) | 1590 | 4 | NA | 125 | 130 | Non-VTEC | VERIFIED |

---

## FAMILIA SUBARU — EJ-Series

| Código | Alias | CC | Cil. | Asp. | HP Std | HP Max | Config | Confianza |
|--------|-------|-----|------|------|--------|--------|--------|-----------|
| `EJ20T` | EJ20 (WRX JDM) | 1994 | 4 | TURBO | 250 | 280 | FLAT | VERIFIED |
| `EJ205` | EJ205 (WRX USDM) | 1994 | 4 | TURBO | 227 | 250 | FLAT | VERIFIED |
| `EJ207` | EJ207 (STI JDM 6MT) | 1994 | 4 | TURBO | 280 | 320 | FLAT | VERIFIED |
| `EJ255` | EJ255 (WRX 2006+) | 2457 | 4 | TURBO | 243 | 265 | FLAT | VERIFIED |
| `EJ257` | EJ257 (STI USDM) | 2457 | 4 | TURBO | 305 | 340 | FLAT | VERIFIED |
| `FA20DIT` | FA20 (WRX 2015+) | 1998 | 4 | TURBO | 268 | 300 | FLAT | VERIFIED |
| `FA24` | FA24 (WRX 2022+) | 2387 | 4 | TURBO | 271 | 315 | FLAT | VERIFIED |

**CRÍTICO — EJ vs FA:**
- EJ257 (STI) y EJ255 (WRX) NO son intercambiables sin modificaciones al motor mount y ECU
- FA20 reemplaza EJ20. Completamente diferente. Ninguna pieza es compatible
- EJ207 (JDM) vs EJ257 (USDM STI): diferentes pistones, bielas y head bolts — NUNCA mezclar partes internas

---

## FAMILIA MITSUBISHI — 4G-Series

| Código | Alias | CC | Cil. | Asp. | HP Std | HP Max | Confianza |
|--------|-------|-----|------|------|--------|--------|-----------|
| `4G63T` | 4G63 (EVO I-IX) | 1997 | 4 | TURBO | 247 | 330 | VERIFIED |
| `4G64` | 4G64 (Galant, non-turbo) | 2350 | 4 | NA | 145 | 160 | COMMUNITY |
| `4B11T` | 4B11 (EVO X) | 1998 | 4 | TURBO | 291 | 330 | VERIFIED |

**CRÍTICO:** 4G63T (EVO IX y anteriores) y 4B11T (EVO X) NO comparten absolutamente ninguna pieza interna.

---

## FAMILIA TOYOTA/LEXUS — JZ y GR-Series

| Código | Alias | CC | Cil. | Asp. | HP Std | HP Max | Confianza |
|--------|-------|-----|------|------|--------|--------|-----------|
| `1JZ-GTE` | 1JZ | 2492 | 6 | TWIN_TURBO | 276 | 320 | VERIFIED |
| `2JZ-GE` | 2JZ NA | 2997 | 6 | NA | 220 | 230 | VERIFIED |
| `2JZ-GTE` | 2JZ | 2997 | 6 | TWIN_TURBO | 276 | 330 | VERIFIED |
| `G16E-GTS` | GR Four (GR Yaris) | 1618 | 3 | TURBO | 261 | 300 | COMMUNITY |

---

## FAMILIA NISSAN/INFINITI — SR, RB, VQ-Series

| Código | Alias | CC | Cil. | Asp. | HP Std | HP Max | Confianza |
|--------|-------|-----|------|------|--------|--------|-----------|
| `SR20DET` | SR20 (S13/S14 JDM) | 1998 | 4 | TURBO | 205 | 250 | VERIFIED |
| `RB20DET` | RB20 | 1998 | 6 | TURBO | 212 | 230 | COMMUNITY |
| `RB25DET` | RB25 | 2498 | 6 | TURBO | 247 | 280 | VERIFIED |
| `RB26DETT` | RB26 (R32-R34 GT-R) | 2568 | 6 | TWIN_TURBO | 276 | 330 | VERIFIED |
| `VQ35DE` | VQ35 NA | 3498 | 6 | NA | 287 | 306 | VERIFIED |
| `VQ35HR` | VQ35HR (350Z) | 3498 | 6 | NA | 306 | 315 | VERIFIED |
| `VQ37VHR` | VQ37 (370Z) | 3696 | 6 | NA | 328 | 350 | VERIFIED |

