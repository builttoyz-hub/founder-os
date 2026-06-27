# /brand — Identidad de Marca

## Propósito

Todo lo que define cómo se ve, suena y se siente PITS MARKET. Esta carpeta es la fuente de verdad de la identidad de marca: los activos visuales, las reglas de uso, el tono de comunicación y la voz de la comunidad.

> **Principio:** La marca de PITS MARKET nació de adentro de la comunidad tuning colombiana. Cada decisión de diseño y comunicación debe mantener esa autenticidad. Somos los únicos que no estamos tratando de entender la cultura — somos parte de ella.

---

## Subcarpetas

### `/identity` — Sistema de identidad visual
Logos en todos sus formatos, paleta de colores con códigos exactos, tipografías oficiales, y las reglas básicas de uso. La base del sistema visual.

### `/assets` — Archivos exportados listos para usar
PNGs, SVGs, WebPs de todos los assets de marca en los tamaños estándar. Estos son los archivos que se usan en producción — ya exportados y listos.

### `/guidelines` — Manual de marca completo
Las reglas detalladas: qué se puede y no se puede hacer con el logo, cómo usar los colores, espaciado mínimo, versiones para fondos claros y oscuros.

### `/voice` — Tono y voz de comunicación
Cómo habla PITS MARKET: el vocabulario de la comunidad, los patrones de copy para redes sociales, el tono en emails de notificación y la voz en los mensajes de error.

---

## Identidad Visual en 30 Segundos

| Elemento | Valor | Notas |
|----------|-------|-------|
| Color primario | `#AAFF00` | Verde neón — energía, velocidad, distinción |
| Color de fondo | `#0A0A0A` | Negro profundo — premium, técnico |
| Color de acento | `#FFFFFF` | Blanco — legibilidad, contraste |
| Tipografía UI | Barlow Condensed | Bold para headlines, Regular para body |
| Tipografía técnica | Share Tech Mono | Para datos técnicos, códigos de motor |
| Estética referencia | NFS Underground | Dark, aggressive, comunidad callejera |

---

## Convención de Nombres

```
identity/   → logo-[variante]-[version].[ext]
              → colors-palette-v[N].md
              → typography-system-v[N].md

assets/     → logo-[variante]-[tamaño].[ext]
              → icon-[nombre]-[tamaño].[ext]

guidelines/ → brand-guidelines-v[N].md
              → logo-usage-rules-v[N].md

voice/      → voice-tone-guide-v[N].md
              → copy-patterns-social-v[N].md
              → vocabulary-community-v[N].md

Variantes de logo: primary | dark | light | horizontal | vertical | icon
Tamaños: 32 | 64 | 128 | 256 | 512 | 1024

Ejemplos:
  assets/logo-primary-512.png
  assets/logo-dark-background-256.png
  assets/icon-marketplace-32.svg
  guidelines/brand-guidelines-v1.md
  voice/copy-patterns-social-instagram-v1.md
```

---

## Los 3 Assets Mínimos Siempre Disponibles

Estos archivos siempre deben existir en `assets/`:

| Archivo | Uso |
|---------|-----|
| `logo-primary-1024.png` | Alta resolución, uso general |
| `logo-transparent-512.png` | Para uso sobre fondos oscuros |
| `logo-glow-512.png` | Con efecto glow verde, para momentos especiales |

---

*Propietario: Fundador / Head of Design · Revisión: Por versión mayor*
