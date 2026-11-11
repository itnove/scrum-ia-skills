# Scrum e IA para Product Owners: skills para Claude, en español

Nueve skills para el día a día de un Product Owner que trabaja con Scrum. Las instalas una
vez en Claude y, a partir de ahí, Claude sabe hacer estas tareas con método: no hace falta
copiar prompts ni explicarle cada vez cómo quieres el resultado.

Salen de la [Caja de herramientas IA del Product Owner](https://www.itnove.com/recursos/caja-herramientas-ia-po)
y de los cursos de Scrum e IA de [ITNOVE](https://www.itnove.com).

## Qué incluye

| Skill | Qué hace | Pídelo así |
|---|---|---|
| `contexto-de-producto` | Crea el documento de contexto de tu producto (Product Goal con su métrica, personas, Definición de Hecho, glosario, restricciones). Lo usan todas las demás. | "Ponte en contexto de mi producto con estas notas" |
| `resumir-entrevista` | Resume una entrevista sin perder la voz del cliente: problemas con citas literales, alternativas actuales, lo que se ha supuesto y preguntas para la siguiente. | "¿Qué ha dicho en esta entrevista?" |
| `historias-y-criterios` | Divide una épica en historias pequeñas y verticales con el chequeo INVEST, y escribe criterios Dado / Cuando / Entonces con casos límite. | "Prepárame esto para el refinamiento" |
| `priorizar-backlog` | Prioriza frente al Product Goal con valor, esfuerzo y el supuesto de cada estimación a la vista. | "¿Qué hacemos primero?" |
| `preparar-sprint-review` | Prepara la Sprint Review como conversación para decidir, no como informe de estado. | "El viernes tengo la review, estos son los datos" |
| `acta-de-decisiones` | Saca de una reunión las decisiones, las acciones con responsable y fecha, y lo que quedó abierto, sin añadir nada que no se dijera. | "Hazme el acta de esta reunión" |
| `product-goal` | Propone o revisa el Product Goal a partir de la visión, con una métrica de resultado y tres metas intermedias. | "¿Está bien nuestro Product Goal?" |
| `okr-de-producto` | Escribe o revisa los OKR del equipo (resultados, no actividad; de 2 a 4 resultados clave) y prepara los check-ins. | "Revisa los OKR del trimestre" |
| `flujo-kanban` | Analiza el tablero con métricas de flujo, encuentra el atasco y propone experimentos pequeños, sin señalar a nadie. | "Vamos lentos, ¿por qué?" |

No hace falta nombrar la skill: Claude elige la que toca según lo que pidas.

## Cómo instalarlo

**En Claude (Cowork o la app de escritorio):** Personalizar → Explorar plugins → Personal →
**+** → Añadir marketplace desde GitHub → `itnove/scrum-ia-skills`.

**En Claude Code:**

```bash
claude plugin marketplace add itnove/scrum-ia-skills
claude plugin install scrum-ia-po@scrum-ia
```

**Otros asistentes que leen carpetas `SKILL.md`:** `npx skills add itnove/scrum-ia-skills`.

En [`ejemplos/`](ejemplos/) tienes nueve casos con un producto ficticio y lo que respondió
Claude en cada uno.

## Cómo sacarle partido

1. **Empieza por el contexto.** Pásale a Claude tus notas, el roadmap o la presentación del
   producto y pídele el documento de contexto. Guárdalo como `contexto-producto.md` en tu
   proyecto: las demás skills lo leen solas.
2. **Elige una tarea que hagas cada semana** (resumir entrevistas, preparar el refinamiento,
   la review) y úsala durante dos o tres semanas antes de añadir otra.
3. **Si tienes Claude conectado a Jira u otra herramienta**, las skills pueden leer de ahí.
   No cambian nada en tus herramientas sin enseñártelo antes y que digas que sí.

## Lo que estas skills no hacen

- **No deciden por ti.** Proponen, ordenan y señalan lo dudoso; la decisión sigue siendo del
  Product Owner y del equipo.
- **No inventan.** Si falta un dato, lo marcan como pendiente y te hacen la pregunta.
- **No sustituyen la conversación con el equipo.** Llegas al refinamiento o a la review con
  algo mejor preparado, pero la conversación hay que tenerla.

## Para tu equipo o tu empresa

Si queréis adaptar estas skills a vuestro producto y a vuestra forma de trabajar, lo hacemos
en un taller con vuestro equipo: [formación para empresas](https://www.itnove.com/ia-para-empresas).

## Licencia

MIT. Úsalas, cámbialas y compártelas.
