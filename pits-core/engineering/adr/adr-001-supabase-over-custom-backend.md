# ADR-001: Supabase sobre Backend Custom en Node.js

**Estado:** Accepted
**Fecha:** 2026-06-26
**Autores:** Santiago Tarazona (CTO interim)
**Revisores:** ATLAS (CTO Advisor)

---

## Contexto

En la etapa de diseño de la arquitectura del MVP de PITS MARKET, se evaluó qué plataforma de backend usar. Las opciones eran construir un backend custom en Node.js/Express o FastAPI, o usar un Backend-as-a-Service (BaaS) como Supabase o Firebase.

**Restricciones existentes:**
- Timeline de 30 días para el MVP
- Equipo de 1 desarrollador (el fundador)
- Sin presupuesto inicial para infraestructura compleja
- Necesidad de autenticación, base de datos relacional, storage de archivos y real-time

---

## Decisión

Usar **Supabase** como la plataforma de backend principal del MVP y las versiones tempranas del producto.

Supabase provee: PostgreSQL 15+, autenticación con JWT y OAuth, storage de archivos con CDN, WebSockets para real-time, y Edge Functions (Deno) para lógica serverless — todo en un mismo servicio.

---

## Alternativas Consideradas

### Alternativa A: Backend custom Node.js + Express + PostgreSQL en Railway/Render

**Pros:**
- Control total sobre cada aspecto del backend
- Sin vendor lock-in
- Más barato a muy alta escala

**Contras:**
- Semanas de setup antes de la primera funcionalidad
- Autenticación segura requiere meses de trabajo bien hecho
- Storage con CDN requiere integración adicional (S3 + CloudFront)
- Real-time requiere Socket.io o similar

### Alternativa B: Firebase (Google)

**Pros:**
- BaaS maduro con gran adopción
- Firestore tiene buen real-time

**Contras:**
- Firestore es NoSQL — para un marketplace con relaciones complejas (listings, users, reviews, compatibility), el modelo relacional de PostgreSQL es claramente superior
- Vendor lock-in más severo que Supabase (Firestore es propietario de Google)
- Consultas complejas son más difíciles sin SQL nativo

### Alternativa C: PocketBase (self-hosted)

**Pros:**
- Open source, sin vendor lock-in
- Self-hosted = costo predecible

**Contras:**
- Requiere servidor propio y gestión de infraestructura
- Comunidad y ecosistema más pequeño
- Sin CDN de storage integrado

---

## Consecuencias

### Positivas
- El MVP puede construirse en 30 días con 1 desarrollador
- PostgreSQL con RLS provee seguridad a nivel de fila sin código adicional
- Auth integrado elimina uno de los componentes más complejos de construir
- Storage con CDN resuelve el problema de imágenes sin integración adicional
- Real-time nativo permite features como notificaciones sin infraestructura adicional

### Negativas / Trade-offs
- Vendor lock-in real: Auth, Storage, y Realtime están acoplados a Supabase
- Las Edge Functions usan Deno (no Node.js) — algunas librerías de npm no están disponibles
- El plan Pro de Supabase ($25/mes) tiene límites de egress y conexiones que requieren monitoreo
- Migrar a otra plataforma en el futuro requeriría meses de trabajo

### Mitigaciones del lock-in
- El cliente de Supabase se usa siempre detrás de una capa de servicios (`supabase/services/`), nunca directamente en componentes UI
- La base de datos usa PostgreSQL estándar — migrar solo la DB a otro hosting es posible
- Los datos se pueden exportar en cualquier momento con `pg_dump`

### Riesgos
- **Riesgo:** Supabase alcanza límites del plan Pro antes de poder migrar
  - **Mitigación:** Monitorear métricas semanalmente. Plan de migración a Enterprise documentado en runbooks cuando llegue a 20K MAU
- **Riesgo:** Precio de Supabase sube significativamente
  - **Mitigación:** PostgreSQL estándar hace que la migración a otro PG hosting sea viable en 1-2 semanas

---

## Referencias

- [System Architecture v1](../architecture/SYSTEM_ARCHITECTURE_v1.md) — Sección 07: Problemas con Supabase
- [CTO Design Review](../../board/decks/) — Sección 7: Honestidad brutal sobre Supabase
- [Supabase Pricing](https://supabase.com/pricing)

---

*ADR-001 · Accepted · 2026-06-26*
