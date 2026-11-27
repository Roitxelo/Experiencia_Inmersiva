# Flujo del juego · versión provisional de Codex

**Fecha:** 27/11/2026

**Basado en:** [`flujo_provisional_final.md`](flujo_provisional_final.md) de Claude, [`revision_codex_flujo_2026-11-27.md`](revision_codex_flujo_2026-11-27.md) y las decisiones posteriores de Roi.

**Estado:** versión provisional para que Roi la verifique y la contraste con Claude. Conserva intacto el archivo de Claude. Aún faltan el mapa con medidas, el guion técnico y la prueba en Meta Quest 3.

## 1. Reglas que gobiernan todo el recorrido

- **Aguja:** corta hilos, precintos y materiales finos. Un impacto sobre un mecanismo resistente no lo activa.
- **Clavo:** pulsa o empuja mecanismos de presión. No sustituye la precisión de corte de la aguja.
- **Canica + clavo + chicle:** cada canica se fija a la parte trasera de un clavo mediante chicle disponible en el punto de montaje. El clavo se lanza por la punta, se ancla y deja la canica visible; allí aparece su extremo del salto espacial. El chicle forma parte de la interacción y no se recoge como recurso.
- **Arco:** es la única herramienta lanzadora. Agujas y clavos son ilimitados en el carcaj tras el hombro; el arco y las dos canicas van al cinto. El modo exacto de cambiar munición se verificará con los controles reales de Quest 3.
- **Movimiento:** teletransporte apuntado y giro por pasos. La escala pequeña se comunica con muebles y objetos grandes alrededor. No se exige saltar físicamente.
- **Inspección:** un objeto interactuable se resalta; una línea fina apunta a su nombre. Un botón abre una ficha breve con su uso. El texto debe comprobarse dentro del visor.
- **Fallos:** no se pierde munición ni progreso. Un fallo de tiro permite repetir; el contacto con el robot devuelve al último punto seguro mediante fundido. Las canicas siempre tienen un modo de recuperación.

La frase de diseño es: **cortar con aguja, pulsar con clavo y saltar entre canicas unidas a clavos con chicle**. Cada regla debe recibir una demostración clara antes de ser necesaria en un momento de presión.

## 2. Mapa lógico y conexión física

```
Caja de herramientas → rampa de cartón → suelo bajo mesa baja → canal de cables
                                                          ↓ regla-puente
                              cajonera → robot → base de la mesa → salto de canicas → máquina
```

La bolsa cuelga del borde de la mesa baja y se alcanza desde el suelo. Después de recoger los clavos se avanza **por el suelo** hasta un canal de cables abierto, que una persona diminuta no puede cruzar. La regla cae sobre ese canal y conecta dos superficies de suelo a la misma altura. En la otra orilla está el pie de la cajonera. Así se corrige el salto espacial que había entre bajar de la caja y aparecer sobre la mesa baja en la versión anterior. La anchura del canal y la longitud de la regla se fijarán en el mapa medido.

## 3. Recorrido de ocho zonas

