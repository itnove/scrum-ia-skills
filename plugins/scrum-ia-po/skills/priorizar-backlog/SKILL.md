---
name: priorizar-backlog
description: Prioriza elementos del Product Backlog frente al Product Goal estimando valor y esfuerzo con el supuesto de cada estimación a la vista, y los agrupa en hacer ahora, siguiente, más adelante y no hacer, marcando lo más dudoso para revisarlo con el equipo. Usar cuando el Product Owner pida "prioriza el backlog", "qué hacemos primero", "ordena estas ideas", "qué entra en el próximo Sprint" o pegue una lista de elementos para ordenar.
---

# Priorizar el backlog con los supuestos a la vista

Una puntuación sin su supuesto es una opinión con decimales. Esta skill obliga a
escribir por qué se estima cada cosa, para que el equipo discuta los supuestos y no los
números.

## Antes de empezar

- Necesitas el **Product Goal**. Búscalo en `contexto-producto.md`; si no existe, pídelo.
  Sin Product Goal no hay forma honesta de priorizar: dilo y propón definirlo primero.
- Necesitas la lista de elementos (pegada, en un fichero o leída de Jira u otra
  herramienta mediante un conector). **No cambies el orden ni el estado** en la
  herramienta: devuelve la propuesta y deja que el Product Owner decida.

## Qué devolver

1. **Tabla ordenada** con: elemento, valor (1-5), esfuerzo (1-5), y **el supuesto detrás
   de cada estimación en una línea** ("valor 4 porque 34 % del feedback habla de
   reservas", "esfuerzo 2 si reutilizamos el aviso de pago").
2. **Grupos**: hacer ahora · siguiente · más adelante · no hacer. Para "no hacer", di por
   qué (no acerca al Product Goal, duplica otro, coste desproporcionado).
3. **Estimaciones dudosas**: marca las 2 o 3 que más cambiarían el orden si estuvieran
   mal, y qué dato las aclararía (una métrica, una pregunta al equipo, un experimento).
4. **Riesgos y dependencias** que alteren el orden (un elemento que desbloquea a otros,
   una fecha legal, algo que solo sabe una persona).

## Reglas

- **El valor se mide contra el Product Goal**, no en abstracto. Si un elemento no ayuda
  al objetivo, su valor es bajo aunque sea "importante".
- El esfuerzo lo estima el equipo de desarrollo: tu cifra es un **borrador** para la
  conversación y lo dices así.
- Si los datos de valor vienen de una fuente (feedback, analítica), cítala. Si es
  intuición, escríbelo.
- Si el usuario pide otro método (WSJF, RICE, MoSCoW, Kano), úsalo, pero mantén la
  columna de supuestos.
