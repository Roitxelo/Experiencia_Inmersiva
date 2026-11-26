# Estructura aprobada de la experiencia

**Fecha:** 26/11/2026

**Estado:** cuatro objetivos principales y salto espacial entre dos canicas aprobados por Roi. El resto de los pasos intermedios son propuestas para concretar con Roi y Claude antes de hacer el mapa, la lista de objetos y el guion de puzles.

**Respuesta posterior de Roi:** la primera munición será una aguja; propone clavos como segunda munición, obtenidos al romper con agujas los últimos hilos de una bolsa suspendida. También propuso una misión tutorial previa, un acceso a la bolsa mediante un puente, un robot con falso apagado y cortocircuito por agua, dos canicas que se lanzan para enlazar portales, un final que pulse el botón indirectamente y una ayuda de inspección al apuntar. El detalle y las dependencias se recogen en [`respuesta_roi_y_revision_codex_fase_1.md`](respuesta_roi_y_revision_codex_fase_1.md).

## Visión

El usuario aparece diminuto en un taller de inventor o aula de tecnología. La habitación cotidiana parece monumental. Una máquina que puede devolverle el tamaño normal es el destino. El interés está en aprender a usar objetos del taller, construir una herramienta y resolver obstáculos que reaccionan de forma visible a sus acciones. Duración orientativa: 10–12 minutos, pendiente de medir con jugadores.

## Los cuatro objetivos aprobados por Roi

1. **Montar el arco.** Buscar y encontrar las piezas, combinarlas y aprender al mismo tiempo los mandos y las mecánicas básicas.
2. **Conseguir una segunda munición.** Su obtención debe abrir una forma nueva de actuar sobre el entorno, no limitarse a cambiar el aspecto del proyectil.
3. **Detener un robot aspirador.** Puede patrullar simplemente hacia delante y hacia atrás. Bloquea el acceso a la zona final; el jugador debe inhabilitarlo.
4. **Ascender a la máquina.** Alcanzarla y activar su botón mediante una acción especial, todavía por diseñar.

## Pasos entre objetivos que Roi quiere explorar

Los láseres, portales y pequeñas interacciones con herramientas del taller **forman parte del diseño que se va a estudiar**, en lugar de quedar relegados automáticamente a ampliaciones. No requieren crear más objetivos principales: deben servir para pasar de uno a otro, enseñar un uso nuevo del arco o cambiar la lectura del espacio.

| Transición | Posible función, pendiente de decidir | Qué se debe evitar |
|---|---|---|
| Arco → segunda munición | Un sensor o haz láser protege una caja de piezas. La primera munición permite desactivar su emisor o accionar una pieza del taller que corta el haz. Entonces se abre el acceso al material de la segunda munición. | Exigir la segunda munición para abrir la caja que la contiene. |
| Segunda munición → robot | Un pequeño obstáculo permite practicar la diferencia entre los dos tipos de disparo antes de enfrentarse al robot. Puede ser un interruptor resistente, una tapa o una pieza móvil. | Repetir el mismo blanco sin una consecuencia nueva. |
| Robot → máquina | Tras detener al robot se abre la ruta de ascenso. Una pareja de canicas portal podría trasladar al usuario a una plataforma alta mediante una transición breve; el resto del ascenso debe mantener clara la posición de la máquina. | Presentar portales, escalada y un mecanismo final nuevo todos a la vez sin preparación. |
| Frente a la máquina | Reutilizar una acción aprendida para desbloquear el botón y terminar con una pulsación física cercana. | Un botón final que solo pide apuntar y hacer clic, sin aprovechar lo aprendido. |

Esta tabla expresa **funciones de juego**, no fija todavía ubicación de objetos ni solución exacta. Roi ha elegido un par de canicas conectado que produce un salto espacial. Por ahora no es necesario ver el destino a través del portal; esa presentación puede estudiarse al final. El teletransporte con transición corta encaja mejor con las pautas de comodidad de Meta para cambios de posición y altura.

## Principios para concretar el mapa y los puzles

- Cada obstáculo debe responder a una pregunta clara: qué bloquea, qué pista lo hace entendible, qué acción lo resuelve y qué cambia después.
- La segunda munición debe tener una propiedad distinta de la primera; ambas deben usarse al menos una vez más después de aprenderse.
- El robot debe ser legible y predecible; su trayectoria lineal basta si el momento de detenerlo resulta satisfactorio.
- Los pasos intermedios deben alternar acciones: buscar, combinar, disparar, moverse y observar consecuencias. No encadenar solo dianas.
- Los elementos nuevos deben verse o insinuarse antes de que sean necesarios. La máquina debe seguir siendo una referencia espacial durante el ascenso.
- El mapa debe comprobar alturas, distancias, superficies de teletransporte y alcance real de los mandos antes de construir modelos finales.
- La comodidad y fluidez se validarán en Meta Quest 3. El diseño podrá ajustarse tras esa prueba sin cambiar los cuatro objetivos aprobados.

## Decisiones aún abiertas para el siguiente debate

1. **Identidad de las dos municiones.** La propuesta actual es aguja que corta/perfora materiales ligeros y punta con peso que acciona mecanismos resistentes. Hay que confirmar si resulta intuitiva dentro del taller.
2. **Función del láser.** Sensor que bloquea el acceso, peligro temporizado o parte de una máquina del inventor. Elegir una función principal y una solución que use una mecánica ya aprendida.
3. **Función de las canicas portal.** Ya está decidido que son dos canicas conectadas y permiten un salto espacial sin vista continua del otro lado. Falta determinar cómo se descubren, cómo se activan y qué parte del ascenso resuelven.
4. **Acción especial de la máquina.** Diseñar un final que combine disparo y acción física cercana, pero que se entienda sin texto largo.
5. **Disponibilidad de Quest 3 y fecha exacta de entrega.** Estas dos condiciones fijan cuándo se debe cerrar el prototipo técnico y cuánto detalle cabe producir.

## Nota técnica de viabilidad

La estructura sigue siendo viable como aplicación React/WebXR. Three.js ofrece detección de impactos mediante raycasting para blancos y sensores; la locomoción con teletransporte y giros por pasos tiene respaldo en las pautas de Meta. La complejidad real depende del número de interacciones simultáneas, la presentación de los portales y el rendimiento en el visor. La prueba técnica prioritaria sigue siendo arco a dos manos, selección/agarre, disparo y escala en Quest 3.

**Fuentes consultadas el 26/11/2026:** [Three.js Raycaster](https://threejs.org/docs/pages/Raycaster), [Meta locomotion best practices](https://developers.meta.com/vr/design/locomotion-best-practices/), [Meta WebXR performance best practices](https://developers.meta.com/vr/documentation/web/webxr-perf-bp/) y [React Three XR gamepad](https://pmndrs.github.io/xr/docs/tutorials/gamepad).
