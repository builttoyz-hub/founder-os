# Contributing to PITS MARKET

Gracias por querer contribuir a PITS CORE. Este documento explica cómo funciona el trabajo en este repositorio.

> Este repositorio es de **documentación y conocimiento**, no de código de aplicación. Los cambios aquí definen cómo opera PITS MARKET como empresa.

---

## Tipos de Contribución

| Tipo | Descripción | Quién puede hacerlo |
|------|-------------|---------------------|
| **Documentación** | Agregar o actualizar documentos en cualquier carpeta | Todo el equipo |
| **Arquitectura** | Cambios en `engineering/` | Solo equipo técnico + CTO sign-off |
| **Legal** | Cambios en `legal/` | Solo Fundador + abogado externo |
| **Board** | Cambios en `board/` | Solo Fundador y directores |
| **Producto** | Cambios en `product/` | Product team + Fundador |

---

## Proceso de Contribución

### 1. Crear un Branch

```bash
# Formato: tipo/descripcion-corta
git checkout -b docs/add-competitor-analysis
git checkout -b engineering/update-db-schema-v2
git checkout -b product/spec-search-feature
```

### 2. Convención de Naming de Archivos

- **Siempre en minúsculas con guiones:** `competitor-analysis-facebook-marketplace.md`
- **Prefijo de fecha para documentos con versión:** `2026-07-15-board-meeting-minutes.md`
- **Prefijo de versión para specs:** `v1.0-search-feature-spec.md`
- **Sin espacios, sin caracteres especiales, sin tildes en nombres de archivo**

### 3. Convención de Commits

```
tipo(scope): descripción en minúsculas (max 72 caracteres)

Tipos válidos:
  docs     → Documentación nueva o actualizada
  feat     → Nuevo documento de feature/producto
  fix      → Corrección de información incorrecta
  refactor → Reorganización sin cambio de contenido
  chore    → Tareas de mantenimiento del repo
  security → Cambios relacionados con seguridad

Scopes válidos:
  engineering | product | growth | board | brand | legal | research | founder-os

Ejemplos:
  docs(engineering): add runbook for supabase outage
  feat(product): add spec for messaging feature v2
  docs(board): add Q3 2026 investor report
  security(legal): update privacy policy for LATAM expansion
```

### 4. Pull Request

- Usar el template incluido en `.github/PULL_REQUEST_TEMPLATE.md`
- Asignar al propietario de la carpeta como reviewer
- No hacer merge sin al menos 1 approval
- Describir qué cambió y por qué

### 5. Review

| Carpeta | Reviewer primario | Reviewer secundario |
|---------|-------------------|---------------------|
| `engineering/` | CTO | Fundador |
| `product/` | Fundador | Product Lead |
| `board/` | Fundador | — |
| `legal/` | Fundador | Abogado externo |
| `brand/` | Head of Design | Fundador |
| `growth/` | Head of Growth | Fundador |
| `research/` | Product Lead | — |
| Cualquier otra | Fundador | — |

---

## Estándares de Documentación

### Estructura de un buen documento

```markdown
# Título del Documento

> Una línea que describe exactamente qué es este documento.

## Contexto
Por qué existe este documento.

## Contenido Principal
El cuerpo del documento.

## Decisiones / Conclusiones
Si aplica, qué se decidió.

## Próximos Pasos
Acciones concretas con responsable y fecha.

---
*Creado: YYYY-MM-DD | Autor: Nombre | Versión: X.Y*
```

### Reglas de Markdown

- Usar `#` para el título principal (solo uno por documento)
- Usar `##` para secciones principales
- Usar tablas para comparaciones y listas de datos
- Usar `>` para notas y advertencias importantes
- Usar ` ```código``` ` para cualquier fragmento técnico
- Imágenes en la misma carpeta del documento o en `brand/assets/`

---

## Lo que NO hacer

- ❌ No subir archivos `.env`, contraseñas, API keys ni secretos de ningún tipo
- ❌ No subir archivos de diseño sin exportar (`.psd`, `.fig` sin exports)
- ❌ No borrar documentos — moverlos a `archive/deprecated/` con nota de qué los reemplaza
- ❌ No hacer commits directamente a `main` — siempre via Pull Request
- ❌ No modificar documentos en `legal/` sin la firma del Fundador y revisión legal
- ❌ No subir datos personales de usuarios o vendedores de la plataforma

---

## Preguntas

Abrir un issue con el label `question` o escribir a builttoyz@gmail.com.

---

*Última actualización: Junio 2026 | PITS MARKET*
