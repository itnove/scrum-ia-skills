**Vais lentos porque casi todo lo empezado está esperando, no porque se trabaje poco.** De las 9 tarjetas abiertas, 7 están en pruebas, revisión o bloqueadas y solo 2 en curso. Desde mediados de octubre termináis un tercio de lo que terminabais antes, y lo abierto lleva una mediana de 52 días cuando lo normal era acabar en una semana.

No he podido ejecutar el script de comprobación en esta sesión, así que las cifras están calculadas a mano sobre las 25 filas.

## Métricas

| Métrica | Valor | De dónde sale |
|---|---|---|
| Trabajo en curso | 9 tarjetas: 4 en pruebas, 2 en revisión, 1 bloqueada, 2 en curso | Filas sin fecha de fin |
| Tiempo de ciclo | Mediana 6 días, percentil 85 de 15 días | 15 tarjetas terminadas (`fin` − `inicio`) |
| Rendimiento global | 1,5 tarjetas por semana | 15 terminadas en 10 semanas (3/9 a 11/11) |
| Rendimiento hasta el 11/10 | 2,2 por semana | 12 terminadas en 5,5 semanas |
| Rendimiento desde el 12/10 | 0,7 por semana | 3 terminadas en 4,4 semanas |
| Antigüedad de lo abierto | Mediana 52 días, de 19 a 64 | Hoy − `inicio` |

- **Dato dudoso:** KAN-13 figura como Hecho con fecha de fin 13/11, que aún no ha llegado. La he dejado fuera; si la cuento, la mediana sube a 7 días y el percentil 85 a unos 20.
- **Lo terminado engaña:** las 12 tarjetas cerradas hasta el 11/10 tardaron 5,5 días de mediana; las 3 cerradas después tardaron 15, 28 y 28.
- **Ley de Little:** con un trabajo en curso medio de 8,5 tarjetas y 1,5 terminadas por semana, el tiempo de ciclo esperable es de unos 39 días, no los 9,5 de media que muestran las terminadas. La diferencia es el trabajo viejo que aún no ha salido.
- **Fiabilidad:** 15 terminadas es el mínimo para fiarse de estas cifras; tomadlas como orden de magnitud.
- **Lo que no puedo calcular:** cuánto tiempo pasa cada tarjeta en cada columna, porque la exportación solo trae inicio y fin.

## Tarjetas envejecidas

Las 9 abiertas superan el percentil 85 (15 días):

| Tarjeta | Estado | Días abierta |
|---|---|---|
| KAN-23 Mejora de carga | En pruebas | 64 |
| KAN-22 Acceso con QR | En pruebas | 62 |
| KAN-19 Texto legal del aviso | En curso | 57 |
| KAN-21 Reservar con un amigo | Bloqueado | 53 |
| KAN-24 Calendario semanal | En pruebas | 52 |
| KAN-18 Crash al abrir en Android | En curso | 46 |
| KAN-20 Panel de cohortes | En revisión | 36 |
| KAN-17 Error al pagar con tarjeta | En pruebas | 35 |
| KAN-25 Recordatorio de cuota | En revisión | 19 |

Miraría primero KAN-17 y KAN-18: por el título parecen fallos que afectan a pagos y al arranque en Android, y llevan más de un mes abiertos.

## Experimentos

1. **Terminar antes de empezar.** Durante 2 semanas nadie abre una tarjeta nueva mientras haya algo en pruebas o revisión que pueda ayudar a cerrar. Funciona si el trabajo en curso baja de 9 a 5 o menos y el rendimiento vuelve a 2 por semana.
2. **Límite de 2 en pruebas.** Con la columna llena, el equipo prueba en vez de desarrollar. Funciona si en 3 semanas ninguna tarjeta lleva más de 15 días en pruebas.
3. **Repaso diario de lo bloqueado y lo más viejo.** Dedicad 5 minutos a KAN-21 y a las 3 tarjetas más antiguas: qué falta, de quién depende y cuál es el siguiente paso. Funciona si en 2 semanas KAN-21 se ha desbloqueado o descartado y la antigüedad máxima baja de 64 días.

## Tres preguntas que cambiarían el diagnóstico

- ¿Quién prueba y quién revisa? Si depende de alguien de fuera del equipo o de una sola persona, el atasco está ahí y los experimentos 1 y 2 se quedan cortos.
- Con 4 desarrolladores y solo 2 tarjetas en curso, ¿hay trabajo que no pasa por el tablero?
- ¿Qué pasó hacia el 11/10 (un lanzamiento, una baja, un cambio en el proceso de pruebas)? El frenazo empieza ahí.