| Zona | Qué ve y qué hace el jugador | Qué aprende o consigue |
|---|---|---|
| **0 · Caja de herramientas** | Despierta en una caja abierta. Ve la máquina muy arriba y busca una varilla flexible, hilo y un acerico. Inspecciona, agarra y combina varilla e hilo para montar el arco. Sale de los compartimentos mediante teletransporte. | Arco, agujas, selección e inspección. |
| **1 · Rampa de cartón** | La solapa de una caja está levantada por un hilo. Corta el hilo con una aguja; la solapa baja como rampa. Desciende por puntos seguros y obtiene una primera vista amplia del taller. | La aguja corta y una acción cambia el camino. |
| **2 · Bolsa de clavos** | Desde el suelo ve una bolsa sobresaliendo de la mesa baja. Dos costuras tensas en la parte inferior están a punto de ceder. Corta ambas con agujas; la bolsa se abre y unos clavos caen formando una montañita. La montañita presenta visualmente el alijo ilimitado, y el carcaj habilita clavos sin obligar a regresar tras cada fallo. | Segunda munición y contraste visual entre aguja y clavo. |
| **3 · Regla-puente** | Un canal de cables corta el suelo. Una regla de madera está inclinada sobre él, retenida por un cierre de presión visible en un soporte del taller. Un clavo pulsa el cierre; la regla cae y queda estable sobre el canal. La aguja no activa el cierre. Cruza mediante teletransporte a la otra orilla. | Primer uso del clavo para pulsar y un cambio grande del entorno. |
| **4 · Cajonera-escalera** | Tres cajones de apertura por presión forman una subida hacia el mirador del robot. **Se mantienen los tres disparos con clavo elegidos por Roi**, alternados con movimiento: pulsa el primer cajón, sube a él, observa y pulsa el segundo desde una nueva altura, sube y repite con el tercero. El primero muestra una pequeña holgura y la ficha indica que se abre al presionar. | El mismo principio de presión se aplica a una secuencia espacial, no a tres blancos desde el mismo sitio. Lo alto es el punto seguro. |
| **5 · Robot aspirador** | Desde la cajonera ve al robot patrullar de ida y vuelta. Un clavo pulsa OFF: el botón se hunde, las luces cambian y el robot entra en un modo más rápido que extiende su recorrido bajo una botella de plástico con líquido de color. Una aguja corta el precinto fino de salida de la botella; cae un chorro estilizado y queda una zona mojada. Cuando el robot descontrolado la cruza, se cortocircuita y suelta la **canica 1**, que era su fuente de energía. Baja con teletransporte. | Combinar pulsar y cortar, observar causa y efecto, resolver una trampa visible. |
| **6 · Base de la mesa** | La **canica 2** brilla en una bandeja suspendida. Una aguja corta su hilo y la deja caer sobre una esponja alcanzable. Junto a ella hay un punto de chicle del taller para fijar cada canica a la parte trasera de un clavo. Dispara un conjunto a una zona válida del suelo: aparece un extremo inactivo. Dispara el segundo a una diana de corcho grande sobre la mesa: ambos se enlazan. Entra por el extremo del suelo y aparece sobre la mesa tras un fundido corto. | Usar el arco para colocar las canicas y completar el único salto espacial obligatorio. |
| **7 · Máquina y plomada** | La máquina tiene un pulsador demasiado resistente para su tamaño, bajo una bandeja que guía un peso. Un clavo pulsa el pestillo del flexo y libera el balanceo de una plomada. La aguja corta el hilo cuando la plomada pasa sobre la bandeja; la plomada cae, rueda hacia el botón y lo pulsa. La máquina se activa y el entorno cambia de escala con un fundido. | Final que exige ambas municiones, puntería y momento de disparo, con resultado visible. |

**Cambio frente a Claude:** en la zona 3, el clavo pulsa un cierre en lugar de desplazar una goma de borrar. En la zona 6, la canica se fija con chicle a la parte trasera de un clavo en lugar de usar dedal. Ambos cambios siguen la distinción de herramientas que fijó Roi el 27/11/2026. Codex propone reducir de tres a dos las costuras de la bolsa para evitar un disparo repetido; Roi podrá verificar este ajuste.

## 4. Orden de recursos

| Recurso | Aparece | Primer uso necesario | Otros usos |
|---|---|---|---|
| Arco y aguja | 0 | 1, hilo de la rampa | 2, precinto de botella, bandeja de canica 2, hilo final |
| Clavo | 2 | 3, cierre de la regla | 4, cajones; 5, OFF; 6, soporte de canica; 7, pestillo |
| Canica 1 | 5, robot detenido | 6, primer disparo de enlace | Recuperable |
| Canica 2 | 6, bandeja bajo mesa | 6, segundo disparo de enlace | Recuperable |
| Chicle | 6, punto de montaje | 6, unión de canica y clavo | Disponible siempre en el punto de montaje; no se recoge |

Nada se pide antes de entregarse. La canica 2 se deja caer a un lugar alcanzable **antes** de pedir que sea disparada. La montañita de clavos sigue siendo un elemento del mundo aunque la recarga sea ilimitada desde el carcaj.

## 5. Fallos y recuperación

