# Changelog — PITS MARKET

Todos los cambios notables de PITS MARKET se documentan en este archivo.

El formato sigue [Keep a Changelog](https://keepachangelog.com/es/1.0.0/) y el proyecto adhiere a [Semantic Versioning](https://semver.org/lang/es/).

---

## [Unreleased]

### En desarrollo
- MVP: Formulario de publicación de piezas
- MVP: Grid de marketplace con filtros básicos
- MVP: Detalle de pieza con contacto por WhatsApp
- MVP: Registro y autenticación con Supabase Auth
- MVP: Panel de administración básico

---

## [0.1.0-mvp] — 2026-07-25 (Target)

### Added
- **F1 — Publicar una pieza:** Formulario de 1 página con subida de hasta 4 fotos
- **F2 — Encontrar una pieza:** Grid con filtros de categoría, ciudad y precio. Búsqueda full-text con PostgreSQL
- **F3 — Ver el detalle:** Galería de fotos, datos técnicos, botón de contacto por WhatsApp
- **F4 — Registro y login:** Autenticación con email/password via Supabase Auth
- **F5 — Panel de admin:** Aprobación/rechazo de avisos, lista de usuarios, KPIs básicos
- Emails transaccionales: bienvenida, aviso aprobado, aviso rechazado (via Resend)
- Meta tags Open Graph dinámicos para compartir avisos en redes sociales
- Sitemap.xml dinámico para SEO
- Integración con Cloudflare para CDN y protección básica

### Infrastructure
- Proyecto en Supabase Pro configurado (PostgreSQL, Auth, Storage, RLS)
- Deploy en Vercel con CI/CD desde GitHub
- Dominio pitsmarket.co con HTTPS
- 6 tablas de base de datos: profiles, listings, listing_images, listing_views, admin_actions, email_log
- 5 triggers: updated_at, create_profile, search_vector, generate_slug, increment_view_count
- 4 API Routes: /api/images/upload-url, /api/contact-click, /api/send-email, /api/og-image/[slug]

---

## [0.0.1] — 2026-06-26

### Added
- Repositorio `pits-core` creado en GitHub
- Estructura completa de carpetas de la organización
- Documentos fundacionales:
  - Documento Maestro Oficial v1.0
  - System Architecture v1.0
  - Database Bible v1.0
  - CTO Design Review (Board Task #004)
  - MVP Launch Plan (Board Task #008)
- README.md, CONTRIBUTING.md, LICENSE, .gitignore
- CODE_OF_CONDUCT.md, SECURITY.md
- Templates de Issues y Pull Requests
- GitHub Labels configurados

---

## Formato de Versiones

| Tipo | Formato | Ejemplo |
|------|---------|---------|
| MVP en desarrollo | `0.x.x-mvp` | `0.1.0-mvp` |
| Beta con monetización | `0.9.x-beta` | `0.9.0-beta` |
| V1 — Producto completo | `1.0.0` | `1.0.0` |
| V2 — Mensajería + App | `2.0.0` | `2.0.0` |
| Parches de seguridad | `x.x.PATCH` | `1.0.1` |

---

## Links

- [Repositorio](https://github.com/pitsmarket/pits-core)
- [Issues](https://github.com/pitsmarket/pits-core/issues)
- [MVP Launch Plan](product/roadmap/mvp-launch-plan-v1.md)

---

## [0.0.2] — 2026-06-26

### Added — Módulos v2 de PITS CORE

**`/constitution`** — La constitución de la empresa
- `principles.md` — 7 principios operacionales no negociables
- `values.md` — Valores del carácter de la empresa con ejemplos de lo que NO somos
- `philosophy.md` — Filosofía de producto, negocio y comunidad
- `decision-doctrine.md` — Cómo se toman decisiones en todos los niveles

**`/community`** — Voz de la comunidad
- Subcarpetas: `interviews/`, `feedback/`, `screenshots/`, `testimonials/`, `ideas/`
- Template de entrevista con estructura completa (alias, perfil, citas, implicaciones)
- Template de testimonial con métricas de impacto y consentimiento
- Sistema de captura de ideas con estados y categorías

**`/metrics`** — Sistema de métricas
- `north-star.md` — North Star Metric: transacciones completadas por semana, con targets por fase
- `dashboards/` — Template de Weekly Dashboard con 5 secciones y métricas específicas
- `kpis/` — 4 documentos de KPIs: producto, growth, ingeniería y negocio con fórmulas y targets

**`/design`** — Sistema de diseño
- `system/` — Design tokens: espaciado, border radius, sombras, breakpoints, animaciones
- `colors/` — Paleta completa con tabla de contraste WCAG y reglas de uso
- `typography/` — Escala tipográfica completa, fuentes oficiales, jerarquía por componente
- `icons/` — Mapa de Lucide Icons por contexto con 40+ íconos documentados
- `components/` — Template y lista de componentes del MVP
- `trust-ui/` — 6 componentes especializados de confianza: Seller Trust Card, Condition Badge, Price Trust Signal, Verification Badges, Safety Alert, Transaction Confirmation

**`/decisions`** — Sistema de registro de decisiones
- `TEMPLATE-decision.md` — Template con opciones evaluadas, trade-offs y criterios de revisión
- `0001-paid-listings.md` — Listings gratuitos en MVP, planes de pago en Beta
- `0002-pits-trust.md` — Sistema de reputación en 4 dimensiones como diferencial core
- `0003-whatsapp-strategy.md` — WhatsApp en MVP, mensajería interna en V2

### Changed
- `README.md` — Sección de módulos adicionales v2 agregada

