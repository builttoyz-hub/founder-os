# 0002 — Sistema de Reputación en 4 Dimensiones como Diferencial Core

**Estado:** ACTIVE
**Fecha:** 2026-06-26
**Decidido por:** Santiago Tarazona (Fundador)
**Área:** Producto
**Impacto:** Alto

---

## Resumen

PITS MARKET implementa un sistema de reputación multidimensional (descripción, velocidad, estado de la pieza, empaque) en lugar de una calificación simple de 1–5 estrellas, y lo posiciona como el diferencial más importante de la plataforma frente a Facebook Marketplace y grupos de WhatsApp.

---

## Contexto

En el mercado colombiano de autopartes de segunda mano, el problema central no es la falta de oferta ni de demanda — es la falta de confianza. Un comprador en Bogotá que quiere comprarle un turbo a un vendedor en Medellín no tiene ninguna señal confiable de que:
1. La pieza está en el estado que dice el vendedor
2. El vendedor va a responder y despachar
3. Si algo sale mal, hay algún tipo de accountability

Los sistemas de calificación simple (1–5 estrellas de Facebook o MercadoLibre) son insuficientes porque:
- Una sola calificación no dice qué falló
- Los vendedores a menudo presionan a los compradores para que califiquen bien
- Las calificaciones de productos de alto valor (turbos, motores, ECUs) merecen más granularidad que "le doy 4 estrellas"

---

## La Decisión

El sistema de reputación de PITS MARKET tiene 4 dimensiones específicas:

1. **Precisión de la descripción** — ¿La pieza era exactamente como se describió?
2. **Velocidad de respuesta y entrega** — ¿El vendedor respondió y despachó a tiempo?
3. **Estado real de la pieza** — ¿La pieza llegó en las condiciones prometidas?
4. **Calidad del empaque** — ¿La pieza llegó bien protegida?

Cada dimensión se califica de 1.00 a 5.00. El `score_total` es el promedio automático de las 4 dimensiones. El `rating_avg` del vendedor es el promedio de todos sus `score_total`.

El sistema es **inmutable** — las calificaciones no se pueden borrar ni modificar. El vendedor puede responder públicamente a una calificación, pero no puede eliminarla.

---

## Opciones Evaluadas

### Opción A: Rating simple 1–5 estrellas
**Pros:** Familiar para usuarios. Fácil de implementar.
**Contras:** Sin contexto sobre qué falló. No diferencia PITS MARKET de cualquier marketplace. Susceptible a manipulación.

### Opción B: Rating simple + campo de comentario
**Pros:** Más contexto que el rating solo.
**Contras:** Los comentarios son inconsistentes. Difícil de agregar y comparar. La lectura de 47 comentarios es costosa para el comprador.

### Opción C — ELEGIDA: 4 dimensiones específicas + comentario opcional
**Pros:** Cada dimensión mapea exactamente a una preocupación real del comprador. Permite análisis de en qué falla cada vendedor. Crea accountability más específico y más difícil de manipular.
**Contras:** Más fricción en el flujo de calificación. 4 preguntas vs 1.

---

## Por Qué Esta Decisión

Las 4 dimensiones no son arbitrarias — cada una existe porque un comprador de autopartes de segunda mano lo necesita saber:

- **Descripción:** Un turbo descrito como "perfecto" que llega con el turbine shaft con juego excesivo es el fraude más común en el mercado
- **Velocidad:** En un mercado donde el comprador a veces necesita la pieza para el carro de trabajo, la velocidad de respuesta importa tanto como el precio
- **Estado real:** Puede estar bien descrito pero llegar dañado en el envío — estas son dimensiones separadas
- **Empaque:** Un intercooler en caja de cartón sin protección puede llegar con las aletas aplastadas — el vendedor que empaca bien cuida su reputación

---

## Consecuencias

### Positivas
- La reputación de PITS MARKET se convierte en un activo real para los vendedores honestos
- Los compradores toman mejores decisiones con información granular
- El sistema hace que el comportamiento honesto sea el comportamiento racional
- Diferencia PITS MARKET de cualquier alternativa actual en Colombia

### Negativas / Trade-offs
- Mayor fricción en el flujo de calificación post-transacción (4 preguntas vs 1)
- Requiere suficientes transacciones para que el rating sea estadísticamente significativo
- En el MVP sin transacciones mediadas, no hay garantía de que el comprador realmente califica

### Riesgos

| Riesgo | Probabilidad | Impacto | Mitigación |
|--------|-------------|---------|-----------|
| Baja tasa de calificación (los compradores no vuelven a calificar) | Alta | Alto | CTA de calificación en el momento de mayor satisfacción. Email de recordatorio a los 3 días. |
| Review bombing (competidores o enemigos poniendo 1 estrella sin comprar) | Media | Alto | Registrar IP, device, y tiempo entre ver el listing y calificar. En V2: transacción verificada antes de poder calificar. |

---

## Criterios de Revisión

```
Revisar si:
- La tasa de calificación post-transacción es < 20% después de 3 meses de operación
- Los vendedores se quejan sistemáticamente de injusticia en el sistema
- Aparece evidencia de manipulación masiva del sistema
```

---

## Conexiones

**Decisiones relacionadas:**
- 0001 — El sistema de reputación es el incentivo para que los vendedores quieran plans premium con mayor visibilidad

**Documentos relacionados:**
- `engineering/database/DATABASE_BIBLE_v1.md` — Sección 12 (Estrategia de Reputación)
- `design/trust-ui/README.md` — Cómo se comunica visualmente la reputación

---

*Decisión 0002 · ACTIVE · 2026-06-26 · PITS MARKET*
