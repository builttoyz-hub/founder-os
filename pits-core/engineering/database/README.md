# /engineering/database — Base de Datos

## Propósito

El diseño completo de la base de datos de PITS MARKET: tablas, relaciones, índices, triggers, políticas de seguridad (RLS), y la estrategia de evolución del schema. **Ninguna tabla puede crearse en producción sin estar documentada aquí primero.**

## Documentos Actuales

| Documento | Descripción | Estado |
|-----------|-------------|--------|
| `DATABASE_BIBLE_v1.md` | Diseño completo de la base de datos — 17 secciones | ✅ Completo |

## Convención de Nombres

```
DATABASE_BIBLE_v[N].md               → Documento maestro de DB
migration-[descripcion]-[fecha].md   → Documentación de una migración
schema-snapshot-[fecha].md           → Snapshot del schema en un momento dado

Ejemplos:
  DATABASE_BIBLE_v1.md
  DATABASE_BIBLE_v2.md
  migration-add-reviews-table-2026-09.md
  migration-add-typesense-columns-2026-10.md
  schema-snapshot-mvp-launch-2026-07.md
```

## Secciones del Database Bible

El documento `DATABASE_BIBLE_v1.md` cubre:
1. Filosofía y principios de diseño (10 principios)
2. Convenciones de nombres
3. Diagrama ER completo
4. Entidades principales con todos sus campos
5. Relaciones entre tablas y cardinalidades
6. Estrategia para compatibilidades automotrices
7. Estrategia para búsquedas rápidas
8. Estrategia para favoritos
9. Estrategia para mensajes
10. Estrategia para notificaciones
11. Estrategia para imágenes
12. Estrategia para reputación
13. Estrategia para suscripciones
14. Estrategia para analytics
15. Estrategia para auditoría
16. Campos obligatorios vs opcionales
17. Reglas de evolución del schema

## Tablas del MVP (6 tablas)

Las únicas 6 tablas del MVP (de las 25+ del Database Bible):

| Tabla | Propósito |
|-------|-----------|
| `profiles` | Usuarios del sistema |
| `listings` | Piezas en venta |
| `listing_images` | Metadata de imágenes |
| `listing_views` | Registro de vistas (deduplicado) |
| `admin_actions` | Log de acciones del admin |
| `email_log` | Registro de emails enviados |
