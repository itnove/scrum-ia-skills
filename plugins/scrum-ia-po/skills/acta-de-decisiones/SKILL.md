---
name: acta-de-decisiones
description: Convierte la transcripción o las notas de una reunión (refinamiento, review, retrospectiva, comité, reunión con stakeholders) en un acta útil: decisiones con quién decidió, acciones con responsable y fecha, temas abiertos y desacuerdos o riesgos, sin añadir nada que no se dijera. Usar cuando el Product Owner pegue o adjunte una transcripción o notas y pida "acta", "resumen de la reunión", "qué se decidió", "acciones y responsables" o similar.
---

# Acta con decisiones, acciones y responsables

Una reunión sin decisiones escritas se repite. Esta skill saca lo que se decidió y
quién hace qué, y deja a la vista lo que quedó sin decidir.

## Qué devolver

1. **Decisiones tomadas**: qué se decidió y **quién decidió** (o "por consenso" si fue así).
   Solo lo que se decidió de verdad, no lo que se comentó.
2. **Acciones**: qué, quién y para cuándo, en una tabla. Si una acción no tiene
   responsable o fecha, márcala con **SIN RESPONSABLE** o **SIN FECHA** en lugar de
   rellenarlo.
3. **Temas abiertos**: lo que se habló sin llegar a decisión, con lo que haría falta para
   decidirlo (un dato, una persona, una fecha).
4. **Desacuerdos y riesgos mencionados**: quién lo planteó (por rol si no conviene el
   nombre) y en qué consiste.
5. **Para el Product Backlog** (solo si la reunión es de producto): elementos que habría
   que crear, cambiar o quitar. Como propuesta: no los toques en la herramienta sin un sí
   explícito.

Añade al final un **mensaje de seguimiento** listo para enviar al equipo (5 líneas como
máximo: decisiones y acciones con responsable).

## Reglas

- **No añadas nada que no se dijera.** Ni acciones "recomendables", ni conclusiones
  propias. Si algo es ambiguo, recógelo como tema abierto.
- **El mensaje de seguimiento solo repite el acta.** No le pongas fechas, plazos ni
  compromisos más concretos que los que se dijeron ("lo hablamos otro día" no es "en la
  próxima reunión"). Si conviene concretarlo, sugiérelo aparte al Product Owner.
- Si la transcripción tiene errores de reconocimiento de voz, no adivines nombres o
  cifras: márcalos con `[?]`.
- Respeta la confidencialidad: si aparecen datos personales o información sensible que
  no hace falta para las acciones, déjalos fuera.
