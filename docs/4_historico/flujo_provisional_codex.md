# Flujo provisional revisado por Codex

**Fecha:** 27/11/2026

**Fuentes de decisión:** `MEMORIA.md` (entradas 11–15), [`flujo_provisional_final.md`](flujo_provisional_final.md) de Claude y la corrección posterior de Roi: **el teletransporte solo se desbloquea con las dos canicas al final**.

**Estado:** versión para verificar con Roi y Claude. No es el diseño final ni sustituye el archivo de Claude.

## Reglas aprobadas

- La aguja **corta** hilos y materiales finos.
- El clavo **pulsa** mecanismos y desplaza piezas resistentes.
- Cada canica, unida con **chicle a la parte trasera de un clavo**, se lanza con el arco. El clavo se ancla y deja la canica expuesta. Al colocar las dos se habilita **un único salto espacial** hasta la mesa de la máquina.
- Agujas y clavos son ilimitados y salen del carcaj situado tras el hombro. El arco y las canicas se llevan en el cinto. El chicle está disponible donde se preparan las canicas y no necesita recogerse como objeto.
- **Antes de las canicas no hay teletransporte.** El jugador recorre el taller con movimiento ordinario, baja por la rampa, cruza el puente y asciende saltando por los cajones. El control exacto de movimiento y salto se decidirá y probará en Quest 3.
- Los objetos interactuables se resaltan; una línea fina muestra su nombre y un botón abre una ficha breve al inspeccionarlos.
- No se agotan los proyectiles ni se pierde el progreso por fallar un disparo. Si el robot alcanza al jugador, la prueba se reinicia desde el punto seguro de la cajonera; esto es una recuperación de fallo, **no una habilidad de desplazamiento del jugador**.

## Ocho zonas y cuatro objetivos

| Zona | Acción y resultado | Progreso |
|---|---|---|
| **0 · Caja de herramientas** | El jugador despierta diminuto, ve la máquina a lo lejos y aprende a mirar, moverse, seleccionar, inspeccionar y agarrar. Encuentra varilla flexible, hilo y agujas; combina varilla e hilo para montar el arco. | Objetivo 1: arco y agujas. |
| **1 · Rampa de cartón** | Una solapa está retenida por un hilo. La aguja lo corta, la solapa baja y el jugador desciende por ella. El descenso abre la primera vista amplia del taller. | Tutorial de corte y movimiento; sin salto espacial. |
| **2 · Bolsa de clavos** | Una bolsa sobresale de la mesa baja y cuelga de **tres hilos** deshilachados. El jugador corta los hilos con agujas; caen clavos y forman el alijo visible. Desde entonces puede sacar clavos ilimitados del carcaj. | Objetivo 2: segunda munición. |
| **3 · Regla-puente** | Una regla de madera está retenida por un calzo de goma de borrar. La aguja no la mueve; un clavo desplaza el calzo y la regla cae sobre un hueco. El jugador **cruza caminando por la regla**, no mediante teletransporte. | Primer uso del peso del clavo para abrir camino. |
| **4 · Cajonera-escalera** | Tres cajones de apertura por presión forman los peldaños. El jugador dispara un clavo al primer frontal, sube al cajón abierto, dispara al segundo desde otra altura y repite con el tercero. **Los tres disparos se mantienen por decisión de Roi.** Entre ellos hay movimiento, cambio de perspectiva y observación. | Llega por sus propios medios al punto seguro frente al robot. |
| **5 · Robot aspirador** | El robot patrulla de ida y vuelta bloqueando el paso. Un clavo pulsa OFF, pero lo pone en modo descontrolado y alarga su recorrido. Una aguja abre el punto frágil de la botella de plástico: cae líquido de color. Al cruzar la zona mojada, el robot se cortocircuita y libera la **canica 1**, su fuente de energía. El jugador baja de la cajonera por los cajones ya abiertos. | Objetivo 3: robot detenido y primera canica. |
| **6 · Base de la mesa** | La **canica 2** está en una bandejita suspendida. Una aguja corta el hilo y la deja caer a una zona alcanzable. El jugador fija cada canica con chicle detrás de un clavo. Dispara la primera a una superficie válida próxima: aparece un extremo inactivo. Dispara la segunda a la diana de corcho visible sobre la mesa: se enlazan. **Solo ahora** puede entrar en el primer extremo y realizar el salto espacial, con fundido corto, hasta la mesa. | Objetivo 4: teletransporte desbloqueado y un solo salto obligatorio. |
| **7 · Máquina y plomada** | El botón es demasiado resistente para el jugador diminuto. Un clavo acciona el pestillo que inicia el balanceo de la plomada. En el momento adecuado, una aguja corta su hilo. La plomada cae en una bandeja que la guía al pulsador; la máquina se activa y devuelve el tamaño con una transición visual. | Final con las dos municiones y puntería. |

