# /design/typography — Tipografía PITS MARKET

## Fuentes Oficiales

### Barlow Condensed — UI Principal
**Fuente:** Google Fonts — `Barlow Condensed`
**Uso:** Todos los textos de interfaz, navegación, labels, body text, precios
**Por qué:** Condensada para aprovechar el espacio horizontal en mobile. Alta legibilidad. Personalidad técnica y directa sin ser fría.

```css
/* Import */
@import url('https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@400;500;600;700;900&display=swap');

/* Variables */
--font-ui: 'Barlow Condensed', system-ui, sans-serif;
```

### Share Tech Mono — Datos Técnicos
**Fuente:** Google Fonts — `Share Tech Mono`
**Uso:** Códigos de motor (N55B30, EA113), precios en formato técnico, números de parte, IDs de aviso
**Por qué:** Monospace refuerza la naturaleza técnica del dato. Referencia al mundo de los computadores de carrera.

```css
/* Import */
@import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap');

/* Variables */
--font-mono: 'Share Tech Mono', 'Courier New', monospace;
```

---

## Escala Tipográfica

| Token | Tamaño | Peso | Line Height | Uso |
|-------|--------|------|------------|-----|
| `text-xs` | 12px | 400 | 1.5 | Labels mínimos, timestamps, metadata |
| `text-sm` | 14px | 400–500 | 1.5 | Texto secundario, descriptions |
| `text-base` | 16px | 400–500 | 1.5 | Cuerpo principal de texto |
| `text-lg` | 18px | 500–600 | 1.4 | Subtítulos de sección, precio en card |
| `text-xl` | 20px | 600 | 1.3 | Títulos de cards, labels importantes |
| `text-2xl` | 24px | 700 | 1.2 | Precio en página de detalle |
| `text-3xl` | 30px | 700–900 | 1.1 | H2, títulos de sección |
| `text-4xl` | 36px | 900 | 1.0 | H1, headline de landing |
| `text-5xl` | 48px | 900 | 1.0 | Hero headline |
| `text-6xl` | 60px | 900 | 1.0 | Display, portadas |

---

## Jerarquía por Componente

### Listing Card

```
Título del aviso:    text-xl / font-bold / text-white
Precio:              text-2xl / font-black / text-[#AAFF00]
Ciudad:              text-sm / font-medium / text-gray-400
Estado de la pieza:  text-xs / font-semibold / badge
Fecha:               text-xs / text-gray-500
```

### Página de Detalle

```
Título:              text-3xl / font-bold / text-white
Precio:              text-4xl / font-black / text-[#AAFF00]
Descripción:         text-base / font-normal / text-gray-300 / line-height: 1.7
Código de motor:     Share Tech Mono / text-sm / text-[#AAFF00]
Info del vendedor:   text-sm / font-medium / text-white
Rating:              text-lg / font-bold / text-yellow-400
```

### Navegación

```
Links:               text-base / font-semibold / uppercase / tracking-wide
CTA primario:        text-base / font-bold / uppercase / tracking-wider
```

---

## Reglas Tipográficas

1. **Nunca mezclar más de 2 fuentes en una pantalla.** Barlow Condensed para UI, Share Tech Mono para datos técnicos.
2. **Los precios siempre en Barlow Condensed Black (900), nunca en Share Tech Mono.** Los precios son acción, no código.
3. **Los códigos de motor SIEMPRE en Share Tech Mono.** "N55B30" en Barlow Condensed pierde su identidad técnica.
4. **Uppercase para labels cortos y CTAs, sentence case para body text.**
5. **Line height mínimo 1.5 para body text.** La legibilidad en mobile depende del interlineado.
