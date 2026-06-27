# Decision Doctrine — Cómo Tomamos Decisiones en PITS MARKET

> Este documento no es el único framework de decisiones (ver también `founder-os/decision-framework.md`). Es la doctrina: los principios de alto nivel que gobiernan cómo se toman decisiones en todos los niveles y en toda la empresa.

---

## El Problema que Resuelve Este Documento

Las empresas sin doctrina de decisiones operan con inconsistencia creciente: cada persona decide según su criterio individual, el equipo no tiene contexto compartido, y las decisiones se revierten cuando cambia quien las tomó. La doctrina elimina eso al establecer **cómo** se decide, no solo **qué** se decide.

---

## Principio 1: Las Decisiones Tienen Dueño

Toda decisión tiene exactamente una persona que la toma. No un comité. No un consenso. Una persona que es responsable del outcome.

**Cómo funciona:**
- El dueño de la decisión consulta a quien quiera consultar
- El dueño de la decisión escucha todos los inputs
- El dueño de la decisión decide
- El dueño de la decisión es responsable del resultado

Los comités deciden lento y nadie es responsable del resultado. PITS MARKET no tiene comités.

**Tabla de ownership:**

| Área | Dueño | Puede consultar a |
|------|-------|-------------------|
| Decisiones de producto (qué construir) | Fundador | CTO, usuarios, equipo |
| Decisiones técnicas de arquitectura | CTO | Fundador, equipo técnico |
| Decisiones de pricing | Fundador | Head of Growth, datos de mercado |
| Decisiones de contratación | Fundador | Quien trabajará con la persona |
| Decisiones de contenido | Head of Content | Fundador, comunidad |
| Decisiones de emergencia técnica | CTO on-call | Nadie — actuar, comunicar después |

---

## Principio 2: Tipo 1 vs Tipo 2

Toda decisión es Tipo 1 o Tipo 2. La tragedia más común es tratar decisiones Tipo 2 como Tipo 1.

**Tipo 1 — Irreversible o muy costosa de revertir:**
- Contratar a alguien
- Elegir el stack tecnológico principal
- Definir el modelo de monetización
- Cambiar los Términos de Servicio fundamentales
- Comprometer recursos por más de 3 meses

*Proceso:* Lento. Análisis. Documentar en `/decisions`. Esperar 48h antes de ejecutar.

**Tipo 2 — Reversible con costo razonable:**
- Cambiar el copy de un botón
- Probar un nuevo canal de contenido
- Agregar un filtro en el marketplace
- Cambiar el horario de moderación

*Proceso:* Rápido. Ejecutar. Medir. Ajustar. No documentar formalmente.

**La trampa:** Tratar decisiones Tipo 2 como Tipo 1 ralentiza todo. Tratar decisiones Tipo 1 como Tipo 2 crea deuda imposible de pagar.

---

## Principio 3: Disagree and Commit

Cuando se ha tomado una decisión, el equipo la ejecuta con convicción — aunque haya estado en desacuerdo en el proceso.

**Cómo funciona:**
1. Durante el proceso: Expresa tu desacuerdo con claridad y argumentos
2. Una vez decidido: Ejecuta con el mismo esfuerzo que si fuera tu propia decisión
3. Después de ejecutar: Si los datos muestran que estabas en lo correcto, lo revisamos

Lo que NO es aceptable: ejecutar a medias porque no estás de acuerdo, o sabotear pasivamente una decisión con la que no estás de acuerdo.

---

## Principio 4: La Velocidad de la Decisión como Métrica

Las decisiones lentas tienen un costo. Ese costo es invisible porque no aparece en ningún reporte, pero es real: oportunidades que se pierden, momentum que se pierde, talento que se aburre esperando claridad.

**Standards de velocidad:**

| Tipo de decisión | Tiempo máximo para decidir |
|-----------------|--------------------------|
| Decisión operacional del día | 2 horas |
| Decisión de producto (feature dentro del sprint) | 24 horas |
| Decisión técnica de arquitectura media | 3 días |
| Decisión de negocio mayor (Tipo 1) | 7 días |
| Decisión de Constitución / Valores | 30 días |

Si una decisión no puede tomarse en ese tiempo, hay un problema de información, no de tiempo. Identificar qué información falta y buscarla activamente.

---

## Principio 5: Documentar las Decisiones Importantes

Las decisiones que importan se documentan en `/decisions`. Las razones:

1. El equipo futuro no tiene que re-inventar la rueda
2. Se pueden evaluar retrospectivamente cuando los resultados llegan
3. El proceso de escribir la decisión la clarifica
4. Crea accountability real

**¿Qué es "importante"?** Una heurística: si esta decisión costara más de 3 días-persona revertir, o si afecta a más de 10 usuarios, va en `/decisions`.

---

## Principio 6: Los Datos Ganan, Las Opiniones Compiten

Cuando hay datos disponibles, los datos ganan. Cuando no hay datos, las opiniones competen en igualdad de condiciones — independientemente del cargo de quien las tiene.

Un practicante con datos correctos tiene más peso en una decisión que el CEO con una opinión. Eso requiere:
- Que los datos sean accesibles para todos (no solo para leadership)
- Que sea seguro presentar datos que contradicen la posición del fundador
- Que las decisiones basadas en datos malos se reconozcan como tales, incluso si las tomó el fundador

---

## Apéndice: Decisiones que NUNCA se Delegan del Fundador

Estas decisiones permanecen con el Fundador independientemente del tamaño del equipo:

1. La visión y dirección estratégica de largo plazo
2. Las primeras 10 contrataciones
3. Cambios a la Constitución (principios, valores, filosofía)
4. El modelo de monetización fundamental
5. Relaciones con inversionistas y términos de inversión
6. Decisiones que afecten la reputación pública de la empresa

---

*Versión 1.0 — Junio 2026 · PITS MARKET*