- **Cortes y pulsadores:** si no se acierta, el objeto permanece en su estado y se puede volver a disparar. Las respuestas de un blanco incorrecto deben ser visibles pero discretas.
- **Regla y cajones:** tras activarse, quedan en posición segura; no se cierran mientras el usuario está encima. El teletransporte solo acepta superficies alcanzables y anchas.
- **Robot:** si toca al jugador, este vuelve a lo alto de la cajonera. El estado de la botella y del robot se conserva. Si se corta el precinto antes de pulsar OFF, la zona mojada espera a que el robot amplíe su patrulla; debe verse que el líquido ya está ahí. Una vez detenido, no se reactiva.
- **Canicas:** solo madera y corcho marcados como superficies válidas aceptan el clavo portacanica. Un disparo inválido devuelve la canica al cinto tras una señal breve. El primer extremo queda inactivo hasta colocar el segundo. La acción “Recoger canicas” devuelve ambas desde cualquier lugar seguro y conserva el progreso de la zona. El salto es bidireccional mientras ambos extremos están colocados. Si se recuperan estando sobre la mesa, una opción de “Volver al último punto seguro” lleva a la base sin pérdida de recursos, evitando quedar atrapado. La salida sobre la mesa es un punto amplio y fijo, independientemente de la orientación de la diana.
- **Plomada:** si se corta el hilo antes de pulsar el pestillo, la plomada cae en una bandeja de retorno y el sistema se repone. Si se corta en un momento desfavorable, también se repone. El botón iluminado y la bandeja ancha hacen visible la ventana de acierto sin exigir precisión milimétrica.

## 6. Ritmo y duración

La cadena alterna **buscar → cortar y moverse → cortar para obtener → pulsar y cruzar → pulsar y subir → pulsar, observar y cortar → combinar y saltar → pulsar y cortar en el momento oportuno**. Roi eligió mantener tres disparos de clavo en la cajonera; se evita convertirlos en una galería de tiro al exigir una nueva posición tras cada disparo.

La estimación de Claude suma **9,5–13,5 minutos sin haberlo medido**. Esta revisión reduce una costura de la bolsa y evita recoger clavos uno a uno, pero no permite asegurar que se llegará a 10–12 minutos: el arco a dos manos, los tres cajones y las canicas pueden ralentizar a alguien nuevo. La duración se validará con usuarios que no conozcan las soluciones, registrando el tiempo de cada zona y los puntos de atasco. No se recortan los tres cajones ni los cuatro objetivos sin una nueva decisión de Roi.

## 7. Viabilidad y pruebas prioritarias en Quest 3

La base **React + React Three Fiber + React Three XR + WebXR** puede mostrar la escena, leer los mandos y lanzar proyectiles; Meta ofrece un ejemplo React de disparos VR. No demuestra que nuestro arco de dos manos, el carcaj tras el hombro, el modo de cambio de munición o la colocación de canicas sean cómodos: necesitan prototipos en las Quest 3.

La solapa, bolsa, regla, cajones, robot y plomada pueden usar estados y animaciones controladas para que los puzles sean repetibles. El líquido puede ser un chorro opaco estilizado con pocas gotas y una zona de contacto, sin simulación completa. Para las canicas, el impacto del clavo determina el anclaje, pero el destino del jugador es un punto seguro predeterminado. Hay que medir rendimiento en el visor y ajustar modelos, luces y efectos; la escala visual por sí sola no garantiza ni impide fluidez.

**Orden de prueba recomendado:** 1) escena gigante, teletransporte y texto; 2) arco, aguja y clavo con carcaj; 3) tres cajones y cambios de altura; 4) robot de dos modos; 5) canicas, recuperación y destino; 6) plomada y reinicio. El diseño aún no está validado en Quest 3.

## Fuentes técnicas consultadas el 27/11/2026

- Meta, [WebXR First Steps React sample](https://developers.meta.com/vr/documentation/web/web-sample-webxr-first-steps-react/).
- Meta, [WebXR performance optimization workflow](https://developers.meta.com/vr/documentation/web/webxr-perf-workflow/).
- Meta, [Locomotion virtual environments](https://developers.meta.com/vr/design/locomotion-virtual-environments/).
- Poimandres, [React Three XR gamepad](https://pmndrs.github.io/xr/docs/tutorials/gamepad).
