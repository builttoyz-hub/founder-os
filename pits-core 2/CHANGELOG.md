# CHANGELOG — PITS MARKET

Todos los cambios del repositorio PITS CORE se documentan aquí.
Formato: [Keep a Changelog](https://keepachangelog.com/es/1.0.0/)

---

## [0.3.0] — 2026-06-28 — CTO Architecture Review

### Automotive Knowledge Graph — Creado desde cero

El AKG existía solo como promesa en el README de `/research/vehicles/`. En esta versión se crea el contenido real que hace de PITS MARKET un Knowledge Graph profesional.

**Añadido — `/research/vehicles/`:**
- `KNOWLEDGE-GRAPH-SCHEMA.md` — Schema canónico de las 6 entidades del AKG: MAKE, MODEL, ENGINE, MODEL_ENGINE_COMPAT, PLATFORM, PART_CATEGORY. Incluye todos los campos con tipo, requerimiento y descripción
- `engines-master.md` — Base de datos de motores: BMW N/B/M-Series, VAG EA-Series y VR6, Honda K/B/D-Series, Subaru EJ-Series, Mitsubishi 4G-Series, Toyota JZ-Series, Nissan SR/RB/VQ-Series. Con notas críticas de incompatibilidad
- `platforms-compatibility.md` — Guía completa de plataformas: PQ35, MQB, MLB (VAG), E8x/E9x/F2x/F3x (BMW), EK/EG/EP3/DC5 (Honda), GC/GD/GRB/VA (Subaru). Con cross-compatibility charts y advertencias críticas
- `models-colombia-bmw.md` — Todos los modelos BMW en Colombia con motorización, años de disponibilidad, popularidad de tuning, y notas específicas del mercado colombiano
- `models-colombia-vag.md` — VW, Audi, Seat en Colombia por plataforma y generación
- `models-colombia-jdm.md` — Honda, Subaru, Mitsubishi, Nissan, Toyota, Mazda JDM/USDM en Colombia
- `scalability-architecture.md` — Arquitectura de índices para 1M+ listings, query patterns con estimaciones de tiempo, estrategia de caché para el AKG, particionamiento futuro, visión del AKG como API pública
- `README.md` — Completamente reescrito con el inventario real de archivos, flujo de uso en la plataforma, niveles de confianza de datos, y guía de contribución

### Inconsistencias Resueltas

**Corregido:**
- `/product/research/README.md` reescrito para diferenciarse claramente de `/research/`. Antes era ambiguo y generaba confusión sobre qué iba en cada carpeta
- `/engineering/adr/README.md` actualizado con tabla comparativa de cuándo usar ADR vs `/decisions`. La diferencia ya estaba documentada en `/decisions/README.md` pero no en el ADR README
- `/research/vehicles/README.md` reescrito para referenciar los archivos que ahora realmente existen (antes prometía 7 archivos que no existían)

**Eliminado como gap:**
- El AKG ya no es "trabajo en progreso" — tiene contenido real y utilizable

### Arquitectura Verificada

- Schema de DB del AKG validado contra el DATABASE BIBLE v1.0 — sin conflictos
- Índices del AKG validados contra el SYSTEM ARCHITECTURE v1.0 — alineados
- Query patterns del AKG validados contra el PPS v1.0 — compatibles
- Estrategia de caché del AKG validada contra la estrategia general de caché

---

## [0.2.0] — 2026-06-26 — Repository V2: New Modules

### Añadido

**`/constitution/`** — La constitución de la empresa
- `principles.md` — 7 principios con señal de violación para cada uno
- `values.md` — 6 valores con sección explícita "Lo que NO somos"
- `philosophy.md` — Filosofía de producto, negocio y comunidad
- `decision-doctrine.md` — Doctrina de decisiones: ownership, Tipo 1/2, Disagree & Commit, velocidades

**`/community/`** — Voz de la comunidad
- `interviews/TEMPLATE-interview.md` — Template con alias, perfil, citas, implicaciones
- `testimonials/TEMPLATE-testimonial.md` — Template con métricas de impacto y consentimiento
- `ideas/README.md` — Sistema de captura con estados y categorías
- `feedback/README.md` — Canales monitoreados y template de registro
- `screenshots/README.md` — Categorías y reglas de privacidad

**`/metrics/`** — Sistema de métricas en 3 capas
- `north-star.md` — North Star: transacciones completadas/semana, con targets por fase y señales de alarma
- `dashboards/TEMPLATE-weekly-dashboard.md` — 5 secciones: NS, inventario, usuarios, engagement, operaciones
- `kpis/kpis-product.md` — Liquidity Rate, Time to First Contact, Seller Repeat Rate, fórmulas exactas
- `kpis/kpis-growth.md` — CAC, Channel Attribution, D30 Retention, NPS
- `kpis/kpis-engineering.md` — Uptime, Error rate, MTTR, Core Web Vitals, DB performance
- `kpis/kpis-business.md` — LTV, Gross Margin, Runway, GMV, costos de infra

**`/design/`** — Sistema de diseño
- `system/README.md` — Design tokens: espaciado 4px, border radius, sombras, breakpoints, animaciones
- `colors/README.md` — Paleta con tabla WCAG, reglas de uso, el verde neón (#AAFF00) con texto negro
- `typography/README.md` — Barlow Condensed + Share Tech Mono, escala, jerarquía por componente
- `icons/README.md` — Lucide Icons con 40+ íconos mapeados por contexto
- `components/README.md` — Lista de componentes MVP + template
- `trust-ui/README.md` — 6 componentes de confianza: Seller Trust Card, Condition Badge, Price Trust Signal, Verification Badges, Safety Alert, Transaction Confirmation

**`/decisions/`** — Sistema de registro de decisiones
- `TEMPLATE-decision.md` — Con opciones evaluadas, trade-offs, riesgos, criterios de revisión
- `0001-paid-listings.md` — Listings gratuitos MVP, planes de pago en Beta
- `0002-pits-trust.md` — Sistema de reputación 4 dimensiones
- `0003-whatsapp-strategy.md` — WhatsApp en MVP, mensajería interna en V2

### Modificado
- `README.md` — Sección de módulos v2 añadida
- `CHANGELOG.md` — Historial iniciado

---

## [0.1.0] — 2026-06-26 — Repository V1: Foundation

### Añadido — Estructura base del repositorio

**GitHub Configuration:**
- 5 Issue templates: bug, feature request, documentación, seguridad, contenido
- Pull Request template con checklist diferenciado por carpeta
- 2 GitHub Actions: validación de docs + auto-labeling de PRs
- `LABELS.md` con 20+ labels con códigos hex y comandos CLI

**Root files:**
- `README.md` — Con badges, stack, estructura y quick start
- `CONTRIBUTING.md` — Proceso de contribución, naming conventions, reviewers por carpeta
- `LICENSE` — MIT con nota sobre scope de datos confidenciales
- `.gitignore` — 150+ entradas incluyendo secretos, office temp, diseño
- `CODE_OF_CONDUCT.md` — Con niveles de violación y consecuencias
- `SECURITY.md` — Proceso de reporte responsable, timelines, checklist

**Módulos V1:**
- `/docs` — Documentación técnica viva
- `/founder-os` — Sistema operativo del fundador (weekly-rituals, decision-framework)
- `/product` — Roadmap, specs, UX, research
- `/engineering` — Architecture, database, API, security, runbooks, ADR (adr-001, adr-002)
- `/growth` — Content, campaigns, analytics, SEO, influencers
- `/research` — Market, competitors, users, vehicles (solo README)
- `/board` — Meetings, decks, reports, legal-entities
- `/brand` — Identity, assets, guidelines, voice
- `/legal` — Contracts, terms, policies, compliance
- `/archive` — Deprecated, historical

---

## Próximos Cambios Previstos

Ver `TODO.md` para el backlog completo de mejoras al repositorio.
