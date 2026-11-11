---
name: flujo-kanban
description: Analiza el flujo de trabajo de un equipo a partir de su tablero o de una exportación (Jira, Trello, un CSV) con métricas de flujo (trabajo en curso, tiempo de ciclo, rendimiento y antigüedad de los elementos), encuentra cuellos de botella y propone experimentos pequeños para mejorar, sin señalar a personas. Usar cuando el Product Owner o el equipo digan "¿por qué vamos tan lentos?", "analiza nuestro tablero", "métricas de flujo", "revisa el Kanban", "qué está atascado" o compartan una exportación del tablero.
---

# Analizar el flujo con Kanban

Casi siempre el trabajo no va lento porque la gente trabaje poco, sino porque hay
demasiadas cosas empezadas a la vez y esperando. Esta skill pone números a eso y propone
cambios pequeños para probar.

## Antes de empezar

- Necesitas el tablero o una exportación con, como mínimo: elemento, estado actual y
  fechas de entrada en cada estado (o al menos de inicio y fin). Si viene de Jira u otra
  herramienta mediante un conector, **solo lee**: no muevas tarjetas ni cambies estados.
- Pregunta qué cuenta como **empezado** y como **terminado** en su tablero si no está claro:
  cambia todas las cifras.

## Qué calcular

1. **Trabajo en curso (WIP)** por columna y total, y el límite si lo tienen.
2. **Tiempo de ciclo** de lo terminado: mediana y percentil 85 (más útil que la media, que
   la deforman unos pocos casos).
3. **Rendimiento**: elementos terminados por semana.
4. **Antigüedad** de lo que está en curso: los elementos que llevan más tiempo que el
   percentil 85 del tiempo de ciclo son los que hay que mirar hoy.
5. **Dónde esperan**: columnas de espera (revisión, pruebas, "bloqueado") y cuánto tiempo
   pasa ahí el trabajo frente al tiempo en que alguien trabaja en él.

Si los datos lo permiten, comprueba la **Ley de Little** (tiempo de ciclo medio ≈ WIP medio /
rendimiento) para explicar por qué bajar el WIP acorta los plazos.

## Qué devolver

- Un **resumen en 3 frases**: cómo fluye el trabajo y dónde está el atasco principal.
- La **tabla de métricas** de arriba, con las cifras y de dónde salen.
- **Los elementos envejecidos** que conviene desatascar ya.
- **2 o 3 experimentos pequeños** (bajar el límite de WIP de una columna, dejar de empezar
  y ponerse a terminar, revisar a diario lo bloqueado), cada uno con la métrica que
  diría si funciona y en cuántas semanas mirarla.
- Si el equipo hace Scrum: qué significa para la previsión del próximo Sprint.

## Reglas

- **Nada de señalar personas.** Se analiza el sistema de trabajo, no a quién tiene más
  tarjetas.
- No inventes fechas que falten: di cuántos elementos se han quedado fuera del cálculo.
- Pocos datos (menos de 15 elementos terminados) dan cifras poco fiables: dilo.
