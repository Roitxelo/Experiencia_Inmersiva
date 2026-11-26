# Concepto y viabilidad de la experiencia a escala reducida

**Fecha:** 26/11/2026

**Estado:** propuesta para debatir con Roi y Claude; ninguna decisión creativa o técnica queda cerrada.

## La idea de Roi

El usuario aparece con tamaño diminuto en una habitación cotidiana. Los muebles se elevan sobre él y los objetos normales se convierten en obstáculos o herramientas. Recoge y combina materiales cercanos para fabricar, entre otras cosas, un arco y flechas improvisados. Su posible objetivo es llegar a una máquina que revierta su tamaño.

La sorpresa buscada no depende de llenar una habitación de objetos: debe venir de la escala, de descubrir nuevos usos para cosas familiares y de que las acciones tengan consecuencias visibles en el espacio.

## Conclusión técnica provisional

**Sí, una aplicación React con WebXR puede realizar esta experiencia en Meta Quest 3.** WebXR aporta la sesión inmersiva, el seguimiento de cabeza y mandos y la entrada del usuario. La escena, los modelos, la lógica de ensamblaje, las colisiones y la física se construyen con otras bibliotecas o código propio. Meta publica un ejemplo de tiro al blanco en VR con React Three Fiber y React Three XR, con mandos, proyectiles, sonido y vibración. Esto respalda la viabilidad del núcleo, aunque no demuestra por sí solo que nuestra escena completa rinda bien: habrá que medirla en las Quest 3.

La limitación principal no es que WebXR impida la idea, sino el coste de producir una habitación convincente y de programar interacciones físicas creíbles en el tiempo disponible. El navegador del visor exige cuidar modelos, materiales, luces, transparencias y número de objetos dibujados. Meta recomienda medir el rendimiento en el propio visor y optimizar a partir de esos datos.

## Propuesta de base técnica para probar

| Parte | Propuesta inicial | Motivo |
|---|---|---|
| Aplicación | React + Vite + TypeScript | Cumple el requisito de React y permite iterar rápido. |
| Escena 3D | Three.js mediante React Three Fiber | Permite construir la escena con componentes React. |
| VR y mandos | `@react-three/xr` sobre WebXR | Se integra con React Three Fiber; Meta lo usa en su ejemplo React. |
| Objetos | Modelos glTF/GLB optimizados y geometría simple donde baste | Mantener detalle donde la escala lo hace visible. |
| Fusión | Reglas explícitas y puntos de encaje con respuesta visual y sonora | Da sensación de construir sin exigir una simulación física completa. |
| Proyectiles | Primero trayectoria y detección de impacto controladas | El ejemplo React de Meta muestra que puede hacerse sin motor físico. |
| Física | Añadir solo si una prueba demuestra que aporta valor | Gravedad, choques complejos y cuerda deformable aumentan el trabajo y el coste por fotograma. |

Meta también recomienda su Immersive Web SDK (IWSDK) para experiencias WebXR y ofrece sistemas de agarre, locomoción y física. Su estructura principal usa Three.js y un sistema de entidades y componentes, no componentes React como base de la escena. Dado que React es requisito de clase, conviene comparar ambas rutas con una prueba pequeña antes de escoger: React Three Fiber/React Three XR encaja de forma más directa; IWSDK podría ahorrar trabajo en interacciones, pero exigiría decidir cómo se integra React. **No se recomienda mezclar ambos sistemas de escena sin una razón demostrada.**

## Qué puede sorprender y qué cuesta más

| Elemento | Valor para la experiencia | Dificultad y forma de acotarlo |
|---|---|---|
| Aparecer bajo una mesa, con muebles enormes | Impacto inmediato y lectura clara del cambio de escala | Modelar una zona muy cuidada de una sola habitación. Escalar el entorno y sus objetos de forma coherente; probar altura y proporciones en el visor. |
| Objetos cotidianos como materiales | Invita a explorar y experimentar | Dar propósito a pocos objetos relevantes, con pistas visuales y reacciones claras. |
| Fabricar un arco | Momento memorable de transformación | Primera versión: dos o tres piezas se fijan en posiciones válidas y aparece un arco funcional. La flexión realista del palo y de la cuerda queda como ampliación. |
| Apuntar y disparar | Acción física satisfactoria | Empezar con apuntado estable y proyectil simple; después probar tensión visual, sonido y vibración. Medir la facilidad de apuntar. |
| Llegar a la máquina | Da dirección y final a la experiencia | Diseñar una ruta corta con dos o tres zonas conectadas dentro de la habitación. La máquina podría estar visible desde el inicio, pero fuera de alcance. |
| Recuperar el tamaño | Final sorprendente | Estudiar una transición con fundido y cambio de escala del entorno. Evitar mover bruscamente la cámara o alterar el seguimiento de la cabeza. |

