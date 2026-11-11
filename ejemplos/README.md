# Ejemplos

Casos con un producto ficticio, **GymApp** (la app de una cadena de gimnasios), y lo que
respondió Claude con estas skills instaladas. Sirven para ver qué esperar de cada una.

Las peticiones no nombran la skill: Claude elige la que toca según lo que pides. Los casos
02 a 09 se lanzaron con el `contexto-producto.md` que generó el caso 01, para mostrar cómo lo
usan las demás.

| Caso | Petición | Skill | Resultado |
|---|---|---|---|
| 01 | [Notas sueltas del producto](01-contexto.md) | contexto-de-producto | [Documento de contexto](resultados/01-contexto-producto.md) |
| 02 | [Transcripción de una entrevista](02-entrevista.md) | resumir-entrevista | [Resumen](resultados/02-entrevista.md) |
| 03 | [Épica para el refinamiento](03-epica.md) | historias-y-criterios | [Respuesta](resultados/03-epica.md) y [documento de refinamiento](resultados/03-refinamiento-lista-de-espera.md) |
| 04 | [Backlog y feedback](04-backlog.md) | priorizar-backlog | [Priorización](resultados/04-backlog.md) |
| 05 | [Datos del Sprint](05-sprint.md) | preparar-sprint-review | [Sprint Review](resultados/05-sprint.md) |
| 06 | [Transcripción de una reunión](06-reunion.md) | acta-de-decisiones | [Acta](resultados/06-reunion.md) |
| 07 | [Un Product Goal para revisar](07-product-goal.md) | product-goal | [Revisión](resultados/07-product-goal.md) |
| 08 | [OKR para revisar](08-okr.md) | okr-de-producto | [Revisión](resultados/08-okr.md) |
| 09 | [Exportación de un tablero](09-kanban.md) ([CSV](09-kanban.csv)) | flujo-kanban | [Análisis del flujo](resultados/09-kanban.md) |

Para repetir un caso con Claude Code desde la carpeta del repo:

```bash
claude -p --plugin-dir plugins/scrum-ia-po "$(cat ejemplos/04-backlog.md)"
```

Las respuestas de un modelo de IA varían de una vez a otra: lo importante es el método que
siguen, no la redacción exacta.
