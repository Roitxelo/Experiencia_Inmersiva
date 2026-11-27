# Revisión de Codex del flujo provisional de Claude

**Fecha:** 27/11/2026

**Fuente revisada:** [`flujo_provisional_final.md`](flujo_provisional_final.md), [`estructura_aprobada.md`](estructura_aprobada.md) y entradas 11–13 de `MEMORIA.md`.

**Estado:** análisis previo a la versión provisional de Codex. Las decisiones sobre flecha con dedal y repetición de clavos se han preguntado a Roi y no se cierran aquí.

## Valoración general

El flujo conserva los cuatro objetivos aprobados y ofrece consecuencias visuales claras. La rampa enseña a cortar, la bolsa entrega clavos con un momento espectacular, el robot tiene dos estados y la plomada culmina las propiedades de ambas municiones. Los recursos principales se obtienen antes de necesitarse. La estimación declarada de 9,5–13,5 minutos cruza el objetivo de 10–12; el cumplimiento se debe medir con jugadores nuevos.

## Revisión de dependencias y fallos

| Lugar | Hallazgo | Corrección necesaria antes de cerrar el flujo |
|---|---|---|
| Zona 0 a 2 | Arco y agujas se obtienen antes de cortar la solapa y los hilos de la bolsa. | Mantener una salida de la caja que no dependa de disparar si el arco aún no se ha montado; después la rampa puede ser el tutorial obligatorio. |
| Zona 2 a 3 | El jugador baja al suelo por la rampa. La regla-puente se describe entre la mesa baja y la cajonera, sin un camino que suba al jugador a la mesa baja. | Dibujar una subida accesible o situar ambos extremos del puente en plataformas alcanzables desde el suelo. Comprobar alturas y distancias en un plano antes de modelar. |
| Zona 3 | La aguja que se clava en la goma de borrar funciona como pista del nuevo uso del clavo. | Asegurar que el calzo sigue visible tras varios impactos y que el clavo siempre puede volver a intentarse. |
| Zona 4 | Tres disparos de clavo consecutivos abren tres cajones, justo después del disparo de clavo al calzo. | Decisión pendiente de Roi: mantenerlo o hacer que el clavo abra solo el primer cajón y el resto se supere con movimiento. |
| Zona 5 | Si se perfora la botella primero, el charco espera a que el robot entre en modo descontrolado. La munición ilimitada permite reintentos y tocar al robot devuelve al punto seguro. | Si el jugador alcanza la botella sin pulsar OFF, el charco debe mostrar que aún falta una condición, sin ocultar la pista del botón. Debe poder volver a disparar desde el punto seguro. El robot debe mantenerse detenido tras el cortocircuito. |
| Zona 6 | Las dos canicas se obtienen antes de dispararlas. Las malas colocaciones regresan al cinto y el menú puede recogerlas. | Definir qué superficies cuentan como válidas, un indicador antes del disparo y una salida segura fija sobre la mesa. El portal de la diana puede aparecer en el punto de impacto, pero el jugador debe emerger en una plataforma cercana y libre, no en la orientación de la diana. |
| Zona 6 tras el salto | Recuperar las canicas desde la mesa podría eliminar la única conexión con la base. | Mantener una acción de regreso al último punto seguro o permitir recolocar el par desde la mesa. Ninguna recuperación debe dejar al usuario sin salida. |
| Zona 7 | La plomada se repone si falla. | Definir qué ocurre si se corta el hilo antes de activar el balanceo: debe resetearse o quedar bloqueado con una pista clara. El botón no debe requerir puntería milimétrica; la bandeja en embudo y la iluminación ayudan. |

## Duración

La suma de la tabla de Claude es correcta: **9,5–13,5 minutos estimados, sin medición**. El extremo alto ya supera la meta. Los tres hilos de la bolsa, tres cajones, dos disparos del robot y dos canicas suman varios gestos repetidos; en VR, fallar o demorarse al entender un control amplía el tiempo. Conviene conservar las ocho zonas como lugares reconocibles y reducir repeticiones dentro de alguna zona, según la decisión de Roi sobre la cajonera. La duración real se comprobará con personas que no conozcan las soluciones. Registrar tiempos por zona y dónde se detienen.

## Viabilidad en Meta Quest 3

- **WebXR con React:** Meta publica un ejemplo de juego de disparos con React Three Fiber y React Three XR que cubre mandos, proyectiles e impactos. El arco a dos manos y el carcaj tras el hombro requieren implementación y prueba propias; el ejemplo no demuestra que esas interacciones funcionen ya para este juego.
- **Animaciones y estados:** hacer caer la solapa, bolsa, regla, cajones y plomada mediante estados y animaciones controladas es una decisión técnica razonable. No se necesita simular física libre para cada puzle. La patrulla lineal del robot y su transición entre modos son también controlables.
- **Canicas:** disparar una flecha portacanicas y abrir un portal en la zona de impacto es programable con detección de impactos. El reto está en que el punto sea válido y la llegada cómoda, no en una prohibición de WebXR.
- **Movimiento vertical:** Meta recomienda teletransporte para huecos y cambios de altura. Cada cajón y el destino del salto espacial necesitan una zona de aterrizaje suficientemente ancha y una orientación comprensible.
- **Rendimiento:** la escala gigante no aumenta por sí misma el número de dibujos, pero sí invita a modelos, luces y texturas detalladas. El rendimiento debe medirse en la Quest 3. Meta describe presupuestos por fotograma y un proceso de medición para WebXR; no se puede afirmar hoy que este recorrido mantendrá una tasa concreta.

## Preguntas remitidas a Roi antes de fijar la versión de Codex

1. ¿Confirmamos la flecha con dedal para lanzar las canicas, preferimos un arco con bolsita o otra solución?
2. ¿Mantenemos la regla y tres cajones activados por clavos, o usamos el clavo para abrir el primer cajón y convertimos el resto en una subida de movimiento?

La decisión de Roi sobre estos puntos se incorporará a otra versión provisional en un archivo nuevo. El flujo de Claude permanecerá intacto.

## Fuentes consultadas el 27/11/2026

- Meta, [WebXR First Steps React sample](https://developers.meta.com/vr/documentation/web/web-sample-webxr-first-steps-react/).
- Meta, [WebXR performance optimization workflow](https://developers.meta.com/vr/documentation/web/webxr-perf-workflow/).
- Meta, [Locomotion virtual environments](https://developers.meta.com/vr/design/locomotion-virtual-environments/).
- Poimandres, [React Three XR gamepad](https://pmndrs.github.io/xr/docs/tutorials/gamepad).
