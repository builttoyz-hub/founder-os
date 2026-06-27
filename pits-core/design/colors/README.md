# /design/colors — Sistema de Color PITS MARKET

## La Paleta

### Primarios

| Nombre | Hex | RGB | HSL | Uso |
|--------|-----|-----|-----|-----|
| **Verde Neón** (primario) | `#AAFF00` | rgb(170,255,0) | hsl(75,100%,50%) | CTA principal, highlights, logo, badges activos |
| **Negro Profundo** (background) | `#0A0A0A` | rgb(10,10,10) | hsl(0,0%,4%) | Fondo principal de la aplicación |
| **Blanco Puro** | `#FFFFFF` | rgb(255,255,255) | hsl(0,0%,100%) | Texto principal sobre fondos oscuros |

### Grises (escala de fondo a texto)

| Nombre | Hex | Uso |
|--------|-----|-----|
| Gray 950 | `#0D0D0D` | Fondo cards ligeramente elevadas sobre background |
| Gray 900 | `#141414` | Fondo navbar, sidebar |
| Gray 800 | `#1E1E1E` | Bordes suaves, separadores |
| Gray 700 | `#2C2C2C` | Inputs, áreas de texto |
| Gray 600 | `#3A3A3A` | Bordes de cards |
| Gray 500 | `#555555` | Texto terciario, placeholders |
| Gray 400 | `#7A7A7A` | Texto secundario |
| Gray 300 | `#AAAAAA` | Texto muted |
| Gray 200 | `#D4D4D4` | Bordes muy sutiles en light mode |
| Gray 100 | `#F5F5F5` | Fondos light mode |

### Semánticos

| Nombre | Hex | Uso |
|--------|-----|-----|
| Success | `#22C55E` | Transacción completada, verificado, aprobado |
| Warning | `#F59E0B` | Aviso próximo a vencer, precio bajo |
| Error | `#EF4444` | Error de validación, rechazado, scam alert |
| Info | `#3B82F6` | Información neutral, tooltips |

### Verde — Escala Completa

| Tono | Hex | Uso |
|------|-----|-----|
| Verde 950 | `#052E16` | Fondo de badges de éxito en dark mode |
| Verde 900 | `#14532D` | Fondo de alertas de éxito |
| Verde 700 | `#15803D` | Verde oscuro para texto sobre fondo claro |
| Verde 500 | `#22C55E` | Verde medio (success) |
| Verde 400 | `#4ADE80` | Verde claro para hover |
| Verde neón | `#AAFF00` | El verde PITS MARKET — solo para elementos principales |

## Reglas de Uso

### ✅ Correcto

```
Fondo de la app          → #0A0A0A
Texto principal          → #FFFFFF
CTA primario (botón)     → bg #AAFF00 / text #0A0A0A
Rating badge (activo)    → #AAFF00 con opacidad o sólido
Link / hover             → #AAFF00
Precio del aviso         → #FFFFFF bold
Estado "activo"          → #22C55E (success verde, NO el verde neón)
```

### ❌ Incorrecto

```
Texto sobre verde neón   → NUNCA texto blanco sobre #AAFF00 (contraste insuficiente)
                          → SIEMPRE texto #0A0A0A sobre #AAFF00
Verde neón para errores  → Nunca. Los errores son #EF4444
Múltiples verdes mezclados → Un elemento usa UN verde. No mezclar neón + success.
```

## Contraste y Accesibilidad

| Combinación | Ratio | WCAG AA (4.5:1) | WCAG AAA (7:1) |
|-------------|-------|-----------------|-----------------|
| #FFFFFF sobre #0A0A0A | 19.5:1 | ✅ | ✅ |
| #0A0A0A sobre #AAFF00 | 12.6:1 | ✅ | ✅ |
| #FFFFFF sobre #AAFF00 | 1.5:1 | ❌ | ❌ |
| #AAAAAA sobre #0A0A0A | 7.2:1 | ✅ | ✅ |
