# /design/components — Especificaciones de Componentes UI

## Propósito

La especificación funcional y visual de cada componente reutilizable de PITS MARKET. Un componente documentado aquí tiene: qué es, cuándo usarlo, cuándo NO usarlo, sus variantes, sus estados, y las reglas de accesibilidad.

## Componentes del MVP

| Componente | Estado | Prioridad |
|------------|--------|-----------|
| `listing-card.md` | Por documentar | Alta |
| `search-bar.md` | Por documentar | Alta |
| `filter-panel.md` | Por documentar | Alta |
| `photo-gallery.md` | Por documentar | Alta |
| `seller-trust-card.md` | Ver `/trust-ui` | Alta |
| `whatsapp-cta-button.md` | Por documentar | Alta |
| `badge-condition.md` | Ver `/trust-ui` | Alta |
| `skeleton-loader.md` | Por documentar | Media |
| `empty-state.md` | Por documentar | Media |
| `modal.md` | Por documentar | Media |
| `toast-notification.md` | Por documentar | Media |

## Template de Componente

```markdown
# Componente: [Nombre]

## Qué es
Una línea describiendo el componente.

## Cuándo usar
- [Caso 1]

## Cuándo NO usar
- [Anti-caso 1]

## Variantes
| Variante | Descripción | Cuándo |
|----------|-------------|--------|

## Estados
| Estado | Descripción | Visual |
|--------|-------------|--------|
| default | | |
| hover | | |
| active | | |
| disabled | | |
| loading | | |
| error | | |

## Props / Parámetros
| Prop | Tipo | Requerido | Default | Descripción |
|------|------|-----------|---------|-------------|

## Accesibilidad
- role: [ARIA role]
- aria-label: [cuándo y qué]
- Keyboard: [cómo se navega con teclado]

## Ejemplo de uso
[Code snippet o descripción de implementación]
```
