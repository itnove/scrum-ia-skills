# Refinamiento: lista de espera para clases llenas

Propuesta para discutir con el equipo, basada en la épica y en `contexto-producto.md`.

**Épica:** cuando una clase está llena, el socio se puede apuntar a una lista de espera
y, si alguien cancela, la plaza se le asigna y se le avisa.

## Antes de entrar en las historias

**Relación con el Product Goal sin demostrar.** El objetivo es que los socios nuevos
lleguen a 3 visitas en sus primeros 30 días (40 % → 65 %). La épica solo ayuda si los
socios nuevos se encuentran clases llenas, y eso no lo sabemos. Tres datos lo aclararían:

- cuántas clases se llenan a la semana, y en qué gimnasios y franjas;
- cuántas cancelaciones hay en clases llenas (si casi nadie cancela, la lista no reparte plazas);
- cuántos socios nuevos intentan reservar una clase llena.

**Dos supuestos míos que la épica no dice:**

1. La lista va por orden de inscripción.
2. La asignación es automática, sin que el socio confirme. Lo leo así en "la plaza se le
   asigna", pero tiene consecuencias (ver preguntas 1 y 2).

## Preguntas de negocio que deciden el diseño

Los criterios marcados con `?` más abajo dependen de ellas.

| # | Pregunta | Por qué importa |
|---|---|---|
| 1 | ¿Asignación automática, o se ofrece la plaza y el socio confirma en un plazo? | Cambia la historia 2 entera. La automática es más simple, pero puede dar plazas a quien ya no puede ir. |
| 2 | Si el socio paga con **bono**, ¿cuándo se descuenta la clase: al apuntarse a la lista, al asignarle la plaza o al asistir? | Con asignación automática se le gastaría una clase del bono sin que haga nada. |
| 3 | ¿Hasta cuánto antes del inicio se asignan plazas? Si alguien cancela 10 minutos antes, ¿se asigna? | Sin un corte, el socio recibe una plaza a la que no llega. |
| 4 | ¿Qué pasa si al socio le asignan la plaza y no va, o la cancela tarde? ¿Hay hoy penalización por no presentarse? | Si la hay, ¿aplica igual a una plaza que no eligió en ese momento? |
| 5 | ¿Por qué canal se avisa (notificación de la app, correo, SMS)? ¿Y si el socio tiene las notificaciones desactivadas? | Sin aviso, la asignación no sirve. |
| 6 | ¿Tiene límite la lista? ¿Puede un socio estar en varias listas, incluso de clases a la misma hora? | Define los casos límite de la historia 1. |
| 7 | ¿Orden de inscripción para todos, o prioridad para el socio nuevo? | Es lo único que conectaría la épica directamente con el Product Goal. |
| 8 | ¿Puede recepción apuntar a un socio a la lista en su nombre? | En el contexto sigue pendiente para qué usa la app recepción. |
| 9 | ¿Ve el monitor hoy datos de salud (lesiones) de los asistentes? ¿Los vería también de quien está en lista de espera? | Son datos de categoría especial en el RGPD: enseñarlos de alguien que quizá no asista es un uso nuevo. |

## Historias

Leyenda INVEST: ✔ pasa · ⚠ con reservas · ✘ falla.

### H1. Apuntarme a la lista de espera de una clase llena

**Como** socio, **quiero** apuntarme a la lista de espera de una clase que está llena,
**para** tener opción a una plaza sin estar entrando a mirar si alguien ha cancelado.

- **Dado** que una clase no tiene plazas libres, **cuando** el socio la consulta,
  **entonces** puede apuntarse a la lista de espera y ve qué posición ocupa.
- **Dado** que el socio ya está en la lista o ya tiene plaza en esa clase, **cuando**
  intenta apuntarse, **entonces** no se le añade otra vez y se le muestra su situación.
- **Dado** que la clase tiene plazas libres, **cuando** el socio la consulta,
  **entonces** reserva con normalidad y no se le ofrece la lista.
- `?` Lista con límite alcanzado, y listas de dos clases a la misma hora (pregunta 6).
- `?` Socio sin bono ni cuota válidos: ¿puede apuntarse? (pregunta 2).

| I | N | V | E | S | T |
|---|---|---|---|---|---|
| ✔ | ✔ | ⚠ | ⚠ | ✔ | ✔ |

- **V:** sola no da ninguna plaza; su valor por separado es medir cuánta gente se apunta.
- **E:** estimable cuando se respondan las preguntas 2 y 6.

### H2. Recibir la plaza cuando alguien cancela

**Como** socio en lista de espera, **quiero** que se me asigne la plaza que queda libre
y que se me avise, **para** poder ir a la clase sin estar pendiente de la app.

- **Dado** que hay socios en la lista, **cuando** un socio con plaza cancela,
  **entonces** la plaza pasa al primero de la lista, que sale de ella, y los demás suben
  una posición.
- **Dado** que se le ha asignado la plaza, **entonces** el socio recibe un aviso con la
  clase, el día y la hora, y la clase aparece entre sus reservas.
- **Dado** que la lista está vacía, **cuando** alguien cancela, **entonces** la plaza
  queda libre para reservar con normalidad.
- **Dado** que dos socios cancelan casi a la vez, **entonces** los dos primeros de la
  lista reciben una plaza cada uno y nadie recibe dos.
