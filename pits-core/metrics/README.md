# /metrics — Sistema de Métricas de PITS MARKET

## Propósito

La fuente de verdad del desempeño de PITS MARKET. No solo qué números miramos, sino **por qué miramos esos números**, qué significan, cómo se calculan, y qué acciones generan.

> **Principio:** Las métricas que no llevan a decisiones son ruido. Cada número en este sistema existe porque conecta con una acción que puede mejorar el producto o el negocio.

---

## Estructura del Sistema de Métricas

```
metrics/
├── README.md                    ← Este archivo — el mapa del sistema
├── north-star.md                ← La métrica única que define el éxito
├── dashboards/                  ← Dashboard semanal operacional
│   ├── README.md
│   ├── TEMPLATE-weekly-dashboard.md
│   └── [YYYY-WW]-weekly-dashboard.md  ← Una por semana
├── kpis/                        ← KPIs por área del negocio
│   ├── README.md
│   ├── kpis-product.md
│   ├── kpis-growth.md
│   ├── kpis-engineering.md
│   └── kpis-business.md
└── growth/                      ← Análisis de crecimiento profundo
    ├── README.md
    ├── cohort-analysis-template.md
    └── funnel-analysis-template.md
```

---

## El Sistema en Tres Capas

### Capa 1 — North Star (semanal, 1 número)
Un solo número que resume si la empresa está yendo en la dirección correcta. Esta semana vs la semana pasada. No hay discusión sobre el estado del negocio sin conocer este número.

**→ Ver `north-star.md`**

### Capa 2 — Weekly Dashboard (semanal, ~15 métricas)
El dashboard operacional que el equipo revisa cada lunes. 15 métricas organizadas por área que explican el movimiento de la North Star.

**→ Ver `dashboards/`**

### Capa 3 — KPIs por Área (mensual, análisis profundo)
El análisis profundo por área de negocio. Se revisa mensualmente en el Board report. No se mira semana a semana porque tiene demasiado ruido.

**→ Ver `kpis/`**

---

## Lo que NO Es Este Sistema

- No es un dashboard de vanity metrics ("mira cuántos followers tenemos")
- No reemplaza el análisis cualitativo — los números explican el **qué**, los usuarios explican el **por qué**
- No es estático — las métricas cambian cuando el negocio cambia de fase (MVP vs Beta vs V1)

---

*Propietario: Fundador · Revisión: Semanal (dashboard) / Mensual (KPIs)*
