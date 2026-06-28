# North Star Metric — PITS MARKET

## La North Star

> **Transacciones completadas por semana** (contactos WhatsApp documentados que llevan a venta confirmada)

---

## Por Qué Esta Métrica

La North Star de PITS MARKET es la única métrica que prueba que el producto funciona para **ambos lados** del marketplace simultáneamente:

- Un comprador encontró la pieza que buscaba ✓
- Un vendedor cerró una venta ✓
- La plataforma fue el puente que lo hizo posible ✓

Si solo medimos "usuarios registrados", podemos tener 10,000 usuarios que nunca compraron ni vendieron nada. Si solo medimos "piezas publicadas", podemos tener inventario sin demanda. La transacción completada es el único número que no miente.

---

## Cómo Se Mide

**En el MVP (sin transacciones mediadas):**

Una "transacción completada" en el MVP = un click en "Contactar por WhatsApp" + confirmación posterior del vendedor de que la venta se concretó.

El proceso de captura:
1. `contact_count` en la tabla `listings` se incrementa automáticamente en cada click
2. Semanalmente, el admin contacta por WhatsApp a los vendedores con más clicks recientes para confirmar ventas
3. Las ventas confirmadas se registran en `/metrics/dashboards/` del dashboard de la semana

**En Beta (con mensajería interna):**

Una "transacción completada" = conversación en mensajería interna marcada como "cerrada con venta" por alguna de las partes.

**En V2 (con transacciones mediadas):**

Una "transacción completada" = transacción procesada por la plataforma con pago confirmado.

---

## Targets por Fase

| Fase | North Star Target | Timeline |
|------|-----------------|----------|
| MVP — Semana 1 post-lanzamiento | 1 transacción/semana | Julio 2026 |
| MVP — Mes 1 | 5 transacciones/semana | Agosto 2026 |
| Beta | 25 transacciones/semana | Octubre 2026 |
| V1 | 100 transacciones/semana | Enero 2027 |
| V2 | 500 transacciones/semana | Julio 2027 |

---

## Métricas de Soporte

La North Star no sube sola. Estas métricas de soporte explican por qué sube o baja:

| Métrica de soporte | Qué mide | Relación con NS |
|-------------------|----------|-----------------|
| Listings activos | ¿Hay suficiente inventario? | Sin inventario, no hay transacciones |
| Contact rate (clicks WA / visitas detalle) | ¿Los compradores quieren contactar? | Proxy de demanda |
| Listing quality score | ¿Los avisos tienen fotos y descripción? | Listings de calidad convierten más |
| Tiempo de respuesta del vendedor | ¿Los vendedores responden? | Respuesta lenta mata la transacción |
| Seller repeat rate | ¿Los vendedores publican más piezas? | Inventario saludable y recurrente |

---

## Señales de Alarma

| Señal | Qué significa | Acción |
|-------|--------------|--------|
| NS baja 2 semanas consecutivas | Algo roto en el funnel | Revisar cada paso del flujo B |
| NS sube pero contact rate baja | Más volumen, menor calidad | Revisar calidad del inventario |
| NS estable pero seller repeat rate baja | Vendedores no están satisfechos | Entrevistar vendedores activos |
| NS sube pero buyer repeat rate baja | Los compradores no vuelven | El producto no retiene compradores |

---

*Versión 1.0 — Junio 2026 · PITS MARKET*
