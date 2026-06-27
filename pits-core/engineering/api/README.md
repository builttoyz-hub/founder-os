# /engineering/api — Contratos de API

## Propósito

Los contratos de API definen exactamente qué acepta cada endpoint, qué retorna, y qué errores puede lanzar. Son el contrato entre el backend y cualquier cliente (web, mobile, integradores).

> **Regla:** Si un endpoint no tiene un contrato documentado aquí, no está en producción.

## Convención de Nombres

```
api-contract-[recurso]-v[N].md

Ejemplos:
  api-contract-listings-v1.md
  api-contract-search-v1.md
  api-contract-auth-v1.md
  api-contract-images-v1.md
  api-contract-public-v1.md     ← API pública (v2+)
```

## APIs del MVP (4 endpoints)

| Endpoint | Archivo | Estado |
|----------|---------|--------|
| `POST /api/images/upload-url` | *(por crear)* | Planned |
| `POST /api/contact-click` | *(por crear)* | Planned |
| `POST /api/send-email` | *(por crear)* | Planned |
| `GET /api/og-image/[slug]` | *(por crear)* | Planned |

## Template de Contrato

```markdown
# API Contract: [Nombre del Endpoint]

**Versión:** v1
**URL:** /api/[path]
**Método:** GET | POST | PUT | DELETE
**Autenticación:** None | Required | Admin only

## Descripción
Qué hace este endpoint en una oración.

## Request

### Headers
| Header | Valor | Requerido |
|--------|-------|-----------|
| Content-Type | application/json | Sí |
| Authorization | Bearer {token} | Si requiere auth |

### Body (para POST/PUT)
| Campo | Tipo | Requerido | Descripción |
|-------|------|-----------|-------------|
| campo1 | string | Sí | Descripción |

## Response

### 200 OK
```json
{
  "success": true,
  "data": { ... }
}
```

### Errores
| Código | Descripción | Cuándo ocurre |
|--------|-------------|---------------|
| 400 | Bad Request | Input inválido |
| 401 | Unauthorized | Sin autenticación |
| 403 | Forbidden | Sin permisos |
| 404 | Not Found | Recurso no existe |
| 500 | Server Error | Error inesperado |

## Ejemplo de uso
```
