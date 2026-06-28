# KPIs de Negocio — PITS MARKET

*Revisión: Mensual (Board report) · Propietario: Fundador*

---

## Unit Economics

### LTV (Lifetime Value) — Vendedor Pro
**Definición:** Revenue total generado por un vendedor Pro durante toda su relación con PITS MARKET.
**Fórmula:** ARPU mensual × Duración promedio de suscripción en meses
**Target V1:** > $200,000 COP
**Nota:** En MVP no hay planes de pago. Este KPI se activa en Beta.

---

### Gross Margin
**Definición:** (Revenue - Costos directos variables) / Revenue × 100
**Costos directos en PITS MARKET:** Storage egress, email transaccional, SMS OTP
**Target V1:** > 85% (software tiene márgenes altos cuando el producto escala)
**Nota:** La infra fija (Supabase, Vercel) es costo fijo, no variable.

---

### Runway
**Definición:** Meses de operación disponibles con el cash actual al burn rate actual.
**Target:** Siempre > 12 meses (o raise antes de llegar a 12 meses)
**Fórmula:** Cash en banco / Burn rate mensual promedio de últimos 3 meses

---

## Métricas de Escala del Marketplace

| Métrica | MVP Target | Beta Target | V1 Target |
|---------|-----------|------------|-----------|
| GMV semanal (valor de piezas transaccionadas) | No medible (sin datos) | $50M COP/mes | $200M COP/mes |
| Listings activos | 50 | 500 | 5,000 |
| Vendedores activos (≥1 listing) | 30 | 200 | 1,500 |
| Compradores activos (≥1 contacto/mes) | 50 | 400 | 3,000 |
| Ciudades con ≥10 listings | 2 | 5 | 15 |

---

## Gestión del Costo

| Costo | Actual | Target MVP | Responsable |
|-------|--------|-----------|-------------|
| Supabase | $25 USD/mes | < $40 USD | CTO |
| Vercel | $20 USD/mes | < $30 USD | CTO |
| Resend | $0 (free tier) | < $20 USD | CTO |
| Dominio | $3 USD/mes | Fijo | Admin |
| Cloudflare | $0 (free) | < $20 USD | CTO |
| **Total infra** | **~$48 USD/mes** | **< $110 USD/mes** | CTO |

---

*Versión 1.0 — Junio 2026*