## Riesgos que conviene comprobar pronto

1. **Escala y altura.** La impresión de ser diminuto depende de proporciones y de una altura de cámara creíble. La escala de los muebles, los objetos que se agarran y las colisiones debe ser consistente. Hay que comprobarlo en Quest 3; una vista de escritorio no basta.
2. **Accesibilidad de los objetos.** Si todo está en el suelo, algunas personas tendrán que agacharse repetidamente. Se puede probar agarre a distancia o colocar la zona de montaje a una altura cómoda, sin perder la ficción de estar a ras de suelo.
3. **Movimiento y confort.** Recorrer una habitación enorme puede producir mareo si se usa desplazamiento continuo. Probar teletransporte y giros por pasos como opciones iniciales, con trayectos cortos y puntos de llegada claros.
4. **Complejidad del arco.** Un arco convincente con dos manos, cuerda deformable, proyectil y colisiones precisas es una tarea independiente. Se recomienda validar primero el ensamblaje y un disparo sencillo antes de prometer una simulación completa.
5. **Rendimiento.** La escala grande hará visibles las texturas y superficies de muebles cercanos. Habrá que equilibrar detalle, iluminación y número de objetos; medir en el visor real.
6. **Acceso al visor.** La experiencia publicada necesitará una URL HTTPS. La compatibilidad se debe detectar en tiempo de ejecución; el navegador y el dispositivo pueden cambiar.

## Primera prueba de viabilidad propuesta

Una prueba pequeña permitiría decidir con datos y sin fijar todavía la historia completa:

1. Escena React/WebXR con suelo, una mesa y una silla a escala gigante, y tres objetos manipulables junto al usuario.
2. Entrada en VR en Meta Quest 3, seguimiento de mandos, selección y una forma cómoda de recoger un objeto.
3. Dos piezas que se unen en un punto definido y producen una herramienta provisional.
4. Un disparo sencillo contra un blanco y respuesta de impacto.
5. Medir comodidad, claridad de la escala y fluidez en las gafas; registrar resultados en `MEMORIA.md`.

Si esta prueba funciona, podremos ampliar el recorrido, el detalle visual y la construcción del arco. Si falla, habremos localizado pronto el problema real: interacción, escala, confort o rendimiento.

## Preguntas para el debate con Roi y Claude

- ¿Qué habitación crea la imagen más potente con el menor número de modelos: aula, salón, garaje u otra?
- ¿Qué causa la reducción de tamaño y por qué existe la máquina? Una razón sencilla puede convertir la mecánica en una historia.
- ¿El arco es la herramienta central o una de varias soluciones? ¿Qué obstáculo justifica fabricarlo y dispararlo?
- ¿Qué debe poder hacer el usuario en los primeros 30 segundos para sentir que está en un mundo enorme?
- ¿Preferimos una experiencia breve y muy pulida o una exploración más larga con más sistemas?
- ¿Cuándo podremos hacer la primera prueba presencial con las Quest 3?

## Fuentes consultadas el 26/11/2026

- Meta, [WebXR overview](https://developers.meta.com/vr/documentation/web/webxr-overview/): WebXR en Meta Quest y detección de capacidades.
- Meta, [WebXR First Steps React sample overview](https://developers.meta.com/vr/documentation/web/web-sample-webxr-first-steps-react/): ejemplo React Three Fiber y React Three XR con mandos, proyectiles, audio y vibración.
- Meta, [WebXR performance optimization workflow](https://developers.meta.com/vr/documentation/web/webxr-perf-workflow/) y [performance best practices](https://developers.meta.com/vr/documentation/web/webxr-perf-bp/): medición y límites de renderizado.
- Meta, [Immersive Web SDK overview](https://developers.meta.com/vr/documentation/iwsdk/guides/overview/) y [built-in interactions](https://developers.meta.com/vr/documentation/iwsdk/guides/06-built-in-interactions/): alternativa con agarre, locomoción y física.
- Meta, [locomotion best practices](https://developers.meta.com/vr/design/locomotion-best-practices/) y [content guidelines](https://developers.meta.com/vr/resources/publish-content-consider/): confort y accesibilidad.
- [React Three Fiber documentation](https://r3f.docs.pmnd.rs/): integración de Three.js en React.
- MDN, [WebXR permissions and security](https://developer.mozilla.org/en-US/docs/Web/API/WebXR_Device_API/Permissions_and_security): condiciones para iniciar una sesión inmersiva.
