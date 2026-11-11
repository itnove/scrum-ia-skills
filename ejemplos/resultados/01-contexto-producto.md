# Contexto del producto: GymApp

Última actualización: 11/11/2026. Fuente única: notas sueltas del Product Owner.
Todo lo que no está marcado como suposición o `PENDIENTE` viene de esas notas.

## 1. Producto y para quién es

GymApp es la app de una cadena de 12 gimnasios con unos 9.000 socios. Sirve para
reservar clases, pagar cuotas y ver horarios. La usan los socios, los monitores que
gestionan las clases y el personal de recepción.

`PENDIENTE`: qué problema resuelve frente a lo que había antes (reservar en recepción,
por teléfono, otra app) no consta en las notas.

## 2. Product Goal actual

**Que los socios nuevos se activen más este trimestre.**

| Métrica | Hoy | Objetivo |
|---|---|---|
| Socios nuevos con 3 o más visitas en sus primeros 30 días | 40 % | 65 % |

- Plazo: "este trimestre". `PENDIENTE`: fecha exacta de cierre.
- `PENDIENTE`: de dónde sale el 40 % y cómo se cuenta una "visita" (ver sección 7).

## 3. Personas principales (hipótesis)

Las notas solo nombran los grupos de usuarios. No hay entrevistas ni datos de uso que
los describan, así que lo que sigue son hipótesis sin evidencia todavía.

| Persona | Qué sabemos (notas) | Qué suponemos (sin confirmar) |
|---|---|---|
| **Socio nuevo** | Es el foco del Product Goal: 6 de cada 10 no llegan a 3 visitas en sus primeros 30 días. | Que la app puede influir en que vuelva (por ejemplo, facilitando la primera reserva). No sabemos por qué no vuelve. |
| **Socio de toda la vida** | Usa la app. | Que ya tiene su rutina y usa sobre todo reservas y pagos. |
| **Monitor** | Gestiona las clases desde la app. | Que su trato con el socio nuevo influye en la activación. |
| **Recepción** | También la usa. | `PENDIENTE`: para qué la usa (altas, cobros, reservas en nombre del socio). |

## 4. Definición de Hecho

`PENDIENTE`: no aparece en las notas. ¿Cuál es la Definición de Hecho del equipo, tal cual
la tenéis escrita?

## 5. Glosario

| Término | Significado |
|---|---|
| **Bono** | Paquete de 10 clases. |
| **Plaza** | Sitio en una clase. |
| **Socio nuevo** | `PENDIENTE`: ¿desde el alta hasta el día 30, o hay otra definición? |
| **Visita** | `PENDIENTE`: ¿entrada al gimnasio, asistencia a una clase reservada, o ambas? |
| **Activación** | Suposición a partir del Product Goal: hacer 3 o más visitas en los primeros 30 días. |

## 6. Restricciones

- **Legales:** la app guarda datos de salud (lesiones que cuenta el socio). Son datos
  de categoría especial en el RGPD, lo que suele exigir consentimiento explícito,
  acceso limitado y más cuidado al usarlos en funciones nuevas o en analítica.
  `PENDIENTE`: quién puede verlos hoy, con qué consentimiento se recogen y si hay una
  persona de referencia (DPO o legal).
- **Técnicas:** `PENDIENTE` (plataformas, sistema de control de acceso a los gimnasios,
  pasarela de pago, integraciones).
- **De marca:** `PENDIENTE`.
- **Equipo y ritmo:** 4 desarrolladores, 1 diseñadora y el Product Owner. Sprints de
  2 semanas. En lo que queda de trimestre caben pocos Sprints: el objetivo de 65 % hay
  que leerlo con esa capacidad delante.

## 7. Pendiente

Ordenadas por cuánto bloquean el trabajo sobre el Product Goal:

1. **¿Cómo se mide una "visita" y de dónde sale el 40 %?** Sin esto no se puede saber
   si un cambio mueve la métrica.
2. **¿Cuándo acaba "este trimestre"** y cuántos Sprints quedan?
3. **¿Por qué los socios nuevos no vuelven?** ¿Hay entrevistas, encuestas o datos de
   uso? Hoy las personas son hipótesis sin evidencia.
4. **Datos de salud:** ¿quién los ve (monitores, recepción), con qué consentimiento y
   quién decide sobre su uso?
5. **¿Cuál es la Definición de Hecho del equipo?**
6. **¿Qué se considera "socio nuevo"** y cuántos entran al mes?
7. **¿Para qué usa la app recepción?**
8. **¿Qué problema resolvía GymApp al nacer** y qué alternativa usaban antes los socios?
9. **Restricciones técnicas y de marca.**
