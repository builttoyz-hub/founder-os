# VERSION — PITS CORE

## Versión Actual

```
v0.3.0
```

**Estado:** Production-Ready Foundation
**Fecha:** 28 de junio de 2026
**Tipo:** Knowledge Repository + Automotive Knowledge Graph

---

## Historial de Versiones

| Versión | Fecha | Tipo | Descripción |
|---------|-------|------|-------------|
| v0.3.0 | 2026-06-28 | MINOR | CTO Architecture Review. AKG completo. Inconsistencias resueltas. |
| v0.2.0 | 2026-06-26 | MINOR | Módulos V2: constitution, community, metrics, design, decisions |
| v0.1.0 | 2026-06-26 | MINOR | Foundation: estructura base, 17 carpetas, archivos raíz |
| v0.0.1 | 2026-06-26 | INITIAL | Inicialización del repositorio |

---

## Semver Aplicado a PITS CORE

Este repositorio usa Semantic Versioning adaptado para repositorios de conocimiento:

| Tipo | Cuándo incrementar | Ejemplo |
|------|--------------------|---------|
| `MAJOR` (X.0.0) | Reestructuración completa del repositorio. Renombrar carpetas principales. | v1.0.0 cuando el repositorio sea público |
| `MINOR` (0.X.0) | Agregar módulos nuevos o el AKG con contenido sustancial | v0.3.0 → v0.4.0 al agregar los modelos americanos y el proceso de seed de DB |
| `PATCH` (0.0.X) | Correcciones, actualizaciones de documentos individuales, nuevas decisiones | v0.3.0 → v0.3.1 al agregar el runbook de rollback |

---

## Estado por Módulo

| Módulo | Estado | Completitud | Listo para producción |
|--------|--------|-------------|----------------------|
| `/constitution` | ✅ Completo | 100% | ✅ Sí |
| `/community` | 🟡 Templates listos | 50% (solo templates) | ✅ Sí (se llena con uso) |
| `/decisions` | 🟡 Fundacional | 30% (3 de ~10 decisiones) | ✅ Sí (se llena con uso) |
| `/design` | ✅ Completo | 90% | ✅ Sí |
| `/engineering/adr` | 🟡 En progreso | 40% (2 de ~5 ADRs) | 🟡 Parcial |
| `/engineering/architecture` | ⚠️ Referencia externa | 10% (solo README) | ❌ Falta subir el docx |
| `/engineering/database` | ⚠️ Referencia externa | 10% (solo README) | ❌ Falta subir el docx |
| `/engineering/runbooks` | ❌ Vacío | 5% (solo README) | ❌ Falta crear runbooks |
| `/engineering/security` | ❌ Vacío | 5% (solo README) | ❌ Falta threat model |
| `/engineering/api` | ❌ Vacío | 5% (solo README) | ❌ Falta contratos de API |
| `/founder-os` | ✅ Operacional | 70% | ✅ Sí |
| `/growth` | 🟡 En progreso | 30% (solo estructura) | 🟡 Parcial |
| `/legal` | ❌ Vacío | 5% (solo README) | ❌ Falta revisión legal |
| `/metrics` | ✅ Completo | 90% | ✅ Sí |
| `/product` | 🟡 En progreso | 30% | 🟡 Parcial |
| `/research/competitors` | ❌ Vacío | 5% | ❌ |
| `/research/market` | ❌ Vacío | 5% | ❌ |
| `/research/users` | ❌ Vacío | 5% | ❌ |
| `/research/vehicles` (AKG) | ✅ Fundación sólida | 70% | ✅ Sí |
| `/board` | 🟡 En progreso | 20% | 🟡 Parcial |
| `/brand` | 🟡 Referenciado | 20% | 🟡 Parcial |
| `/archive` | ✅ Listo | 100% (vacío = correcto) | ✅ Sí |

---

## Criterio de v1.0.0

El repositorio alcanza v1.0.0 cuando:

- [ ] Todos los runbooks críticos están escritos (deploy, rollback, supabase outage, DB restore)
- [ ] Los términos de servicio y política de privacidad están revisados y firmados
- [ ] El threat model de seguridad está completo
- [ ] El AKG cubre: BMW, VAG, Honda, Subaru, Mitsubishi, Americanos, Off-road (los 7 segmentos del PPS)
- [ ] Al menos 5 decisiones formales están documentadas en `/decisions`
- [ ] El repositorio ha pasado por revisión de un CTO o advisor técnico externo

---

## Dependencias Externas

| Documento | Ubicación externa | Pendiente de migrar |
|-----------|------------------|---------------------|
| SYSTEM_ARCHITECTURE_v1.0 | .docx en OneDrive/Drive | Sí → `engineering/architecture/` |
| DATABASE_BIBLE_v1.0 | .docx en OneDrive/Drive | Sí → `engineering/database/` |
| PPS (Product Specification) v1.0 | .docx en OneDrive/Drive | Sí → `product/specs/` |
| CTO Design Review | .docx en OneDrive/Drive | Sí → `board/decks/` |
| MVP Launch Plan | .docx en OneDrive/Drive | Sí → `product/roadmap/` |
| Documento Maestro Oficial | .docx en OneDrive/Drive | Sí → `board/decks/` |

> **Acción requerida:** Migrar estos documentos al repositorio en formato Markdown para que sean versionables, buscables, y enlazables.

---

*Mantenido por: Santiago Tarazona (Fundador/CTO) · PITS MARKET*
