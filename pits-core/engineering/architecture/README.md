# /engineering/architecture — Arquitectura del Sistema

## Propósito

Documenta cómo está construido el sistema PITS MARKET a nivel macro: qué tecnologías se usan, cómo se comunican entre sí, y cuáles fueron las decisiones de diseño principales. Es la primera lectura obligatoria para cualquier ingeniero que se une al equipo.

## Documentos Actuales

| Documento | Descripción | Estado |
|-----------|-------------|--------|
| `SYSTEM_ARCHITECTURE_v1.md` | Arquitectura completa del sistema — 25 secciones | ✅ Completo |

## Convención de Nombres

```
SYSTEM_ARCHITECTURE_v[N].md        → Documento principal de arquitectura
architecture-[componente]-v[N].md  → Arquitectura de un componente específico

Ejemplos:
  SYSTEM_ARCHITECTURE_v1.md
  SYSTEM_ARCHITECTURE_v2.md
  architecture-search-engine-v1.md
  architecture-image-pipeline-v1.md
  architecture-mobile-app-v1.md
```

## Secciones del System Architecture

El documento `SYSTEM_ARCHITECTURE_v1.md` cubre:
1. Arquitectura completa del sistema (diagrama)
2. Organización del frontend
3. Organización del backend
4. Arquitectura de Supabase
5. Diseño de base de datos
6. Relaciones entre tablas
7. Sistema de autenticación
8. Sistema de permisos
9. Gestión de imágenes
10. Sistema de búsqueda
11. Compatibilidades automotrices
12. Arquitectura preparada para IA
13. Arquitectura preparada para App móvil
14. APIs internas
15. APIs públicas futuras
16. Escalabilidad a 1 millón de usuarios
17. Estrategia de caché
18. Estrategia CDN
19. Seguridad
20. Backups
21. Logging
22. Observabilidad
23. Costos estimados
24. Riesgos técnicos
25. Roadmap tecnológico
