# /engineering/runbooks — Procedimientos Operacionales

## Propósito

Los runbooks son instrucciones paso a paso para responder a situaciones operacionales: incidentes, mantenimiento, deployments y operaciones críticas. Un runbook bien escrito permite que **cualquier miembro del equipo técnico** responda a un incidente sin depender del conocimiento exclusivo de una sola persona.

> **Principio:** Si necesitas pensar mucho durante un incidente a las 2AM, el runbook está incompleto.

---

## Cuándo usar un Runbook

- **Incidente en producción** → buscar el runbook del servicio afectado
- **Deployment en producción** → seguir el runbook de deployment
- **Operación de base de datos** → seguir el runbook de DB operations
- **Rollback de una versión** → seguir el runbook de rollback

---

## Runbooks Requeridos para el MVP

| Runbook | Descripción | Prioridad |
|---------|-------------|-----------|
| *(por crear)* `runbook-deploy-production.md` | Cómo hacer un deploy en producción paso a paso | CRÍTICO |
| *(por crear)* `runbook-rollback.md` | Cómo revertir a la versión anterior en Vercel | CRÍTICO |
| *(por crear)* `runbook-supabase-outage.md` | Qué hacer si Supabase está caído | CRÍTICO |
| *(por crear)* `runbook-db-backup-restore.md` | Cómo restaurar la DB desde un backup | CRÍTICO |
| *(por crear)* `runbook-add-admin-user.md` | Cómo agregar un nuevo admin manualmente en la DB | ALTO |
| *(por crear)* `runbook-rotate-secrets.md` | Cómo rotar API keys y secretos de forma segura | ALTO |

---

## Estructura de un Runbook

```markdown
# Runbook: [Nombre del Procedimiento]

**Servicio afectado:** [Supabase / Vercel / Cloudflare / etc.]
**Severidad típica:** Critical / High / Medium
**Tiempo estimado:** X minutos
**Precondiciones:** [Qué necesitas antes de empezar]

## Síntomas
- [Cómo se ve este problema desde el usuario / monitoring]

## Diagnóstico Rápido
1. Verificar [X] en [URL/herramienta]
2. Si [condición] → ir a Sección A
3. Si [otra condición] → ir a Sección B

## Sección A: [Escenario específico]
1. Paso 1 (con comandos exactos si aplica)
2. Paso 2
3. Verificar que funcionó: [cómo sabes que se resolvió]

## Escalación
Si los pasos anteriores no resuelven el problema:
- Contactar: [nombre y método de contacto]
- Abrir ticket en: [herramienta]

## Post-Incidente
- [ ] Documentar en el canal de incidentes
- [ ] Actualizar este runbook si faltó algún paso
- [ ] Crear issue para prevenir la recurrencia
```
