# /engineering — Documentación Técnica de Ingeniería

## Propósito

Todo lo técnico vive aquí. Esta carpeta es la biblia de ingeniería de PITS MARKET: cómo está construido, por qué está construido así, cómo operar el sistema, y cómo evolucionar la arquitectura sin romper lo que existe.

> **Regla:** Ninguna decisión de arquitectura es oficial hasta estar documentada en esta carpeta. El código es la implementación. Esta carpeta es el razonamiento.

---

## Subcarpetas

### `/architecture` — Decisiones de arquitectura del sistema
El sistema completo documentado: stack, capas, flujos, diagramas. La primera lectura obligatoria para cualquier desarrollador nuevo.

**Documento clave:** `SYSTEM_ARCHITECTURE_v1.md`

### `/database` — Schema, migraciones y políticas de datos
El diseño completo de la base de datos: tablas, relaciones, índices, triggers, políticas de RLS y estrategia de migración.

**Documento clave:** `DATABASE_BIBLE_v1.md`

### `/api` — Contratos de API
Los contratos de cada endpoint: qué acepta, qué retorna, qué errores puede lanzar. La documentación que los clientes (web, mobile, API pública) consumen.

### `/security` — Políticas y auditorías de seguridad
Modelo de amenazas, controles por capa, políticas de acceso, historial de auditorías y vulnerabilidades resueltas.

### `/runbooks` — Procedimientos operacionales
Cómo responder a incidentes, hacer deployments, hacer rollbacks, gestionar backups y ejecutar operaciones críticas. Documentación de respuesta de emergencia.

### `/adr` — Architecture Decision Records
Registro de decisiones de arquitectura importantes: qué se decidió, por qué, qué alternativas se evaluaron, y cuáles son las consecuencias esperadas.

---

## Convención de Nombres

```
[tipo]-[descripcion]-v[N].md

Tipos por carpeta:
  architecture/   → SYSTEM_ARCHITECTURE_v1.md, SYSTEM_ARCHITECTURE_v2.md
  database/       → DATABASE_BIBLE_v1.md, migration-add-reviews-table.md
  api/            → api-contract-listings-v1.md, api-contract-search-v1.md
  security/       → security-threat-model-v1.md, security-audit-2026-07.md
  runbooks/       → runbook-supabase-outage.md, runbook-deploy-production.md
  adr/            → adr-001-supabase-over-custom-backend.md

Prefijo numérico para ADRs: adr-001, adr-002, etc.
```

---

## Stack Técnico de Referencia Rápida

| Capa | Tecnología | Versión |
|------|-----------|---------|
| Frontend | Next.js + TypeScript + Tailwind | 14.x |
| Database | PostgreSQL via Supabase | 15+ |
| Auth | Supabase Auth | latest |
| Storage | Supabase Storage | latest |
| Hosting | Vercel | latest |
| CDN | Cloudflare | Pro |
| Email | Resend | latest |
| Error tracking | Sentry | latest |
| Analytics | PostHog | latest |

---

*Propietario: CTO · Requiere aprobación del CTO para cambios en `/architecture` y `/database`*
