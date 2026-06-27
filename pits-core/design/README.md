# /design — Sistema de Diseño PITS MARKET

## Propósito

La fuente de verdad del lenguaje visual y de interacción de PITS MARKET. Esta carpeta define cómo se ve, cómo se comporta, y cómo comunica confianza el producto en cada pantalla y cada estado.

> **Principio de diseño:** PITS MARKET no imita. Tiene una estética propia: oscura, técnica, callejera pero precisa. NFS Underground meets Bloomberg Terminal para carros colombianos.

---

## Subcarpetas

| Carpeta | Contenido | Quién lo usa |
|---------|-----------|-------------|
| `/system` | Design system completo, tokens, principios | Devs + Diseñadores |
| `/components` | Especificaciones de componentes UI reutilizables | Devs + Diseñadores |
| `/colors` | Paleta completa con todos los usos y contextos | Devs + Diseñadores |
| `/typography` | Sistema tipográfico: fuentes, tamaños, jerarquía | Devs + Diseñadores |
| `/icons` | Sistema de iconografía: qué íconos, cuándo, cómo | Devs + Diseñadores |
| `/trust-ui` | Componentes específicos de confianza y reputación | Devs + Product |

---

## Los 5 Principios de Diseño de PITS MARKET

### 1. Mobile-First Sin Excepción
El 85% de los usuarios llegan desde el celular. Primero se diseña para 375px (iPhone SE) y se escala hacia arriba. No al revés. Un feature que no funciona perfectamente en mobile no está listo.

### 2. La Confianza Se Diseña, No Se Asume
En un marketplace de segunda mano, el diseño visual transmite (o no transmite) confianza antes de que el usuario lea una sola palabra. Los colores, la tipografía, la forma de mostrar el rating de un vendedor, el estado de una pieza — todo eso comunica confianza o genera duda.

### 3. La Velocidad Percibida Es Producto
El skeleton loading, el blur placeholder de imágenes, los optimistic updates — no son detalles técnicos. Son la diferencia entre "esta plataforma es rápida" y "esta plataforma me hace esperar". El diseño de los estados de carga es tan importante como el diseño de los estados llenos.

### 4. El Lenguaje Técnico Como Identidad
Mostrar "EA113" y "N55B30" en la interfaz no es jerga — es el lenguaje que habla la comunidad. El diseño abraza la terminología técnica automotriz porque es lo que nos diferencia de un marketplace genérico. La tipografía Share Tech Mono para códigos técnicos no es decorativa — es identidad.

### 5. Dark Mode Como Default
La estética de PITS MARKET es oscura. No como elección de moda — como elección de identidad. Negro profundo `#0A0A0A` + verde neón `#AAFF00` es la firma visual de la plataforma. El dark mode no es una feature, es la experiencia base.

---

## Stack de Diseño

| Herramienta | Uso | Dónde vive |
|-------------|-----|-----------|
| Figma | UI/UX design, prototipos | Figma Cloud (link en `/design/system/`) |
| Tailwind CSS | Implementación de estilos | Código de la app |
| Shadcn/UI | Componentes base accesibles | Código de la app |
| Lucide Icons | Iconografía principal | Código de la app |

---

*Propietario: Head of Design / CTO · Revisión: Por versión mayor del producto*