La secuencia se organiza en los cuatro objetivos aprobados: **montar el arco → obtener clavos → detener el robot → ascender mediante canicas y activar la máquina**. La rampa, regla y cajonera son pruebas dentro de esa progresión. El láser quedó eliminado por decisión de Roi en la entrada 12 de `MEMORIA.md`.

## Recursos, fallos y recuperación

| Situación | Regla provisional coherente con lo decidido |
|---|---|
| Fallo con aguja o clavo | Se puede volver a disparar desde el carcaj ilimitado. El blanco conserva su estado. |
| Regla y cajones abiertos | Permanecen abiertos y estables para que el jugador pueda cruzar o volver por ellos. |
| Botella antes del falso OFF | El líquido puede caer primero; la zona mojada permanece hasta que el robot amplíe su recorrido. |
| Robot alcanza al jugador | Se reinicia el encuentro desde el punto seguro de la cajonera, conservando los puzles ya resueltos. |
| Canica disparada a superficie inválida | La canica vuelve al cinto; el clavo no es un recurso limitado. |
| Una sola canica colocada | El extremo aparece inactivo. El jugador puede retirar esa colocación y volver a intentarlo. |
| Dos canicas colocadas | El enlace se activa para el único salto obligatorio. La salida del jugador debe ser una superficie segura junto a la diana, no el punto geométrico exacto del impacto. |
| Canicas colocadas en lugares equivocados | La opción “Recoger canicas” del menú de muñeca las devuelve al cinto. Tras el salto, el enlace puede mantenerse para regresar por él; la recuperación no debe dejar al jugador atrapado sobre la mesa. Este caso se verificará con un prototipo. |
| Plomada soltada antes de tiempo | El mecanismo vuelve a su estado inicial y permite reintentar sin límite. |

**Punto espacial aún por medir:** la versión de Claude sitúa el puente entre la mesa baja y la cajonera, pero después de la rampa el jugador está en el suelo. El mapa físico debe mostrar una subida ordinaria y alcanzable al inicio del puente, o ajustar los extremos del puente para que se llegue caminando. No se añadirá una capacidad de teletransporte para resolverlo.

## Ritmo, duración y viabilidad

La alternancia es **buscar y montar → cortar y bajar → cortar para obtener clavos → desplazar un calzo y cruzar → disparar, subir y repetir → pulsar, observar y cortar → combinar y enlazar canicas → pulsar y cortar en el momento adecuado**. Se conservan los tres disparos en la cajonera; cada uno se hace desde una altura distinta. La regla del calzo sigue la propuesta de Claude. No se cambia el número de hilos de la bolsa sin una decisión de Roi.

Claude estimó **9,5–13,5 minutos sin medir**; el objetivo sigue siendo 10–12. El extremo alto supera la meta. Habrá que observar jugadores nuevos y medir tiempos por zona antes de prometer la duración. La dificultad real del movimiento y salto sin teletransporte debe probarse pronto en Quest 3.

React/WebXR puede soportar la escena, el arco y los impactos; las caídas de rampa, bolsa, regla, cajones y plomada pueden ser animaciones controladas. La patrulla del robot y los estados de las canicas también se pueden programar. **Nada de esto demuestra aún que el conjunto sea cómodo o fluido en Quest 3.** La primera prueba técnica debe incluir movimiento y salto ordinarios, arco a dos manos, lectura de fichas y un prototipo de canicas. Si resulta incómodo, se revisarán controles y mapa con Roi sin adelantar el desbloqueo del salto espacial.

## Fuentes técnicas consultadas

- Meta, [ejemplo WebXR con React](https://developers.meta.com/vr/documentation/web/web-sample-webxr-first-steps-react/).
- Meta, [optimización WebXR](https://developers.meta.com/vr/documentation/web/webxr-perf-workflow/).
- Meta, [movimiento y confort en entornos virtuales](https://developers.meta.com/vr/design/locomotion-virtual-environments/).
