# Respuesta de Codex al debate del concepto

**Fecha de revisión:** 26/11/2026

**Responde a:** [`propuesta_comun_concepto.md`](propuesta_comun_concepto.md) y [`debate_concepto_opinion_claude.md`](debate_concepto_opinion_claude.md).

**Estado:** recomendación para que Roi y Claude la contrasten. Las decisiones que Roi ya tomó se respetan; las propuestas nuevas no quedan aprobadas por este documento.

**Actualización posterior:** Roi aprobó los cuatro objetivos principales y pidió estudiar láseres, portales e interacciones del taller como pasos intermedios. Esa decisión se recoge en [`estructura_aprobada.md`](estructura_aprobada.md) y sustituye la recomendación de este documento de reservar láseres y portales para una ampliación.

## Mi posición

La elección del **taller de inventor**, la **máquina visible como destino**, **una sola herramienta lanzadora con munición que cambia las soluciones** y una duración orientativa de **10–12 minutos** forman un concepto sólido. Mantendría esas cuatro decisiones. La ambición debería concentrarse en la escala, en construir el arma con objetos cotidianos y en dos consecuencias físicas muy visibles, como romper una bolsa y detener un robot. Añadir a la vez láseres, espejo, puente de hilo, caída de lámpara, portales y cinco tipos de flecha haría que cada sistema recibiera menos atención y que el recorrido fuera difícil de aprender y probar.

**Recomendación de diseño:** un taller continuo con **cuatro tramos jugables**, no seis zonas con reglas propias. La habitación entera se ve desde el principio, pero solo los tramos próximos al jugador tienen interacción detallada. La máquina permanece visible en la mesa. La ruta asciende desde debajo del banco hasta ella. Eso conserva la sensación de mundo enorme sin exigir modelar y simular toda la habitación al mismo nivel.

## Respuesta a las seis verificaciones técnicas

| Punto | Veredicto | Condición o límite real |
|---|---|---|
| Arco a dos manos en `@react-three/xr` | **Viable como interacción propia; comodidad sin demostrar.** La biblioteca expone estado de mandos y eventos de entrada. Una mano puede portar el arco y la otra controlar la posición de tensión; dos segmentos visuales bastan para representar la cuerda. | No es una función completa lista para activar. Hay que resolver agarre, encaje de flecha, dirección de tiro, soltar y diferencias de altura/postura. Probarlo en Quest 3 antes de prometerlo como mecánica final. |
| `@react-three/rapier` | **Útil de forma selectiva.** Admite cuerpos rígidos, colisionadores, eventos e impulsos en React Three Fiber. | Lo incluiría en la prueba para recoger y soltar 2–3 objetos. No haría depender todos los puzles de una simulación: la bolsa rota, la regla que cae y el botón del robot pueden usar animaciones y estados controlados. La física no garantiza por sí sola que el agarre VR se sienta bien. Medir coste en el visor. |
| Robot aspirador | **Viable y recomendable.** Ruta de puntos, pausa y detección de proximidad requieren lógica sencilla; no hace falta inteligencia artificial ni física compleja. | Necesita lectura clara de su recorrido, aviso de peligro y recuperación cómoda. Si alcanza al jugador, volver al último punto seguro con fundido breve es más claro que empujarlo. Darle un botón grande y visible evita frustración al apuntar. |
| Láseres y espejo | **Viables técnicamente; aplazar como sistema independiente.** Un rayo y su intersección se calculan con geometría/raycast. | Desviar un haz con un espejo introduce orientación precisa y otro tutorial. En el recorrido actual hay además un bloqueo: se pide una tuerca para cruzar los láseres antes de obtenerla. Sugiero reservar los sensores como decoración o aviso del robot; añadir un puzle de láseres solo si la experiencia base ya está pulida. |
| Canicas portal | **Teletransporte con fundido: viable. Portal visual real: mucho más caro.** | El teletransporte ya es una necesidad de comodidad. Hacer de las canicas un segundo sistema de puzles cambia la gramática del juego y quita protagonismo al arco. Las reservaría para una ampliación posterior; no forman parte del recorrido principal de 10–12 minutos. |
| Fichas de ayuda 3D | **Viables, con prueba de legibilidad.** | Al apuntar: nombre corto y resalte. Al inspeccionar: una ficha voluntaria, estable, a distancia cómoda. No mostrar un panel largo pegado a la mano cada vez que se coge algo. La libreta de muñeca puede ser una mejora, no un requisito inicial. |

**Sobre el arco y el tirachinas:** estoy de acuerdo con Claude en que el tirachinas reduce geometría y animación, pero cambiarlo no sería completamente gratis: su anclaje y dirección de tiro también requieren diseño y pruebas. Roi prefiere el arco y las flechas modulares dan una razón para combinar piezas. Probaría primero un arco visual simplificado. Solo decidiría sustituirlo si el gesto de apuntar o tensar resulta incómodo o poco fiable en la Quest 3.

## Recorrido que propongo para cerrar el concepto

El recorrido es una **cadena de causas visible**. Cada acción abre el siguiente tramo. La versión base usa dos tipos de punta: **aguja**, que corta o perfora materiales blandos, y **peso** (tuerca montada en una flecha), que acciona mecanismos resistentes. Es suficiente para que el jugador descubra que cambiar la munición cambia el mundo.

