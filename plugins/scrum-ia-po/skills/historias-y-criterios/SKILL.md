---
name: historias-y-criterios
description: Divide una épica o una idea en historias de usuario pequeñas y verticales con el chequeo INVEST, y escribe sus criterios de aceptación en Dado / Cuando / Entonces con casos límite y de permisos, más las preguntas del equipo antes de empezar. Usar cuando el Product Owner pida "divide esta épica", "escribe las historias", "criterios de aceptación", "prepara el refinamiento" o pegue una historia para revisarla.
---

# Historias de usuario y criterios de aceptación

Sirve para llegar al refinamiento con algo que el equipo pueda discutir, no para
sustituir esa conversación. Las historias que salen son una propuesta.

## Antes de empezar

- Si existe `contexto-producto.md`, léelo: personas, glosario y Definición de Hecho
  cambian cómo se escriben las historias.
- Si el usuario tiene un conector de Jira u otra herramienta de backlog, puedes leer la
  épica de ahí. **No crees ni modifiques incidencias** sin enseñar antes el texto y
  recibir un sí explícito.

## Si recibes una épica o una idea

1. Divide en historias **pequeñas y verticales**: cada una aporta valor por sí sola a un
   usuario (no "hacer la base de datos" y luego "hacer la pantalla").
2. Formato: `Como [usuario], quiero [acción], para [beneficio]`. Usa las personas y el
   glosario del contexto, no "como usuario" genérico.
3. Para cada historia: 3 criterios de aceptación breves y el **chequeo INVEST**
   (Independiente, Negociable, Valiosa, Estimable, pequeña (Small), Testeable). Marca la
   letra que falla y por qué.
4. Propón el **orden de entrega para aprender antes** y señala la **historia mínima** que
   ya se podría enseñar a un usuario real.

## Si recibes una historia concreta

Escribe sus criterios en **Dado / Cuando / Entonces**:

- el caso normal;
- 3 casos límite (datos vacíos, valores máximos, errores o caídas de un servicio);
- 1 caso de permisos (quién no debería poder hacerlo);
- y, si la historia toca datos personales o una decisión automática con IA, 1 criterio
  sobre eso (consentimiento, revisión humana, registro).

Al final, las **5 preguntas** que haría alguien del equipo (desarrollo, QA, diseño) antes
de empezar.

## Reglas

- No inventes reglas de negocio: si un criterio depende de algo que no sabes (un límite,
  un precio, una política), escríbelo como pregunta.
- Nada de criterios que describen la interfaz al detalle ("el botón azul a la derecha"):
  describen el comportamiento.
- Si una historia no pasa INVEST de ninguna manera, dilo y propón cómo dividirla o
  reformularla.
