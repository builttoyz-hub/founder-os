# /design/trust-ui — Componentes de Confianza

## Propósito

La confianza en un marketplace no se declara — se diseña. Esta carpeta documenta los componentes de UI específicamente diseñados para comunicar y construir confianza: el sistema de reputación visual, los badges de verificación, los indicadores de estado de piezas, y los mensajes de seguridad.

> **Principio:** Cada píxel de trust-ui tiene una función específica: reducir la incertidumbre del comprador o del vendedor en el momento de la decisión.

---

## Componentes de Confianza

### 1. Seller Trust Card
Muestra la confiabilidad de un vendedor de forma inmediata y comparable.

```
┌──────────────────────────────────────┐
│  [Avatar]  Santiago T.               │
│  ⭐ 4.9  · 47 ventas · Medellín     │
│  ✓ Confiable  🏆 Top Vendedor       │
│  Responde en < 2 horas              │
└──────────────────────────────────────┘
```

**Reglas de diseño:**
- El rating siempre visible con 1 decimal
- El badge de mayor nivel del vendedor siempre visible
- El tiempo de respuesta solo si es < 4 horas (señal positiva)
- Color del avatar border = color del badge más alto

---

### 2. Listing Condition Badge
Comunica el estado físico de la pieza con claridad visual inmediata.

| Estado | Color | Ícono | Texto |
|--------|-------|-------|-------|
| Nuevo | Verde `#22C55E` | ✦ | NUEVO |
| Como nuevo | Verde claro `#86EFAC` | ◆ | COMO NUEVO |
| Buen estado | Azul `#60A5FA` | ◇ | BUEN ESTADO |
| Regular | Ámbar `#FCD34D` | ⬡ | REGULAR |
| Para piezas | Rojo `#F87171` | ○ | PIEZAS |

**Regla:** El badge de estado es siempre el primer dato después del título. Es la información más crítica para la decisión de compra.

---

### 3. Price Trust Signal
El precio en un marketplace de segunda mano necesita contexto. ¿Es caro? ¿Barato? ¿Normal?

```
$2,800,000          ← Precio en #AAFF00, grande
≈ Precio de mercado: $2.5M – $3.2M  ← Context en gray-400, pequeño
📦 Con envío disponible              ← Info adicional
```

**Regla:** El precio de mercado de referencia se muestra cuando tenemos suficientes datos (≥3 piezas similares en los últimos 90 días). Cuando no hay datos, no mostramos nada — nunca inventar un "precio de mercado".

---

### 4. Verification Badges
Badges progresivos que comunican niveles de verificación del vendedor.

```
🆕 Nuevo          → Sin borde, gris       → 0-5 ventas
✓ Confiable       → Borde verde suave     → 6-20 ventas, rating ≥ 4.5
🏆 Top            → Borde dorado          → 21-50 ventas, rating ≥ 4.7
⭐ Elite           → Borde platino gradiente → 51+ ventas, rating ≥ 4.8
🏪 Tienda         → Borde verde + ícono tienda → Plan Tienda activo
```

**Regla:** Solo mostrar el badge de mayor nivel. No acumular badges — confunde más de lo que informa.

---

### 5. Safety Alert Component
Señales de advertencia para compradores cuando hay señales de alerta.

```
⚠️  Este vendedor tiene menos de 5 transacciones.
    Toma precauciones adicionales. Ver guía de compra segura →
```

**Cuándo aparece:**
- Vendedor con 0 transacciones (nuevo en la plataforma)
- Precio significativamente por debajo del mercado (> 40% más barato)
- Aviso publicado hace menos de 24 horas sin historial del vendedor

**Tono:** Informativo, no alarmista. "Toma precauciones" vs "¡CUIDADO, POSIBLE ESTAFA!". El primero informa; el segundo destruye la confianza en la plataforma completa.

---

### 6. Transaction Confirmation UI
La pantalla que muestra al vendedor que la pieza fue vendida y al comprador que la transacción fue confirmada.

```
✅ ¡Transacción confirmada!

Felicitaciones a [Vendedor] y [Comprador].
¿Cómo fue la experiencia? Califica la transacción →

[Calificar ahora]   [Más tarde]
```

**Regla:** Siempre mostrar el CTA de calificación en el momento de mayor satisfacción (recién se confirmó). La tasa de calificación baja dramáticamente si el CTA se muestra días después.

---

## Guía de Escritura para Trust UI

El copy de los componentes de confianza sigue estas reglas:

- **Específico, nunca genérico:** "47 ventas en 8 meses" > "Vendedor activo"
- **Evidencia, no afirmación:** "4.9 ⭐ (47 calificaciones)" > "Vendedor excelente"
- **Positivo primero:** Mostrar las fortalezas del vendedor antes de las advertencias
- **Accionable cuando hay alerta:** Cada advertencia tiene un "qué hacer" asociado
- **Lenguaje de la comunidad:** "parcero con trayectoria" vs "usuario verificado premium"

---

*Versión 1.0 — Junio 2026 · PITS MARKET*
