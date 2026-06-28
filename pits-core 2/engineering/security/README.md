# /engineering/security — Seguridad

## Propósito

Documenta el modelo de seguridad de PITS MARKET: amenazas identificadas, controles implementados, auditorías realizadas y políticas de acceso. Es la referencia para tomar decisiones de seguridad informadas.

> **Regla:** Toda vulnerabilidad resuelta se documenta aquí, aunque sea menor. El historial de seguridad es tan valioso como la seguridad actual.

---

## ¿Qué va aquí?

| Documento | Descripción |
|-----------|-------------|
| `security-threat-model-v1.md` | Modelo de amenazas completo: actores, vectores, controles |
| `security-audit-[fecha].md` | Resultados de auditorías de seguridad externas |
| `security-policy-access-control.md` | Política de acceso a sistemas y datos |
| `security-incident-log.md` | Registro de incidentes de seguridad (incluso los menores) |
| `security-checklist-launch.md` | Checklist de seguridad antes del lanzamiento |

---

## Checklist de Seguridad — MVP Launch

```markdown
## Infraestructura
- [ ] HTTPS forzado en todos los dominios
- [ ] Headers de seguridad configurados (CSP, HSTS, X-Frame-Options)
- [ ] Cloudflare WAF activo
- [ ] Rate limiting en API Routes (20 req/min por IP)

## Base de Datos (Supabase)
- [ ] RLS activado en todas las tablas
- [ ] service_role key NUNCA en el cliente
- [ ] Backup automático diario verificado
- [ ] Conexiones desde IPs no autorizadas bloqueadas

## Autenticación
- [ ] 2FA habilitado para cuentas de GitHub y Supabase
- [ ] Variables de entorno en Vercel Dashboard (nunca en código)
- [ ] No hay secretos en el historial de commits (gitleaks)

## Aplicación
- [ ] Input sanitizado con Zod en todos los formularios
- [ ] Números de WhatsApp validados antes de guardar
- [ ] Imágenes validadas por tipo MIME real (no solo extensión)
- [ ] Errores del servidor no exponen información técnica al cliente
```

---

## Convención de Nombres

```
security-[tipo]-[descripcion]-[fecha-si-aplica].md

Tipos: threat-model | audit | policy | incident | checklist

Ejemplos:
  security-threat-model-v1.md
  security-audit-external-2026-10.md
  security-policy-data-access.md
  security-incident-log.md
```
