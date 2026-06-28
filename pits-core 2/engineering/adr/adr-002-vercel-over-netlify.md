# ADR-002: Vercel sobre Netlify para Hosting de Next.js

**Estado:** Accepted
**Fecha:** 2026-06-26
**Autores:** Santiago Tarazona (CTO interim)
**Revisores:** ATLAS (CTO Advisor)

---

## Contexto

El diseño inicial del sistema contemplaba Netlify como plataforma de hosting para la aplicación Next.js. Después del CTO Design Review (Board Task #004), se identificaron problemas específicos con Netlify para proyectos Next.js 14 con App Router.

---

## Decisión

Usar **Vercel** en lugar de Netlify como plataforma de hosting y deployment para la aplicación Next.js de PITS MARKET.

---

## Alternativas Consideradas

### Alternativa A: Netlify (opción original)

**Pros:**
- Precio ligeramente menor ($19/mes Pro vs $20/mes Pro de Vercel)
- Buena DX general

**Contras:**
- Soporte de Next.js App Router features nuevas (Server Actions, RSC) no es de primera clase
- Modelo de pricing por invocaciones de funciones se vuelve costoso a 50K+ MAU
- Cold starts de 200–800ms en Functions
- Rollback requiere más pasos que en Vercel

### Alternativa B: Railway / Render (self-hosted Next.js)

**Pros:**
- Más control sobre el entorno de ejecución
- Pricing más predecible (por hora de CPU/RAM)

**Contras:**
- Requiere configurar y mantener el servidor de Next.js
- Sin CDN edge nativo
- Sin preview deployments automáticos

---

## Consecuencias

### Positivas
- Vercel construyó Next.js — compatibilidad perfecta con todas las features del App Router
- Rollback instantáneo con 1 click si hay un bug crítico en producción
- Preview deployments automáticos por Pull Request
- Edge Functions con latencia mínima para Colombia (PoP en São Paulo)
- Analytics de Core Web Vitals integrados

### Negativas / Trade-offs
- $1/mes más caro que Netlify (irrelevante a la escala actual)
- Otro vendor de infraestructura

---

## Referencias

- [CTO Design Review](../../board/decks/) — Sección 08: Problemas con Netlify
- [System Architecture v1](../architecture/SYSTEM_ARCHITECTURE_v1.md) — Sección 01

---

*ADR-002 · Accepted · 2026-06-26*