- `?` Cancelación poco antes del inicio (pregunta 3).
- `?` El aviso no se puede entregar: ¿se mantiene la plaza o pasa al siguiente? (pregunta 5).
- `?` Descuento del bono al asignar (pregunta 2).

| I | N | V | E | S | T |
|---|---|---|---|---|---|
| ✘ | ✔ | ✔ | ✘ | ⚠ | ✔ |

- **I:** necesita H1.
- **E:** no se puede estimar hasta decidir la pregunta 1 (automática o con confirmación).
- **S:** es la más grande. Si no cabe, dividir en "asignar y avisar por un solo canal" y
  "resto de canales", no en "asignar" y "avisar": una plaza asignada sin aviso no vale nada.

### H3. Salir de la lista de espera

**Como** socio en lista de espera, **quiero** poder salir de la lista, **para** que no
se me asigne una plaza que ya no quiero.

- **Dado** que el socio está en la lista, **cuando** sale, **entonces** deja de estar en
  ella y los que iban detrás suben una posición.
- **Dado** que el socio ha salido, **cuando** se libera una plaza, **entonces** ni se le
  asigna ni se le avisa.
- **Permisos:** un socio solo puede salir él mismo; no puede ver ni quitar a otros socios
  de la lista.

| I | N | V | E | S | T |
|---|---|---|---|---|---|
| ⚠ | ✔ | ✔ | ✔ | ✔ | ✔ |

- **I:** necesita H1. Con asignación automática es imprescindible para publicar: sin ella
  el socio no puede evitar una plaza que no quiere.

### H4. Ver mis listas de espera y mi posición

**Como** socio, **quiero** ver en qué listas de espera estoy y en qué posición,
**para** decidir si sigo esperando o busco otra clase.

- **Dado** que el socio está en una o varias listas, **cuando** consulta sus reservas,
  **entonces** ve cada clase con su posición actual.
- **Dado** que alguien que iba delante sale o recibe plaza, **entonces** la posición que
  ve el socio está actualizada.
- **Dado** que la clase ya ha empezado, **entonces** deja de aparecer entre sus listas.
- **Permisos:** el socio ve su posición, no quiénes son los demás.

| I | N | V | E | S | T |
|---|---|---|---|---|---|
| ⚠ | ✔ | ⚠ | ✔ | ✔ | ✔ |

- **V:** valor pequeño. Candidata a ir después o a fusionarse con H1 si el equipo la ve trivial.

### H5. Enterarme si la clase que espero se cancela o cambia

**Como** socio en lista de espera, **quiero** que se me avise si la clase se cancela o
cambia, **para** no seguir esperando una plaza que no va a existir.

- **Dado** que la clase se cancela, **entonces** la lista se cierra y se avisa a todos
  los que estaban en ella.
- **Dado** que se amplían las plazas de la clase, **entonces** las nuevas se asignan por
  orden de lista igual que en H2.
- `?` Cambio de hora o de monitor: ¿el socio sigue en la lista o hay que volver a apuntarse?

| I | N | V | E | S | T |
|---|---|---|---|---|---|
| ✘ | ✔ | ✔ | ⚠ | ✔ | ✔ |

- **I:** necesita H1 y H2.
- **E:** depende de qué hace hoy la app con los socios que sí tienen plaza cuando la
  clase cambia.

### H6. Ver la lista de espera de mis clases (monitor)

**Como** monitor, **quiero** ver cuántos socios hay en la lista de espera de mis clases
y quiénes son, **para** conocer la demanda real de cada clase.

- **Dado** que una clase tiene lista, **cuando** el monitor la consulta, **entonces** ve
  a los socios en orden.
- **Dado** que a un socio se le asigna plaza, **entonces** aparece entre los asistentes
  y ya no en la lista.
- **Permisos:** el monitor solo ve las listas de sus clases.
- `?` Datos de salud de los socios en lista (pregunta 9).

| I | N | V | E | S | T |
|---|---|---|---|---|---|
| ⚠ | ✔ | ⚠ | ✔ | ✔ | ✔ |

- **V:** es una hipótesis mía; la épica no menciona al monitor. Confirmar con un monitor
  antes de meterla.

### Sin escribir todavía

- **Recepción apunta a un socio a la lista.** Depende de la pregunta 8.
- **Prioridad para socios nuevos.** Depende de la pregunta 7.

## Orden de entrega propuesto

| Orden | Historia | Qué se aprende |
|---|---|---|
| 1 | H1 Apuntarme | Cuánta gente se apunta y en qué clases: demanda real. |
| 2 | H2 Recibir la plaza | Cuántas plazas se reasignan y si quien la recibe asiste. |
| 3 | H3 Salir de la lista | Cuánta gente se arrepiente de esperar. |
| 4 | H5 Clase cancelada o cambiada | Cierra los casos que generan quejas. |
| 5 | H4 Ver mis listas | Comodidad. |
| 6 | H6 Monitor | Solo si un monitor confirma que le sirve. |

- **Historia mínima para enseñar a un socio real:** H1. Se puede enseñar en una Sprint
  Review y medir demanda, pero todavía no cumple la promesa de la épica.
- **Mínimo para publicar:** H1 + H2 + H3.

## Definición de Hecho

Sigue pendiente en el contexto. Sin ella, "terminada" significa algo distinto para cada
persona del equipo; conviene traerla escrita al refinamiento.
