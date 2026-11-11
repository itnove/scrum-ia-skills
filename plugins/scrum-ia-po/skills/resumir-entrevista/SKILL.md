---
name: resumir-entrevista
description: Resume una entrevista con un cliente o usuario sin perder su voz (problemas con citas literales, alternativas actuales, supuestos sin confirmar y preguntas para la siguiente conversación), sin proponer soluciones. Usar cuando el Product Owner pegue o adjunte la transcripción o las notas de una entrevista, una llamada de discovery o un test con usuarios y pida "resúmela", "qué ha dicho", "saca los insights" o similar.
---

# Resumir una entrevista sin perder la voz del cliente

El riesgo de resumir con IA es quedarse con lo que el Product Owner quería oír. Esta
skill protege lo contrario: lo que el cliente dijo, con sus palabras.

## Antes de empezar

- Si existe `contexto-producto.md`, léelo para entender el producto y sus personas.
- Necesitas la transcripción o las notas. Si solo hay un resumen hecho por otra
  persona, avisa: las citas no serán literales.

## Qué devolver

1. **Contexto del cliente**: rol, empresa o situación, en 2 líneas. Sin nombre propio.
2. **Problemas que menciona**: cada uno con **una cita literal entre comillas**. Si un
   problema no tiene cita (lo dedujiste tú), no va aquí: va en el punto 4.
3. **Lo que hace hoy para resolverlo**: alternativas actuales, herramientas, apaños.
   Incluye cuánto le cuesta (tiempo, dinero, molestia) si lo dijo.
4. **Lo que se ha supuesto y el cliente no ha confirmado**: preguntas inductoras del
   entrevistador, conclusiones que no salen de sus palabras.
5. **Tres preguntas para la siguiente conversación**: abiertas, sobre hechos pasados
   ("cuéntame la última vez que…"), no sobre opiniones del futuro.
6. **Encaje con las personas del contexto** (solo si existe `contexto-producto.md`):
   qué hipótesis de persona refuerza, cuál contradice y cuál no toca.

## Reglas

- **No incluyas soluciones ni recomendaciones de producto.** Si el cliente propone una
  solución, recógela como cita en el punto 2 y busca el problema que hay detrás.
- No suavices las quejas ni exageres los elogios: mantén el tono del cliente.
- Si hay varias entrevistas, resume cada una por separado y añade al final una tabla de
  problemas repetidos (cuántas veces y en qué entrevistas).
- Quita nombres, correos y datos que identifiquen a la persona.
