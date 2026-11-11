He leído el contexto de GymApp y he dejado la épica dividida en seis historias, con criterios en Dado / Cuando / Entonces, chequeo INVEST y orden de entrega. Es una propuesta para discutir con el equipo, no un backlog cerrado.

Lo que más pesa para el jueves:

- **Relación con el Product Goal sin demostrar.** La lista de espera solo ayuda a activar socios nuevos si estos se encuentran clases llenas, y eso no consta en el contexto. Conviene llevar cuántas clases se llenan, cuántas cancelaciones hay en ellas y cuántos socios nuevos intentan reservarlas.
- **Asignación automática o con confirmación.** He leído "la plaza se le asigna" como automática, pero es un supuesto mío y de él depende toda la historia 2, que no se puede estimar hasta decidirlo.
- **Bono.** Con asignación automática, al socio se le podría descontar una clase del bono sin que haga nada. Hay que decidir cuándo se descuenta.
- **Corte antes del inicio.** Si alguien cancela diez minutos antes, falta decidir si se asigna la plaza.
- **Orden de la lista.** He supuesto orden de inscripción. Dar prioridad al socio nuevo es lo único que conectaría la épica directamente con el Product Goal.

| # | Historia | Reserva principal |
|---|---|---|
| H1 | Apuntarme a la lista de una clase llena | Sola no da plaza; sirve para medir demanda |
| H2 | Recibir la plaza cuando alguien cancela | La más grande; depende de H1 y de la decisión sobre asignación |
| H3 | Salir de la lista | Imprescindible para publicar si la asignación es automática |
| H4 | Ver mis listas y mi posición | Valor pequeño; se puede fusionar con H1 |
| H5 | Enterarme si la clase se cancela o cambia | Depende de H1 y H2 |
| H6 | Monitor ve la lista de sus clases | Hipótesis mía: la épica no menciona al monitor |

El orden propuesto es H1, H2, H3, H5, H4, H6. H1 ya se puede enseñar a un socio real; lo mínimo para publicar es H1 + H2 + H3.

He dejado sin escribir "recepción apunta a un socio" y "prioridad para socios nuevos", porque dependen de preguntas abiertas. El documento recoge nueve preguntas de negocio en total, y la Definición de Hecho sigue pendiente en el contexto.


Documento: `refinamiento-lista-de-espera.md`