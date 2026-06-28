# TODO — PITS CORE

> Lista de mejoras pendientes al repositorio. Organizadas por prioridad y área.
> Este no es el backlog del producto (ese está en `/product/roadmap/`). Es el backlog del repositorio mismo.

---

## 🔴 Prioridad Alta — Antes del lanzamiento MVP

### Knowledge Graph
- [ ] `research/vehicles/models-colombia-americanos.md` — Ford Mustang, Chevrolet Camaro, Camaro SS, Dodge Challenger, Dodge Charger, Jeep Wrangler
- [ ] `research/vehicles/models-colombia-koreans.md` — Hyundai Elantra N, Hyundai i30 N, Kia Stinger, Kia Ceed
- [ ] `research/vehicles/models-colombia-masivos.md` — Toyota Corolla (todas las gen), Mazda 3/6, Honda Civic (no-performance, la que se vende masivamente), Chevrolet Cruze. El mercado de tuning entry-level colombiano
- [ ] `research/vehicles/models-colombia-offroad.md` — Toyota Land Cruiser Prado, Land Rover Defender, Jeep Wrangler JK/JL, Ford Ranger, Toyota Hilux
- [ ] Validar los datos del AKG con al menos 3 expertos técnicos de la comunidad tuning colombiana
- [ ] Crear el proceso de PR para contribuciones al AKG desde la comunidad

### Engineering
- [ ] `engineering/architecture/SYSTEM_ARCHITECTURE_v1.md` — Subir el documento de arquitectura al repositorio (actualmente existe solo como .docx)
- [ ] `engineering/database/DATABASE_BIBLE_v1.md` — Subir el documento al repositorio
- [ ] `engineering/runbooks/runbook-deploy-production.md` — Runbook de deployment en producción
- [ ] `engineering/runbooks/runbook-rollback.md` — Runbook de rollback en Vercel
- [ ] `engineering/runbooks/runbook-supabase-outage.md` — Qué hacer si Supabase está caído
- [ ] `engineering/runbooks/runbook-add-admin-user.md` — Cómo activar la cuenta admin

### Product
- [ ] `product/roadmap/roadmap-mvp-v1.md` — Subir el MVP Launch Plan al repositorio
- [ ] `product/specs/spec-publish-listing-v1.md` — Spec del formulario de publicación
- [ ] `product/specs/spec-marketplace-search-v1.md` — Spec de búsqueda y filtros
- [ ] `product/specs/spec-listing-detail-v1.md` — Spec del detalle de pieza
- [ ] `product/specs/spec-auth-registration-v1.md` — Spec de registro y login
- [ ] `product/specs/spec-admin-panel-v1.md` — Spec del panel de admin

---

## 🟡 Prioridad Media — Post-lanzamiento MVP

### Decisions
- [ ] `decisions/0004-colombia-first-no-latam-expansion-in-mvp.md` — Documentar decisión de Colombia primero
- [ ] `decisions/0005-no-commission-model.md` — Por qué no hay comisión vs modelos de comisión
- [ ] `decisions/0006-supabase-pricing-strategy.md` — Cómo gestionar costos de Supabase conforme crece

### Engineering
- [ ] `engineering/security/security-threat-model-v1.md` — Modelo de amenazas completo
- [ ] `engineering/security/security-checklist-launch.md` — Checklist pre-lanzamiento
- [ ] `engineering/api/api-contract-listings-v1.md` — Contrato de la API de listings
- [ ] `engineering/api/api-contract-images-v1.md` — Contrato de upload de imágenes
- [ ] `engineering/adr/adr-003-postgresql-price-in-pesos-not-centavos.md` — Decisión de usar pesos enteros en lugar de centavos
- [ ] `engineering/adr/adr-004-whatsapp-external-contact.md` — Decisión técnica del contacto por WhatsApp

### Community
- [ ] Primera entrevista real de usuario (vendedor) documentada y anonimizada
- [ ] Primer screenshot de frustración del mercado actual (grupo de Facebook) documentado
- [ ] Primera idea de la comunidad registrada

### Metrics
- [ ] `metrics/dashboards/2026-W30-weekly-dashboard.md` — Primer dashboard real post-lanzamiento
- [ ] `metrics/growth/cohort-analysis-template.md` — Template de análisis de cohortes

---

## 🟢 Prioridad Baja — Versión Beta en adelante

### Knowledge Graph (expansión)
- [ ] `research/vehicles/engines-master-diesel.md` — Motores diesel relevantes en Colombia (BMW N47, VW TDI, Mercedes OM-series)
- [ ] `research/vehicles/models-colombia-muscle.md` — Dodge Challenger SRT, Ford Mustang Shelby
- [ ] Integración del AKG con la base de datos de producción (script de seed inicial)
- [ ] API pública del AKG documentada para terceros

### Brand
- [ ] `brand/identity/logo-original.fig` — Archivo Figma del logo
- [ ] `brand/assets/logo-pitsmarket-transparente.png` — Export PNG con transparencia
- [ ] `brand/assets/logo-pitsmarket-glow.png` — Export PNG con glow verde
- [ ] `brand/guidelines/brand-guidelines-v1.md` — Manual de marca completo

### Legal
- [ ] `legal/terms/terms-of-service-v1.md` — Términos de servicio (revisado por abogado)
- [ ] `legal/terms/privacy-policy-v1.md` — Política de privacidad (Ley 1581)
- [ ] `legal/policies/policy-content-moderation-v1.md` — Política de moderación
- [ ] `legal/policies/policy-prohibited-items-v1.md` — Lista de ítems prohibidos
- [ ] `legal/compliance/compliance-ley-1581-rnbd.md` — Registro en SIC

### Growth
- [ ] `growth/content/strategy-content-q3-2026.md` — Estrategia de contenido post-lanzamiento
- [ ] `growth/seo/strategy-seo-colombia-2026.md` — Keywords y estructura SEO

---

## ✅ Completado

- [x] Estructura base del repositorio (v1.0)
- [x] Módulos: constitution, community, metrics, design, decisions (v2.0)
- [x] Automotive Knowledge Graph — Schema, engines, plataformas, modelos (v0.3.0)
- [x] Scalability architecture para el AKG (v0.3.0)
- [x] Inconsistencias de naming resueltas (v0.3.0)
- [x] Ambigüedad entre ADR y decisions resuelta (v0.3.0)
- [x] Ambigüedad entre product/research y research resueltas (v0.3.0)
- [x] CHANGELOG.md, TODO.md, VERSION.md creados (v0.3.0)

---

*Actualizar este archivo cada vez que se completa un item o se identifica un nuevo gap.*
*Owner: Fundador + CTO*
