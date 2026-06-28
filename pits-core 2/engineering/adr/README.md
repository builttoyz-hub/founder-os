# /engineering/adr — Architecture Decision Records

## Propósito

Un ADR documenta una decisión de arquitectura importante: qué se decidió, por qué, qué alternativas se evaluaron, y cuáles son las consecuencias. Los ADRs son **inmutables**: una vez tomada una decisión, el registro no se borra ni se modifica. Si la decisión cambia, se crea un nuevo ADR que la reemplaza y referencia al anterior.

> **Por qué importan:** Las decisiones de arquitectura sin contexto se convierten en "cargo cult engineering" — el equipo futuro sigue las decisiones del pasado sin saber por qué, y no puede cambiarlas inteligentemente.

---

## Formato de un ADR

```markdown
# ADR-[NNN]: [Título de la Decisión]

**Estado:** Proposed | Accepted | Deprecated | Superseded by ADR-[NNN]
**Fecha:** YYYY-MM-DD
**Autores:** [Nombres]
**Revisores:** [Nombres]

## Contexto

¿Qué situación o problema motivó esta decisión?
¿Qué restricciones o requisitos existían?

## Decisión

¿Qué se decidió exactamente?
Sea específico y sin ambigüedad.

## Alternativas Consideradas

### Alternativa A: [Nombre]
- Pros: ...
- Contras: ...

### Alternativa B: [Nombre]
- Pros: ...
- Contras: ...

## Consecuencias

### Positivas
- [Beneficio 1]

### Negativas / Trade-offs
- [Costo o limitación 1]

### Riesgos
- [Riesgo 1 y cómo se mitiga]

## Referencias
- [Link a documento relacionado]
```

---

## ADRs Registrados

| ID | Título | Estado | Fecha |
|----|--------|--------|-------|
| ADR-001 | Supabase sobre backend custom en Node.js | Accepted | 2026-06-26 |
| ADR-002 | Vercel sobre Netlify para hosting de Next.js | Accepted | 2026-06-26 |
| ADR-003 | PostgreSQL con precio en enteros (pesos, no centavos) | Accepted | 2026-06-26 |
| ADR-004 | WhatsApp externo como canal de contacto en el MVP | Accepted | 2026-06-26 |
| ADR-005 | Formulario de publicación de 1 página sobre wizard de pasos | Accepted | 2026-06-26 |

---

## Convención de Nombres

```
adr-[NNN]-[titulo-kebab-case].md

NNN: número de 3 dígitos, secuencial
Ejemplos:
  adr-001-supabase-over-custom-backend.md
  adr-002-vercel-over-netlify.md
  adr-006-typesense-for-search-beta.md
```

---

## Relación con /decisions

`/engineering/adr/` y `/decisions/` son complementarios, no duplicados:

| `/engineering/adr/` | `/decisions/` |
|--------------------|--------------|
| Decisiones de arquitectura técnica interna | Decisiones de negocio, producto y estrategia |
| ADR-001: Usar Supabase | 0001: No cobrar en el MVP |
| ADR-002: Vercel sobre Netlify | 0002: Sistema de reputación 4 dimensiones |
| Audiencia: equipo técnico | Audiencia: todos + inversionistas |

**Regla:** ¿La decisión cambia cómo se construye el sistema internamente? → ADR. ¿Cambia cómo el usuario experimenta el producto o cómo gana dinero la empresa? → /decisions.
