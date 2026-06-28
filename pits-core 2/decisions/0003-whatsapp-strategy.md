# 0003 — WhatsApp como Canal de Contacto en MVP, Mensajería Interna en V2

**Estado:** ACTIVE
**Fecha:** 2026-06-26
**Decidido por:** Santiago Tarazona (Fundador)
**Área:** Producto
**Impacto:** Alto

---

## Resumen

En el MVP, el contacto entre compradores y vendedores en PITS MARKET ocurre por WhatsApp externo (link wa.me). PITS MARKET no construye mensajería interna en el MVP. La mensajería interna es un feature de V2 (aproximadamente Q2 2027).

---

## Contexto

El marketplace necesita un canal de comunicación entre compradores y vendedores. Las opciones son: construir mensajería interna en la plataforma, o usar una plataforma de mensajería existente donde la comunidad ya está.

En Colombia, WhatsApp tiene una penetración de ~90% entre personas con smartphone. La comunidad tuning colombiana usa WhatsApp para todo: grupos de carros, ventas, preguntas técnicas, coordinación de meetups. No es una app que algunos usan — es la app que todos usan.

---

## La Decisión

**MVP:** El botón "Contactar" en el detalle de cada pieza genera un link `wa.me/57XXXXXXXXXX?text=[mensaje pre-formateado]`. El comprador hace clic y WhatsApp se abre en su celular con un mensaje listo. La transacción ocurre completamente por fuera de la plataforma.

**V2 (Q2 2027):** Mensajería interna en la plataforma con inbox consolidado, historial de conversaciones, sistema de ofertas, y integración con el sistema de transacciones mediadas.

---

## Opciones Evaluadas

### Opción A: Mensajería interna desde el MVP
**Pros:** Control total de la experiencia. Datos de transacciones. Posibilidad de cobrar comisión.
**Contras:**
- 2–3 meses adicionales de desarrollo solo para mensajería
- Los usuarios ya tienen WhatsApp — obligarlos a usar otro canal es fricción
- Sin suficientes usuarios, el inbox interno está vacío y parece una plataforma muerta
- Requiere notificaciones push nativas para no perder mensajes

### Opción B — ELEGIDA: WhatsApp externo en MVP
**Pros:**
- Cero desarrollo adicional
- Los usuarios ya saben cómo funciona
- Adopción inmediata
- Permite lanzar el MVP en el timeline de 30 días

**Contras:**
- PITS MARKET no tiene visibilidad de las transacciones
- No se puede cobrar comisión sobre las transacciones
- Los datos de comportamiento post-contacto son limitados

### Opción C: Formulario de contacto interno (sin real-time)
**Pros:** Más simple que mensajería completa.
**Contras:** La comunidad espera WhatsApp. Un formulario de contacto en 2026 es una experiencia pobre.

---

## Por Qué Esta Decisión

WhatsApp es donde la comunidad vive. Forzarlos a usar otro canal en el MVP — cuando la plataforma aún no tiene suficiente inventario ni reputación para justificar aprender algo nuevo — es añadir fricción sin valor.

La mensajería interna tiene su lugar, pero ese lugar es cuando tenemos: suficiente inventario para que el inbox esté activo, suficiente confianza de usuarios para que prefieran el canal propio, y la infraestructura de transacciones mediadas que hace que la mensajería interna tenga sentido de negocio.

El orden correcto es: primero que los compradores y vendedores se encuentren (MVP), luego que la conversación ocurra dentro de la plataforma (V2).

---

## Trade-off Explícito Aceptado

Esta decisión acepta conscientemente que:

1. **No podemos cobrar comisión en el MVP.** Las transacciones ocurren fuera. Esto es correcto para el MVP porque la comisión requiere transacciones mediadas que requieren mensajería interna.

2. **Tenemos visibilidad limitada del post-contacto.** Solo sabemos que el comprador hizo clic en WhatsApp, no si la transacción se completó. Mitigación: encuesta semanal a vendedores con muchos clicks.

3. **El WhatsApp del vendedor queda expuesto.** Mitigación parcial: el número solo se muestra a usuarios registrados, no a visitantes anónimos.

---

## Consecuencias

### Positivas
- Lanzamiento en 30 días (sin el overhead de mensajería interna)
- Adopción natural — los usuarios ya saben cómo funciona WhatsApp
- Cero fricción adicional en el flujo de contacto

### Negativas / Trade-offs
- Sin datos de transacciones completadas
- Sin posibilidad de comisión hasta V2
- Número de WhatsApp del vendedor expuesto a usuarios registrados

### Riesgos

| Riesgo | Probabilidad | Impacto | Mitigación |
|--------|-------------|---------|-----------|
| WhatsApp bloquea el número del admin por comunicaciones masivas | Baja | Alto | Usar WhatsApp Business API para comunicaciones automatizadas del sistema (NO para el contacto comprador-vendedor) |
| Los vendedores cierran por fuera y nunca vuelven a la plataforma | Media | Alto | El sistema de reputación y los planes de visibilidad crean razones para volver |

---

## Criterios de Revisión

```
Revisar si:
- Llegamos a 500 transacciones/semana (la mensajería interna se vuelve necesaria para escalar)
- El 30% de los vendedores pide explícitamente mensajería interna
- Aparece un competidor con mensajería interna y nos quita usuarios por eso
- Timeline de V2 (Q2 2027) — revisión programada
```

---

## Conexiones

**Documentos relacionados:**
- `engineering/architecture/SYSTEM_ARCHITECTURE_v1.md` — APIs internas (sección 14)
- `product/roadmap/` — V2 incluye mensajería interna

---

*Decisión 0003 · ACTIVE · 2026-06-26 · PITS MARKET*
