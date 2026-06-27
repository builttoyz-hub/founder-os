<div align="center">

```
██████╗ ██╗████████╗███████╗    ███╗   ███╗ █████╗ ██████╗ ██╗  ██╗███████╗████████╗
██╔══██╗██║╚══██╔══╝██╔════╝    ████╗ ████║██╔══██╗██╔══██╗██║ ██╔╝██╔════╝╚══██╔══╝
██████╔╝██║   ██║   ███████╗    ██╔████╔██║███████║██████╔╝█████╔╝ █████╗     ██║
██╔═══╝ ██║   ██║   ╚════██║    ██║╚██╔╝██║██╔══██║██╔══██╗██╔═██╗ ██╔══╝     ██║
██║     ██║   ██║   ███████║    ██║ ╚═╝ ██║██║  ██║██║  ██║██║  ██╗███████╗   ██║
╚═╝     ╚═╝   ╚═╝   ╚══════╝    ╚═╝     ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝   ╚═╝
```

**El Marketplace de la Comunidad Tuning Colombia**

[![Status](https://img.shields.io/badge/status-MVP%20Development-brightgreen?style=flat-square)](https://pitsmarket.co)
[![Version](https://img.shields.io/badge/version-0.1.0--mvp-blue?style=flat-square)](CHANGELOG.md)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](LICENSE)
[![Colombia](https://img.shields.io/badge/built%20in-Colombia%20🇨🇴-yellow?style=flat-square)](https://pitsmarket.co)

[pitsmarket.co](https://pitsmarket.co) · [Instagram @built\_toyz](https://instagram.com/built_toyz) · [builttoyz@gmail.com](mailto:builttoyz@gmail.com)

</div>

---

## ¿Qué es PITS MARKET?

PITS MARKET es el primer marketplace especializado de Colombia para la compra, venta e intercambio de piezas, accesorios y componentes automotrices entre entusiastas del tuning, mecánicos, importadores y talleres especializados.

No es un clasificado genérico. No es un grupo de Facebook. Es una plataforma construida específicamente para personas que saben lo que tienen, saben lo que buscan, y exigen un entorno donde el conocimiento técnico es el denominador común.

> **"Cansado de buscar turbos entre publicaciones de sofás usados."**

---

## Estado del Proyecto

| Fase | Estado | Timeline |
|------|--------|----------|
| MVP (5 features core) | 🟡 En desarrollo | Julio 2026 |
| Beta (monetización + reputación) | ⚪ Planeado | Sep–Nov 2026 |
| V1 (retención + PWA) | ⚪ Planeado | Dic 2026–Mar 2027 |
| V2 (mensajería + app nativa) | ⚪ Planeado | Abr–Sep 2027 |
| V3 (expansión LATAM) | ⚪ Planeado | 2027–2028 |

---

## Los 5 Features del MVP

1. **Publicar una pieza** — Formulario de 1 página. Menos de 3 minutos.
2. **Encontrar una pieza** — Grid + filtros básicos + búsqueda full-text.
3. **Ver el detalle** — Galería + datos técnicos + contacto directo por WhatsApp.
4. **Registro y Login** — Email/password. Sin fricción.
5. **Panel de Admin** — Aprobar, rechazar, ver métricas básicas.

---

## Stack Tecnológico

| Capa | Tecnología | Por qué |
|------|-----------|---------|
| Frontend | Next.js 14 + TypeScript + Tailwind CSS | SSR/ISR para SEO, App Router, DX óptimo |
| Backend / DB | Supabase (PostgreSQL 15+) | BaaS con RLS, Auth, Storage, Realtime integrados |
| Hosting | Vercel | Mejor compatibilidad con Next.js App Router, rollback instantáneo |
| CDN | Cloudflare | DDoS protection, cache global, WAF |
| Email | Resend | Transaccionales de alta entrega, API moderna |
| Monitoreo | Sentry + Uptime Robot | Error tracking + alertas de disponibilidad |
| Dominio | pitsmarket.co | .co de Colombia, relevante para el mercado |

---

## Estructura del Repositorio

```
pits-core/
├── .github/                    # GitHub configuration (templates, workflows)
│   ├── ISSUE_TEMPLATE/         # Templates para issues por tipo
│   └── workflows/              # GitHub Actions (CI/CD, checks)
├── docs/                       # Documentación técnica viva
├── founder-os/                 # Sistema operativo del fundador
├── product/                    # Definición del producto
│   ├── roadmap/                # Roadmap por versión
│   ├── specs/                  # Especificaciones funcionales
│   ├── ux/                     # Flujos y wireframes
│   └── research/               # Investigación de producto
├── engineering/                # Todo lo técnico
│   ├── architecture/           # Decisiones de arquitectura
│   ├── database/               # Schema, migraciones, políticas
│   ├── api/                    # Contratos de API
│   ├── security/               # Políticas y auditorías de seguridad
│   ├── runbooks/               # Procedimientos operacionales
│   └── adr/                    # Architecture Decision Records
├── growth/                     # Crecimiento y marketing
│   ├── content/                # Estrategia de contenido
│   ├── campaigns/              # Campañas activas y archivadas
│   ├── analytics/              # Métricas y reportes
│   ├── seo/                    # Estrategia SEO
│   └── influencers/            # Relaciones con influencers
├── research/                   # Investigación de mercado
│   ├── market/                 # Análisis del mercado colombiano
│   ├── competitors/            # Benchmarks de competidores
│   ├── users/                  # Entrevistas y user research
│   └── vehicles/               # Ontología automotriz colombiana
├── board/                      # Nivel directivo
│   ├── meetings/               # Minutas y agendas
│   ├── decks/                  # Presentaciones para inversionistas
│   ├── reports/                # Reportes mensuales/trimestrales
│   └── legal-entities/         # Documentos de constitución
├── brand/                      # Identidad de marca
│   ├── identity/               # Logos, colores, tipografía
│   ├── assets/                 # Archivos de diseño exportados
│   ├── guidelines/             # Manual de marca
│   └── voice/                  # Tono y voz de comunicación
├── legal/                      # Marco legal
│   ├── contracts/              # Contratos con proveedores y socios
│   ├── terms/                  # Términos de servicio y privacidad
│   ├── policies/               # Políticas internas
│   └── compliance/             # Cumplimiento regulatorio
└── archive/                    # Archivos históricos
    ├── deprecated/             # Documentos reemplazados
    └── historical/             # Versiones anteriores para referencia
```

---

## Quick Start para el Equipo

### Acceso al Repositorio
1. Solicitar acceso a [@builttoyz](https://github.com/builttoyz)
2. Clonar: `git clone https://github.com/pitsmarket/pits-core.git`
3. Leer [`CONTRIBUTING.md`](CONTRIBUTING.md) antes de hacer cualquier cambio
4. Leer el README de la carpeta con la que vas a trabajar

### Primera Contribución
1. Crear un branch: `git checkout -b docs/[nombre-documento]`
2. Hacer cambios siguiendo las convenciones de la carpeta correspondiente
3. Commit con mensaje descriptivo: `docs(engineering): add API contract v1`
4. Abrir Pull Request usando el template incluido
5. Esperar review del propietario de la carpeta

### Convención de Commits
```
tipo(scope): descripción breve en minúsculas

tipos: docs | feat | fix | refactor | chore | security
scopes: engineering | product | growth | board | brand | legal | research
```

---

## Documentos Clave

| Documento | Ubicación | Descripción |
|-----------|-----------|-------------|
| Documento Maestro Oficial | `board/decks/` | Visión, misión, modelo de negocio |
| System Architecture v1 | `engineering/architecture/` | Arquitectura técnica completa |
| Database Bible v1 | `engineering/database/` | Diseño de base de datos |
| CTO Design Review | `board/decks/` | Análisis estratégico técnico |
| MVP Launch Plan | `product/roadmap/` | Plan de 30 días al lanzamiento |

---

## Equipo

| Rol | Persona | Responsable de |
|-----|---------|----------------|
| CEO / Fundador | Santiago Tarazona | Visión, producto, comunidad |
| CTO | Santiago Tarazona (interim) | Arquitectura, infraestructura |
| Head of Content | Santiago Tarazona (interim) | @built_toyz, contenido |

> PITS MARKET está en etapa de fundador único. Este repositorio está preparado para escalar al equipo que vendrá.

---

## Contacto

- **Producto & negocio:** builttoyz@gmail.com
- **Seguridad:** ver [SECURITY.md](SECURITY.md)
- **Bugs y features:** abrir un [Issue](https://github.com/pitsmarket/pits-core/issues/new/choose)

---

<div align="center">
  <sub>© 2026 PITS MARKET · Medellín, Colombia 🇨🇴 · Construido desde adentro de la comunidad.</sub>
</div>

---

## Módulos Adicionales (v2)

| Módulo | Descripción |
|--------|-------------|
| [`/constitution`](constitution/) | Principios, valores, filosofía y doctrina de decisiones |
| [`/community`](community/) | Voz de la comunidad: entrevistas, feedback, testimoniales, ideas |
| [`/metrics`](metrics/) | North Star, dashboards semanales, KPIs por área |
| [`/design`](design/) | Design system, componentes, colores, tipografía, trust UI |
| [`/decisions`](decisions/) | Registro de decisiones estratégicas de la empresa |

