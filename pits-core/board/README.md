# /board — Nivel Directivo

## Propósito

Esta carpeta contiene los documentos de nivel Board de PITS MARKET: minutas de reuniones, presentaciones para inversionistas, reportes de desempeño de la empresa, y documentos de constitución legal de la entidad.

> **Acceso:** Esta carpeta es de acceso restringido. Solo el Fundador y directores designados tienen permisos de escritura. Los documentos aquí son de naturaleza confidencial.

---

## Subcarpetas

### `/meetings` — Minutas y agendas de reuniones
Registro de cada reunión de nivel directivo: agenda previa, decisiones tomadas, acciones comprometidas y responsables.

### `/decks` — Presentaciones para inversionistas y socios estratégicos
Pitch decks, investor updates, presentaciones de partnership. Los documentos que representan a PITS MARKET ante audiencias externas.

### `/reports` — Reportes de desempeño
Reportes mensuales y trimestrales de métricas de negocio: revenue, usuarios, transacciones, costos, y proyecciones.

### `/legal-entities` — Documentos de constitución
Actas de constitución de la empresa, estatutos, estructura de capital, y documentos regulatorios fundamentales de la entidad legal.

---

## Convención de Nombres

```
meetings/    → [fecha]-meeting-[tipo]-agenda.md
              → [fecha]-meeting-[tipo]-minutes.md

decks/       → [fecha]-deck-[audiencia]-v[N].md
              → [año]-investor-update-[mes].md

reports/     → report-monthly-[YYYY-MM].md
              → report-quarterly-[YYYY-Q#].md

legal-entities/ → [tipo-documento]-[entidad]-[fecha].md

Ejemplos:
  meetings/2026-07-25-meeting-weekly-minutes.md
  decks/2026-07-pitch-seed-investors-v3.md
  decks/2026-08-investor-update-monthly.md
  reports/report-monthly-2026-08.md
  reports/report-quarterly-2026-q3.md
  legal-entities/acta-constitucion-sas-2026.md
```

---

## Template de Reporte Mensual

```markdown
# Reporte Mensual — [Mes YYYY]

**Período:** [Fecha inicio] – [Fecha fin]
**Preparado por:** Santiago Tarazona
**Distribución:** [Quiénes reciben este reporte]

## Resumen Ejecutivo
Dos párrafos: qué pasó y qué significa.

## Métricas Clave

| Métrica | Este mes | Mes anterior | Δ |
|---------|----------|--------------|---|
| MAU | | | |
| Listings activos | | | |
| Nuevos usuarios | | | |
| MRR | | | |
| Contactos WhatsApp | | | |

## Hitos Alcanzados
- [Hito 1]

## Retos y Blockers
- [Reto 1] → Plan de acción: [...]

## Próximas 4 Semanas
- [Prioridad 1]

## Proyecciones
[Proyección para el próximo mes/trimestre]
```

---

*Propietario: Fundador — Acceso restringido*
