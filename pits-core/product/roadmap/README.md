# /product/roadmap — Plan de Versiones

## Propósito

El roadmap define **cuándo** llega qué feature y en qué orden. No es una lista de deseos — es un plan con hipótesis a validar y métricas de exit para cada fase.

> **Regla:** Solo avanzamos de fase cuando tenemos evidencia de que la hipótesis se cumplió, no cuando se acabó el tiempo.

## Convención de Nombres

```
roadmap-[fase]-v[version].md

Ejemplos:
  roadmap-mvp-v1.md
  roadmap-beta-v1.md
  roadmap-v1-release.md
  roadmap-2027-annual.md
```

## Fases del Roadmap

| Fase | Hipótesis | Archivo |
|------|-----------|---------|
| MVP | ¿Los vendedores publican y los compradores contactan? | `roadmap-mvp-v1.md` |
| Beta | ¿Los usuarios pagan por visibilidad? | *(por crear)* |
| V1 | ¿La plataforma retiene usuarios? | *(por crear)* |
| V2 | ¿Las transacciones mediadas generan revenue predecible? | *(por crear)* |
| V3 | ¿El modelo escala a otros países? | *(por crear)* |

## Backlog General

Todo lo que no está en el roadmap activo vive en `backlog-master.md` con:
- Descripción del feature
- Por qué fue diferido
- Versión objetivo tentativa
- Señal que lo activaría (qué métrica o evento haría que entre al roadmap)
