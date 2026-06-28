# /design/system — Design System PITS MARKET

## Propósito

El design system es el lenguaje compartido entre diseñadores y desarrolladores. Define los tokens (variables de diseño) que se traducen directamente a clases de Tailwind y a variables CSS. Un token cambiado aquí cambia toda la plataforma.

## Design Tokens

### Espaciado (basado en escala de 4px)

```
space-1:  4px
space-2:  8px
space-3:  12px
space-4:  16px
space-5:  20px
space-6:  24px
space-8:  32px
space-10: 40px
space-12: 48px
space-16: 64px
space-20: 80px
space-24: 96px
```

### Border Radius

```
radius-sm:   4px   → Chips, badges pequeños
radius-md:   8px   → Botones, inputs
radius-lg:   12px  → Cards de listing
radius-xl:   16px  → Modales
radius-full: 9999px → Badges circulares, avatares
```

### Sombras

```
shadow-sm:  0 1px 2px rgba(0,0,0,0.3)                    → Elementos sobre fondo oscuro
shadow-md:  0 4px 6px rgba(0,0,0,0.4)                    → Cards elevadas
shadow-lg:  0 10px 15px rgba(0,0,0,0.5)                  → Modales
shadow-neon: 0 0 20px rgba(170,255,0,0.3)                 → Hover en CTA principal
```

### Breakpoints

```
sm:  640px   → Teléfonos grandes
md:  768px   → Tablets
lg:  1024px  → Laptops
xl:  1280px  → Desktops
2xl: 1536px  → Monitores grandes
```

## Grid del Marketplace

```
Mobile (< 640px):    1 columna
Tablet (640–1024px): 2 columnas
Desktop (> 1024px):  3 columnas
Wide (> 1280px):     4 columnas

Gap entre cards: 16px (space-4)
Padding del grid: 16px cada lado en mobile, 24px en tablet+
```

## Animaciones

```
duration-fast:   150ms  → Hover states, micro-interacciones
duration-normal: 250ms  → Transiciones de página, accordions
duration-slow:   400ms  → Modales, skeleton → contenido real
easing: cubic-bezier(0.4, 0, 0.2, 1)  → Material Design easing
```
