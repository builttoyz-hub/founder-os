# /decisions — Registro de Decisiones de Empresa

## Propósito

Este es el registro oficial de las decisiones importantes de PITS MARKET. No solo decisiones técnicas (que viven en `/engineering/adr/`) — sino decisiones de negocio, producto, growth, y estrategia que tienen consecuencias duraderas y merecen estar documentadas con su contexto completo.

> **Por qué existe esto:** Las empresas toman miles de decisiones. Las que importan — las que definen el producto, el negocio, y la cultura — a menudo se toman en conversaciones de WhatsApp y se olvidan. Tres meses después, nadie recuerda por qué se decidió algo. Este archivo lo recuerda por nosotros.

---

## Diferencia entre `/decisions` y `/engineering/adr`

| `/decisions` | `/engineering/adr` |
|--------------|-------------------|
| Decisiones de negocio, producto y estrategia | Decisiones de arquitectura técnica |
| Quién puede comprar en la plataforma, cómo monetizamos, qué features incluye el MVP | Qué base de datos usar, cómo manejar la autenticación, qué framework elegir |
| Audiencia: todo el equipo, inversionistas, futuros empleados | Audiencia: equipo técnico |
| Frecuencia: cuando hay una decisión estratégica importante | Frecuencia: cuando hay una decisión técnica de arquitectura |

**Regla práctica:** Si la decisión cambiaría cómo un vendedor experimenta la plataforma, cómo ganamos dinero, o qué tipo de empresa somos — va en `/decisions`. Si cambia cómo el sistema funciona internamente — va en `/engineering/adr`.

---

## Sistema de Numeración

```
[NNNN]-[titulo-kebab-case].md

NNNN: 4 dígitos, secuencial, con ceros a la izquierda
Título: descriptivo, corto, sin artículos

Ejemplos:
  0001-paid-listings.md
  0002-pits-trust.md
  0003-whatsapp-strategy.md
  0004-colombia-first-expansion.md
  0015-remove-commission-model.md
  0023-hire-first-engineer.md
```

**Regla:** El número es permanente. Una decisión 0007 siempre es 0007, aunque sea reemplazada por una posterior. La nueva decisión tendrá su propio número y referenciará la anterior.

---

## Estados de una Decisión

| Estado | Descripción |
|--------|-------------|
| `PROPOSED` | En consideración, no aprobada aún |
| `ACTIVE` | Decisión vigente y en implementación |
| `SUPERSEDED` | Reemplazada por otra decisión (referencia al número nuevo) |
| `REVERSED` | Se tomó pero se revirtió (con fecha y razón) |
| `DEPRECATED` | Ya no aplica porque el contexto cambió completamente |

---

## Índice de Decisiones

| # | Título | Estado | Fecha | Área |
|---|--------|--------|-------|------|
| [0001](0001-paid-listings.md) | Listings gratuitos en el MVP, planes de pago en Beta | ACTIVE | 2026-06-26 | Producto / Negocio |
| [0002](0002-pits-trust.md) | Sistema de reputación en 4 dimensiones como diferencial | ACTIVE | 2026-06-26 | Producto |
| [0003](0003-whatsapp-strategy.md) | WhatsApp como canal de contacto en MVP, mensajería interna en V2 | ACTIVE | 2026-06-26 | Producto |

*Actualizar este índice cada vez que se agrega una decisión.*

---

## Template

Ver `TEMPLATE-decision.md` en esta carpeta.

---

## Quién Puede Crear Decisiones

Cualquier miembro del equipo puede **proponer** una decisión (estado PROPOSED). Solo el Fundador puede cambiar el estado a ACTIVE. Las decisiones en `/decisions` son formales — no son ideas de Slack.

---

*Propietario: Fundador · Revisión: Cada vez que se toma una decisión importante*
