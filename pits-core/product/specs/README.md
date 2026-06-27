# /product/specs — Especificaciones Funcionales

## Propósito

Una spec es el contrato entre Producto e Ingeniería. Define exactamente qué se va a construir antes de que se escriba una línea de código.

> **Regla:** Ingeniería no inicia desarrollo sin una spec en estado `Approved` en esta carpeta.

## Estados de una Spec

| Estado | Significado |
|--------|-------------|
| `Draft` | En redacción, no lista para review |
| `In Review` | Lista para revisión del equipo |
| `Approved` | Aprobada por Fundador. Se puede iniciar desarrollo. |
| `Implemented` | Feature construido e implementado |
| `Deprecated` | Feature que fue descontinuado |

## Convención de Nombres

```
spec-[nombre-del-feature]-v[N].md

Ejemplos:
  spec-publish-listing-v1.md
  spec-marketplace-search-v1.md
  spec-buyer-contact-whatsapp-v1.md
  spec-admin-moderation-v1.md
  spec-user-registration-v1.md
```

## Specs del MVP

| Spec | Estado | Feature |
|------|--------|---------|
| *(por crear)* `spec-publish-listing-v1.md` | — | F1 — Publicar pieza |
| *(por crear)* `spec-marketplace-search-v1.md` | — | F2 — Encontrar pieza |
| *(por crear)* `spec-listing-detail-v1.md` | — | F3 — Ver detalle |
| *(por crear)* `spec-auth-registration-v1.md` | — | F4 — Registro y login |
| *(por crear)* `spec-admin-panel-v1.md` | — | F5 — Panel de admin |
