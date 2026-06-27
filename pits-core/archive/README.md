# /archive — Archivos Históricos

## Propósito

El cementerio organizado de PITS MARKET. Los documentos que han sido reemplazados o descontinuados no se borran — se mueven aquí con una nota que explica qué los reemplaza. El historial importa.

> **Regla de oro:** Nada se borra del repositorio principal. Se archiva. Borrar un documento es borrar el contexto de una decisión.

---

## Subcarpetas

### `/deprecated` — Documentos reemplazados
Documentos que fueron reemplazados por una versión más nueva. Al moverlos aquí, se debe agregar un header que indique qué los reemplaza y cuándo fueron archivados.

### `/historical` — Versiones anteriores para referencia
Versiones anteriores de documentos que pueden ser útiles para entender la evolución del proyecto. No están activos, pero su contexto histórico tiene valor.

---

## Cómo Archivar un Documento

1. **Mover** el archivo a la carpeta correspondiente (`deprecated/` o `historical/`)
2. **Agregar** este header al inicio del archivo:

```markdown
> ⚠️ **ARCHIVO ARCHIVADO**
> **Fecha de archivo:** YYYY-MM-DD
> **Razón:** [Por qué fue archivado]
> **Reemplazado por:** [Link al documento nuevo, si aplica]
> **No usar para decisiones activas.**

---
[Contenido original del documento sigue aquí]
```

3. **Actualizar** el documento nuevo para que referencie al anterior si hay contexto histórico relevante.

---

## Convención de Nombres

Los archivos archivados mantienen su nombre original. Si hay conflicto de nombres, agregar el prefijo de fecha de archivo:

```
[nombre-original].md                        → si no hay conflicto
[YYYY-MM-DD]-archived-[nombre-original].md  → si hay conflicto de nombre

Ejemplos:
  deprecated/roadmap-mvp-v0-draft.md
  deprecated/2026-06-15-archived-old-scope.md
  historical/2026-07-launch-landing-page-copy-v1.md
```

---

## Lo que NO va aquí

- **Datos de usuarios** de la plataforma → nunca en el repo
- **Secretos o credenciales** expiradas → eliminar, no archivar
- **Archivos gigantes** (>10MB) → usar almacenamiento externo
- **Documentos activos** → siguen en su carpeta original

---

*Este repositorio es la memoria institucional de PITS MARKET. Archivamos, no borramos.*
