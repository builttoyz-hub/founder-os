# /product — Definición del Producto

## Propósito

Esta carpeta contiene todo lo relacionado con la **definición de qué construye PITS MARKET y por qué**. Es la fuente de verdad del producto: qué existe, qué viene, qué decidimos no hacer y cómo llegamos a esas decisiones.

> **Regla:** El código no puede existir sin un documento en esta carpeta que lo justifique. Un feature sin spec es un feature que nadie entiende.

---

## Subcarpetas

### `/roadmap` — Plan por versión
El camino de MVP a V3. Cada versión tiene su propio documento con features, métricas de exit y timeline.

### `/specs` — Especificaciones funcionales
Documento detallado de cada feature antes de construirlo. El equipo de ingeniería no inicia desarrollo sin una spec aprobada.

### `/ux` — Flujos y experiencia de usuario
User flows, wireframes, mapas de customer journey. El puente entre la spec y el diseño visual.

### `/research` — Investigación de producto
User interviews, encuestas, sesiones de usabilidad. La voz del usuario documentada.

---

## Convención de Nombres

```
[tipo]-[descripcion]-[version/fecha].md

Tipos: spec | flow | roadmap | research | decision

Ejemplos correctos:
  product/specs/spec-publish-listing-v1.md
  product/roadmap/roadmap-mvp-v1.md
  product/ux/flow-buyer-contact-v1.md
  product/research/user-interview-seller-medellin-2026-07.md

Ejemplos incorrectos:
  feature.md                    ← no descriptivo
  Especificacion Busqueda.md    ← espacios y mayúsculas
  spec_search_v2.md             ← guiones bajos
```

---

## Documentos Actuales

| Documento | Carpeta | Estado |
|-----------|---------|--------|
| MVP Launch Plan v1 | `roadmap/` | ✅ Completo |
| Documento Maestro Oficial v1 | `roadmap/` | ✅ Completo |

---

## Template de Spec

Cada spec debe responder estas preguntas:

```markdown
# Feature Spec: [Nombre del Feature]

**Versión:** v1.0
**Estado:** Draft | In Review | Approved | Implemented
**Autor:** [Nombre]
**Fecha:** YYYY-MM-DD

## Resumen
Una oración que describe el feature.

## Problema que Resuelve
¿Qué frustración del usuario soluciona?

## Usuario Objetivo
Comprador / Vendedor / Admin / Todos

## Descripción Funcional
Qué hace exactamente el feature, paso a paso.

## Casos de Uso
1. Caso principal (happy path)
2. Casos alternativos
3. Casos de error

## Criterios de Aceptación
- [ ] El usuario puede hacer X
- [ ] El sistema hace Y cuando Z
- [ ] Los errores se muestran como W

## Fuera de Scope
Qué NO hace este feature (explícitamente).

## Métricas de Éxito
Cómo sabemos que el feature funciona.

## Dependencias Técnicas
Qué necesita del equipo de ingeniería.

## Mockups
Links o imágenes de mockups.
```

---

*Propietario: Fundador / Product Lead · Revisión: Por sprint*
