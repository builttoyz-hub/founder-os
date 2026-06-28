# /design/icons — Sistema de Iconografía

## Biblioteca Principal: Lucide Icons

PITS MARKET usa **Lucide Icons** como biblioteca de íconos principal. Razones:
- Open source, sin licencia de uso
- Consistente (todos los íconos siguen las mismas reglas de diseño)
- Tree-shakeable (solo se importa lo que se usa)
- Compatible con React y cualquier framework moderno

**Importar en Next.js:**
```jsx
import { Search, ChevronDown, MapPin } from 'lucide-react'
```

---

## Íconos Clave por Contexto

### Navegación y Acciones Principales

| Ícono Lucide | Código | Uso en PITS MARKET |
|--------------|--------|-------------------|
| `Search` | `<Search />` | Barra de búsqueda |
| `Filter` | `<Filter />` | Panel de filtros |
| `Plus` | `<Plus />` | Publicar pieza (CTA) |
| `Menu` | `<Menu />` | Menú hamburguesa mobile |
| `X` | `<X />` | Cerrar modal, limpiar filtro |
| `ChevronDown` | `<ChevronDown />` | Dropdown, expandir |
| `ArrowLeft` | `<ArrowLeft />` | Volver atrás |

### Piezas y Marketplace

| Ícono Lucide | Código | Uso en PITS MARKET |
|--------------|--------|-------------------|
| `Camera` | `<Camera />` | Subir fotos |
| `Image` | `<Image />` | Galería de fotos |
| `Tag` | `<Tag />` | Precio |
| `MapPin` | `<MapPin />` | Ciudad del aviso |
| `Package` | `<Package />` | Estado "Nuevo en caja" |
| `Wrench` | `<Wrench />` | Categoría general de piezas |
| `Zap` | `<Zap />` | Performance, turbos, potencia |
| `Truck` | `<Truck />` | Envío disponible |
| `Eye` | `<Eye />` | Vistas del aviso |

### Confianza y Reputación

| Ícono Lucide | Código | Uso en PITS MARKET |
|--------------|--------|-------------------|
| `Star` | `<Star />` | Rating (estrella llena) |
| `StarHalf` | `<StarHalf />` | Rating (media estrella) |
| `Shield` | `<Shield />` | Vendedor verificado |
| `CheckCircle` | `<CheckCircle />` | Aprobado, verificado |
| `AlertTriangle` | `<AlertTriangle />` | Advertencia de seguridad |
| `XCircle` | `<XCircle />` | Error, rechazado |
| `ThumbsUp` | `<ThumbsUp />` | Calificación positiva |

### Comunicación

| Ícono Lucide | Código | Uso en PITS MARKET |
|--------------|--------|-------------------|
| `MessageCircle` | `<MessageCircle />` | WhatsApp / Mensajes |
| `Phone` | `<Phone />` | Teléfono de contacto |
| `Share2` | `<Share2 />` | Compartir aviso |
| `Heart` | `<Heart />` | Guardar en favoritos |
| `Bell` | `<Bell />` | Notificaciones |

### Admin

| Ícono Lucide | Código | Uso en PITS MARKET |
|--------------|--------|-------------------|
| `LayoutDashboard` | `<LayoutDashboard />` | Dashboard |
| `Users` | `<Users />` | Gestión de usuarios |
| `ClipboardList` | `<ClipboardList />` | Lista de avisos |
| `BarChart3` | `<BarChart3 />` | Métricas |
| `Settings` | `<Settings />` | Configuración |

---

## Reglas de Uso

1. **Tamaño estándar:** 20px para íconos inline, 24px para íconos de acción, 32px para íconos de hero
2. **Stroke width:** 1.5px (el default de Lucide — no cambiar)
3. **Color:** Heredar del texto padre (`currentColor`) o especificar explícitamente
4. **Nunca usar íconos sin label accesible:** Siempre `aria-label` o texto visible acompañante
5. **No mezclar librerías:** Si necesitas un ícono que no está en Lucide, agregarlo como SVG custom — no importar otra librería

---

## Íconos Custom (cuando Lucide no alcanza)

Los íconos custom de PITS MARKET se guardan en `/brand/assets/icons/` como SVGs optimizados y se documentan aquí con su nombre y uso.

| Ícono Custom | Archivo | Uso |
|--------------|---------|-----|
| *(por agregar cuando sean necesarios)* | | |