| Tramo | Situación y acción | Resultado visible | Mecánica nueva |
|---|---|---|---|
| 1. Bajo el banco | Despertar bajo la mesa. La máquina brilla muy arriba. Encontrar una varilla flexible y un hilo/goma; unirlos en un soporte de montaje. | Nace el arco con sonido, vibración y cambio visual. | Escala, inspección y combinación. |
| 2. Materiales suspendidos | Una bolsa de ferretería cuelga fuera de alcance. Una flecha con aguja corta su atadura o perfora la bolsa. | Caen unas pocas tuercas grandes y se descubre el siguiente paso. El jugador fija una tuerca a una flecha. | Tensión y disparo; primera punta con propósito. |
| 3. Suelo vigilado | El robot aspirador patrulla el paso hacia una escalera improvisada de cajas/libros. Su botón de parada resiste la aguja, pero responde al impacto de la punta pesada. | El robot se detiene, libera el camino y sirve de referencia visual de la escala. | Elegir munición y actuar bajo una amenaza con ruta predecible. |
| 4. Ascenso y máquina | Subir por apoyos anchos mediante teletransporte corto; desde una plataforma, cortar con la aguja un cierre que deja caer una regla como puente final. Cruzar y activar la máquina de cerca. | La regla cae ante el jugador; después la máquina se enciende y se muestra un final con fundido y cambio de escala del entorno. | Reutilizar una punta conocida y culminar el objetivo. |

La escalera de cajas/libros y la regla deben diseñarse en un plano de alturas antes de modelar: el último apoyo debe quedar realmente cerca del borde de la mesa. Así evitamos una ruta que parece ingeniosa en texto pero no se puede recorrer en 3D. El teletransporte debe aterrizar solo en superficies seguras; subir de golpe mediante una animación de cámara sería incómodo para parte del público.

**Duración:** conservar los 10–12 minutos como duración esperada para alguien que descubre la experiencia. Diseñar una ruta directa de unos 7–9 minutos deja margen para mirar, entender las fichas y fallar algunos disparos. Se ajustará después de observar usuarios reales, sin añadir puzles solo para alcanzar un número.

## Riesgos del diseño actual que corregiría

1. **Demasiadas reglas a la vez.** Cinco puntas distintas, puentes, portales, espejos y láseres requerirían explicaciones y pruebas independientes. Empezar por dos puntas con comportamientos inequívocos.
2. **Orden de recursos incoherente.** En la propuesta común se usa una tuerca para superar los láseres antes de obtenerla. La ruta anterior entrega primero la punta pesada y luego presenta el botón que la necesita.
3. **Acciones que no parecen físicas.** Un clavo con hilo no crea automáticamente un puente transitable, y una lámpara que cae no garantiza una rampa segura. Esas ideas necesitan diseños específicos; no conviene basar en ellas el camino obligatorio.
4. **Altura y alcance.** Si la persona ficticia mide 10–15 cm, la mesa se siente varias veces mayor, pero también quedan muy lejos los objetos. Probar una escala visual inicial aproximada de 8–12 veces y colocar materiales de montaje a una altura cómoda para el cuerpo real. La cifra final depende de la prueba en Quest 3.
5. **Mareos y lectura visual.** Priorizar teletransporte corto y giro por pasos. Mantener los puntos de interés visibles desde cada tramo. Evitar movimientos forzados de cámara en la transformación final.
6. **Rendimiento.** Pocas luces dinámicas, sombras y transparencias; modelos detallados solo cerca del jugador. El coste se mide en el visor, no se deduce de un ordenador de escritorio.

## Decisiones que propongo cerrar ahora

- **Confirmar:** taller de inventor / aula de tecnología, máquina visible y accesible al final, arco modular como primera opción, dos puntas funcionales, robot aspirador como amenaza principal y 10–12 minutos orientativos.
- **Fijar para el prototipo:** React + TypeScript + React Three Fiber + `@react-three/xr`; probar `@react-three/rapier` únicamente con pocos objetos manipulables.
- **Dejar fuera de la primera versión:** puzle de láseres, espejo, canicas portal, puente de hilo, cinco tipos de puntas y libreta de muñeca. Pueden volver si la ruta base funciona y existe tiempo real para probarlos.
- **No dar por cerrado hasta probar en Quest 3:** escala, arco a dos manos, agarre, legibilidad, teletransporte, caída de objetos y fluidez.

## Primera prueba en Quest 3 que decide el camino

Una escena de baja fidelidad con mesa gigante, dos materiales de montaje, arco provisional, una bolsa suspendida y un blanco grande. Debe permitir entrar en VR, agarrar/unir piezas, tensar/soltar con dos mandos y producir un impacto visible. Añadir dos o tres cuerpos físicos solo para medir si Rapier ayuda al agarre y a las caídas. Registrar: qué comprende un usuario nuevo sin explicación, facilidad para tensar y apuntar, comodidad durante cinco minutos y estabilidad de la imagen en el visor. Si el arco falla, probar el tirachinas con la misma escena antes de cambiar el documento de diseño.

## Fuentes consultadas el 26/11/2026

- Meta, [ejemplo WebXR con React](https://developers.meta.com/vr/documentation/web/web-sample-webxr-first-steps-react/): controladores, proyectiles e impactos en React Three Fiber y React Three XR.
- Poimandres, [entrada de mandos en React Three XR](https://pmndrs.github.io/xr/docs/tutorials/gamepad) y [entradas personalizadas](https://pmndrs.github.io/xr/docs/tutorials/custom-inputs): datos y personalización de controladores.
- Poimandres, [React Three Rapier](https://pmndrs.github.io/react-three-rapier/index.html): cuerpos rígidos, colisionadores e impulsos.
- Meta, [optimización WebXR](https://developers.meta.com/vr/documentation/web/webxr-perf-workflow/) y [buenas prácticas de renderizado](https://developers.meta.com/vr/documentation/web/webxr-perf-bp/): medir en visor y controlar costes de escena.
- Meta, [buenas prácticas de locomoción](https://developers.meta.com/vr/design/locomotion-best-practices/): teletransporte, giros y comodidad.
