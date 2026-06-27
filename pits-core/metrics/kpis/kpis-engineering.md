# KPIs de Ingeniería — PITS MARKET

*Revisión: Mensual · Propietario: CTO*

---

## Confiabilidad

| KPI | Definición | Target | Alerta si |
|-----|------------|--------|-----------|
| Uptime mensual | % del tiempo que pitsmarket.co está disponible | > 99.9% | < 99.5% |
| Error rate (5xx) | % de requests que retornan error 5xx | < 0.1% | > 0.5% |
| MTTR (Mean Time to Recover) | Tiempo promedio para resolver un incidente crítico | < 1 hora | > 2 horas |
| MTTD (Mean Time to Detect) | Tiempo promedio para detectar un incidente | < 5 min | > 15 min |

---

## Performance

| KPI | Definición | Target | Medido en |
|-----|------------|--------|-----------|
| LCP (Largest Contentful Paint) | Tiempo hasta que el contenido principal es visible | < 2.5s | Lighthouse / Vercel |
| FID (First Input Delay) | Tiempo de respuesta al primer input del usuario | < 100ms | Lighthouse |
| CLS (Cumulative Layout Shift) | Estabilidad visual de la página | < 0.1 | Lighthouse |
| P50 API response time | Latencia mediana de API Routes | < 200ms | Vercel Analytics |
| P99 API response time | Latencia en el percentil 99 | < 1000ms | Vercel Analytics |
| DB query P50 | Tiempo de query mediano en Supabase | < 50ms | Supabase Dashboard |

---

## Calidad de Código

| KPI | Definición | Target |
|-----|------------|--------|
| Deploy frequency | Cuántas veces se hace deploy a producción por semana | ≥ 3/semana |
| Lead time for changes | Desde commit hasta producción | < 1 hora |
| Change failure rate | % de deploys que requieren rollback | < 5% |
| Code coverage (cuando aplique) | % de código con tests | > 70% |

---

## Infraestructura

| KPI | Definición | Target | Alerta si |
|-----|------------|--------|-----------|
| Supabase Storage usado | GB usados / GB incluidos | < 80% | > 85% |
| DB connection pool | Conexiones usadas / disponibles | < 70% | > 85% |
| Costo mensual de infra | Total en USD | < $150 (MVP) | > $200 (MVP) |
| Backup verification | Último backup verificado funcional | < 7 días | > 14 días |

---

*Versión 1.0 — Junio 2026*
