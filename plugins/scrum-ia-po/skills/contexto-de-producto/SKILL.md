---
name: contexto-de-producto
description: Crea o actualiza el documento de contexto de un producto (para quién es, Product Goal con su métrica, personas, Definición de Hecho, glosario y restricciones) a partir de notas sueltas, un roadmap o una presentación. Usar cuando el Product Owner diga "crea el contexto de mi producto", "documento de contexto", "ponte en contexto de mi producto", "resume mi producto en una página", o antes de cualquier otra tarea de producto si no existe todavía un contexto-producto.md.
---

# Documento de contexto del producto

Es la base de todo lo demás: con él, el resto de skills (entrevistas, historias,
priorización, Sprint Review) hablan del producto del usuario y no dan respuestas genéricas.

## Antes de empezar

1. Busca si ya existe `contexto-producto.md` en la carpeta de trabajo o en el proyecto.
   Si existe, léelo y trabaja sobre él (actualizar, no empezar de cero).
2. Si el usuario no ha dado material, pídele lo que tenga a mano: notas, el último
   roadmap, la presentación del producto, la web o una conversación con su equipo.
   Con una sola fuente basta para empezar.

## Qué escribir

Una página, con estas secciones y en este orden:

1. **Producto y para quién es**: qué problema resuelve y a quién, en 3 o 4 frases.
2. **Product Goal actual**: el objetivo de los próximos meses con **su métrica** (valor
   de partida y objetivo). Si no hay métrica, dilo.
3. **Personas principales**: 2 o 3, escritas como **hipótesis** (qué creemos y qué
   evidencia hay), no como verdades.
4. **Definición de Hecho**: la del equipo, tal cual.
5. **Glosario**: los términos del negocio que alguien de fuera no entendería.
6. **Restricciones**: legales (datos personales, sector regulado, AI Act), técnicas y de marca.
7. **Pendiente**: la lista de preguntas abiertas (ver la regla de abajo).

## Reglas

- **No inventes.** Si falta información para una sección, escribe `PENDIENTE` y una
  pregunta concreta que el Product Owner deba responder. Es mejor un hueco visible que
  un dato falso que luego usarán las demás skills.
- Usa las palabras del usuario y de su negocio, no jerga genérica.
- Separa lo que es un hecho (con su fuente) de lo que es una suposición.
- Nada de datos personales de clientes concretos: si aparecen en las notas, resúmelos
  sin nombres.

## Al terminar

- Guarda el resultado como `contexto-producto.md` (si el entorno lo permite) y dile al
  usuario dónde está.
- Termina con las preguntas de la sección Pendiente, ordenadas por cuánto bloquean.
- Sugiere el siguiente paso más útil según lo que falte: por ejemplo, si no hay métrica
  del Product Goal, empezar por ahí; si hay entrevistas recientes, resumirlas con la
  skill `resumir-entrevista`.
