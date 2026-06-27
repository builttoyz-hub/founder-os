# Framework de Decisiones — PITS MARKET

> Cómo se toman decisiones importantes en PITS MARKET. Tener un framework explícito reduce el tiempo de decisión y la ambigüedad.

---

## El Framework Principal: ¿Qué Decisión Es Esta?

Antes de tomar una decisión, clasificarla:

| Tipo | Descripción | Cómo decidir | Ejemplo |
|------|-------------|--------------|---------|
| **Tipo 1** | Irreversible, alto impacto | Lento, con análisis profundo, documentar | Elegir el stack tecnológico |
| **Tipo 2** | Reversible, bajo impacto | Rápido, experimentar, iterar | Cambiar el copy de un botón |
| **Tipo 3** | Urgente y crítica | Rápido pero documentado | Bug crítico en producción |

**Error más común:** Tratar decisiones Tipo 2 como Tipo 1 y quedarse paralizado.

---

## Decisiones de Producto: El Filtro del MVP

Cada feature o cambio propuesto pasa por este filtro en orden:

```
1. ¿Es necesario para que un vendedor publique una pieza?
2. ¿Es necesario para que un comprador contacte al vendedor?
3. ¿Afecta la seguridad o la integridad de los datos?

Si la respuesta a las 3 es NO → Backlog. Sin discusión.
Si alguna respuesta es SÍ → Evaluar cómo resolver de la forma más simple posible.
```

---

## Decisiones de Ingeniería: Build vs Buy

```
¿Es nuestro core differentiator?
  Sí → BUILD
  No → ¿Alguna solución del mercado lo hace suficientemente bien?
    Sí → BUY
    No → BUILD la pieza mínima necesaria
```

---

## Decisiones de Negocio: El Test del Fundador

Para decisiones estratégicas importantes, hacerse estas 4 preguntas:

1. **¿Esto nos acerca a tener 100 usuarios en el marketplace?** Si no, ¿por qué es una prioridad?
2. **¿Estaríamos orgullosos de esta decisión en 2 años?** Si hay duda, no hacerlo.
3. **¿Qué diría el CTO de un marketplace con 10M de usuarios sobre esta decisión?** ¿Parece sabio o cortoplacista?
4. **¿Estamos haciendo esto por miedo o por convicción?** El miedo es mal consejero en decisiones de startup.

---

## Decisiones que Requieren Más de 1 Persona

| Decisión | Quién decide | Quién aprueba |
|----------|-------------|----------------|
| Arquitectura técnica mayor | CTO | Fundador |
| Cambio de scope del MVP | Fundador | — |
| Nuevo proveedor > $100K COP/mes | Fundador | — |
| Cambio en términos legales | Abogado externo | Fundador |
| Primera contratación | Fundador | — |
| Precio de planes | Fundador | — |

---

*Versión 1.0 — Junio 2026*
