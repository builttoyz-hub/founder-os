# /docs — Documentación Técnica Viva

## Propósito

Esta carpeta contiene la documentación técnica **activa y vigente** del sistema PITS MARKET. Es la primera parada para cualquier desarrollador que se une al equipo o necesita entender cómo funciona el sistema.

> **Regla de oro:** Si no está aquí documentado, no existe oficialmente. Si cambia en el código, debe cambiar aquí primero.

---

## ¿Qué va aquí?

| Tipo de Documento | Descripción | Ejemplo |
|------------------|-------------|---------|
| Guías de inicio | Cómo configurar el entorno de desarrollo | `setup-local-environment.md` |
| Glosario técnico | Términos específicos del sistema y el dominio | `glossary.md` |
| Decisiones de diseño de alto nivel | Resumen ejecutivo de decisiones técnicas | `tech-decisions-overview.md` |
| FAQs técnicas | Preguntas frecuentes del equipo de desarrollo | `engineering-faq.md` |
| Diagramas del sistema | Imágenes y diagramas explicativos | `diagrams/` |
| Onboarding para nuevos devs | Guía de primer día para nuevos miembros técnicos | `onboarding-engineer.md` |

---

## ¿Qué NO va aquí?

- Especificaciones detalladas de features → `product/specs/`
- Schema de base de datos → `engineering/database/`
- Arquitectura técnica detallada → `engineering/architecture/`
- Runbooks operacionales → `engineering/runbooks/`
- ADRs (Architecture Decision Records) → `engineering/adr/`

---

## Convención de Nombres

```
kebab-case-siempre.md
sin-tildes-ni-caracteres-especiales.md
prefijo-de-version-si-aplica-v1.md

Ejemplos correctos:
  setup-local-environment.md
  glossary-automotive-domain.md
  onboarding-engineer-day-one.md

Ejemplos incorrectos:
  Setup Local.md           ← espacios
  Glosario_Técnico.md      ← guiones bajos y tildes
  doc1.md                  ← sin descripción
```

---

## Documentos Actuales

| Archivo | Descripción | Última actualización |
|---------|-------------|---------------------|
| *(por crear)* `setup-local-environment.md` | Configuración del entorno local | — |
| *(por crear)* `glossary.md` | Glosario de términos técnicos y de negocio | — |
| *(por crear)* `onboarding-engineer.md` | Guía de primer día para devs | — |
| *(por crear)* `tech-stack-rationale.md` | Por qué elegimos cada tecnología | — |

---

## Plantilla de Documento

```markdown
# Título del Documento

> Una línea que describe exactamente para qué sirve este documento.

**Aplica a:** [tecnología/área]
**Audiencia:** [devs junior | devs senior | todo el equipo técnico]
**Última revisión:** YYYY-MM-DD

---

## Resumen

[Párrafo ejecutivo de qué hace este documento]

## Contenido

[El contenido principal]

## Referencias

- [Link a documento relacionado]

---
*Creado: YYYY-MM-DD | Autor: Nombre | Versión: 1.0*
```

---

*Propietario: CTO · Revisión: Cada vez que haya cambios técnicos significativos*
