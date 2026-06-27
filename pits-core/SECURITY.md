# Security Policy — PITS MARKET

## Scope

Este documento aplica a:

- **pitsmarket.co** — Plataforma web principal
- **api.pitsmarket.co** — API pública (cuando esté disponible)
- **Este repositorio** — pits-core en GitHub

---

## Versiones con Soporte de Seguridad

| Versión | Soporte |
|---------|---------|
| MVP (0.x) | ✅ Activo |
| Beta (0.9.x) | ✅ Activo cuando esté disponible |
| Versiones anteriores | ❌ Sin soporte |

---

## Reportar una Vulnerabilidad

**NO abras un Issue público para reportar vulnerabilidades de seguridad.**

Los Issues públicos son visibles para todos y pueden ser explotados antes de que se solucionen.

### Proceso de Reporte Responsable

1. **Email:** builttoyz@gmail.com
2. **Asunto:** `[SECURITY] Descripción breve de la vulnerabilidad`
3. **Incluir en el reporte:**
   - Descripción de la vulnerabilidad
   - Pasos para reproducirla
   - Impacto potencial
   - Versión/URL afectada
   - Tu nombre o alias (para crédito, si lo deseas)

### Qué esperar después del reporte

| Acción | Timeline |
|--------|----------|
| Confirmación de recepción | 48 horas |
| Evaluación inicial de severidad | 5 días hábiles |
| Plan de remediación compartido con el reportante | 10 días hábiles |
| Fix en producción (vulnerabilidades críticas) | 15 días hábiles |
| Fix en producción (vulnerabilidades moderadas) | 30 días hábiles |
| Divulgación pública (si el reportante lo desea) | Después del fix |

---

## Vulnerabilidades Fuera de Scope

Los siguientes no son considerados vulnerabilidades de seguridad para efectos de este programa:

- Rate limiting en endpoints públicos de solo lectura
- Enumeración de IDs en recursos públicos (listings)
- Falta de DNSSEC
- Clickjacking en páginas sin acciones sensibles
- Bugs de UI que no tienen impacto de seguridad
- Resultados de scanners automáticos sin contexto
- Ataques que requieren acceso físico al dispositivo del usuario

---

## Datos Sensibles en el Repositorio

Si descubres que este repositorio contiene credenciales, API keys, o datos personales expuestos:

1. Reportar inmediatamente a builttoyz@gmail.com
2. **No distribuir ni usar** la información encontrada
3. No crear Issues ni Pull Requests con la información expuesta

Las credenciales expuestas serán rotadas inmediatamente y el historial de commits será limpiado.

---

## Prácticas de Seguridad del Equipo

### Obligatorias para acceso al repositorio

- [ ] 2FA habilitado en la cuenta de GitHub
- [ ] No compartir credenciales de acceso con terceros
- [ ] Nunca commitear secretos (ver `.gitignore`)
- [ ] Revisar Pull Requests antes de hacer merge (nunca auto-merge en `main`)

### Para el equipo técnico (pitsmarket.co)

- [ ] Supabase service_role key NUNCA en el frontend
- [ ] Variables de entorno solo en Vercel Dashboard, nunca en el repo
- [ ] RLS activado en todas las tablas de Supabase
- [ ] Rate limiting configurado en Cloudflare y API Routes
- [ ] Logs de acceso revisados semanalmente

---

## Historial de Vulnerabilidades Públicas

*Ninguna reportada hasta la fecha.*

---

## Créditos

Agradecemos a los investigadores de seguridad que repotan responsablemente. Los reportantes serán reconocidos en esta sección (con su consentimiento).

---

*PITS MARKET · Última actualización: Junio 2026*
