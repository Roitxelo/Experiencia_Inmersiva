# Respuesta de Roi y revisión de mecánicas para Claude

**Fecha:** 26/11/2026

**Estado:** decisiones de Roi registradas y cuestiones de diseño pendientes de contrastar con Claude. Este archivo conserva el debate; no es el documento final del juego.

## Decisiones y preferencias expresadas por Roi

| Tema | Decisión o dirección de Roi | Aún por concretar |
|---|---|---|
| Primera munición | Aguja. | Forma de llevarla, recarga y blancos válidos. |
| Primeros minutos | Montar el arco mientras se aprenden controles. Después, una misión guiada con agujas y movimiento para practicar y contemplar la escala del taller. | Qué movimiento se enseña y qué acción resuelve la misión. |
| Acceso a la bolsa | Antes de conseguir clavos, puede haber una misión de acceso: subir a una mesa/silla y disparar a un amarre o globo para dejar caer un puente. Roi plantea decidir si es opcional u obligatoria. | Geometría exacta y si este paso necesita o no un láser. |
| Segunda munición | Clavos. Una bolsa que sobresale de una mesa está a punto de romperse; las agujas rompen los últimos hilos por abajo. Los clavos caen y forman una montañita que actúa como alijo infinito. | Cuántos proyectiles se pueden llevar y cómo se recargan. |
| Láser | Debe tener una función con sentido. Puede intervenir antes o después de conseguir clavos. | Qué bloquea y cómo se supera sin repetir otro puzle. |
| Robot | Patrulla lineal delante de la zona final. Un clavo pulsa su botón de apagado, pero la acción es una trampa: el robot entra en un segundo modo descontrolado. La solución definitiva usa agua que cae desde una botella perforada sobre su trayectoria y cortocircuita el robot. | Señales de la trampa, secuencia de botella, recuperación si el jugador falla y representación visual del resultado. |
| Canicas | Tras el robot se obtienen dos canicas vinculadas. Una era su fuente de poder; la otra se ve en una plataforma. La primera lanzada abre un portal inactivo; al lanzar la segunda, ambos se conectan y permiten uno o dos saltos espaciales obligatorios con fundido corto. | Cómo se alcanza la segunda canica, superficies de lanzamiento válidas, cancelación y recuperación después de un error o tras el salto. |
| Máquina | La persona diminuta no debería pulsar el botón directamente. El final debe requerir puntería, habilidad y lógica, aprovechando herramientas o mecánicas adquiridas. | Qué objeto pulsa físicamente el botón y cuál es la cadena de acciones. |
| Ayudas | El objeto interactuable se resalta. Una línea muy fina señala su nombre. Una indicación permite pulsar un botón para inspeccionarlo; la inspección muestra una descripción breve de su uso. | Ubicación legible de línea, nombre y ficha en Quest 3; botón disponible sin conflicto con arco y canicas. |

## Mi lectura del recorrido

Los cuatro tramos aprobados siguen vigentes. Dentro de ellos ya aparecen varios momentos: tutorial de aguja y movimiento, acceso a bolsa, obtención del alijo de clavos, láser, dos fases del robot, botella, recuperación de canicas, salto espacial y máquina final. Para preservar los 10–12 minutos orientativos, cada momento debe resolverse con una acción comprensible y una consecuencia visible. El tiempo exacto se comprobará con personas nuevas; no conviene declarar que encaja sin probarlo.

**Recomendación de Codex:** que la misión del puente sea obligatoria si ese puente es el único acceso a la bolsa. Así el mapa enseña la ruta y evita construir contenido opcional que algunas personas no verán. El láser encajaría mejor **después** de los clavos, para que la segunda munición abra de verdad otra mecánica y el tramo previo no acumule tutorial, puente y sensor antes de la recompensa. Claude debería proponer una función del láser distinta de pulsar otro botón pesado.

## Reglas que propongo para evitar bloqueos

### Agujas y clavos

- El alijo visual de clavos puede ser infinito sin obligar a volver a él tras cada fallo. Recomiendo llevar una pequeña reserva que se recargue automáticamente al regresar cerca de la montañita, o que el carcaj reponga clavos tras unos segundos. El alijo seguiría siendo el origen visible y memorable de la munición.
- Si un disparo obligatorio falla, el proyectil debe poder recuperarse o regenerarse. El jugador nunca debe agotar la única munición que permite avanzar.
- El inventario puede ser abstracto (carcaj con contador pequeño) en lugar de simular físicamente docenas de agujas y clavos.

### Robot y botella

- El primer impacto de clavo debe producir una **señal inequívoca de cambio de modo**: botón hundido, sonido anómalo, luces que pasan de verde a rojo y patrulla más rápida, pero aún predecible. Es una propuesta de comunicación visual para que la trampa no parezca un fallo arbitrario.
- La botella debería ser de plástico fino o tener un cierre frágil; una flecha puede perforarla o liberar su tapón. La botella de vidrio perforada por un clavo o aguja resultaría menos creíble.
- **Propuesta técnica:** representar el chorro de agua con una animación y pocas gotas, y activar el cortocircuito cuando el robot atraviese una zona mojada. No hace falta simular un fluido completo. Chispas y una pequeña descarga pueden comunicar la parada sin llenar la escena de partículas. Esto es una inferencia de diseño apoyada en las recomendaciones de Meta sobre transparencias y partículas en Quest.
- Si el jugador dispara a la botella antes de activar el falso apagado, el juego debe tener una respuesta coherente. Recomiendo que el agua caiga y forme una zona mojada; el robot solo sufre el cortocircuito al cruzarla en el segundo modo. Si esa dependencia no se entiende, será preferible permitir que el agua lo detenga en cualquier momento y usar el falso apagado como sorpresa no obligatoria.

### Canicas y salto espacial

- Antes de lanzar una canica, el jugador debe haber obtenido ambas. Si la segunda se ve en una plataforma alta, hace falta una acción previa para bajarla o acercarla. **Propuesta:** una flecha corta su sujeción y la deja caer a un lugar alcanzable, reutilizando la aguja.
- Una canica lanzada solo queda colocada si toca una superficie autorizada. El punto se marca de forma discreta para que el jugador entienda dónde puede activar el salto. Si cae fuera, se devuelve al inventario tras una breve señal.
- La primera canica colocada abre un efecto inactivo; la segunda completa el enlace. Los dos extremos deben tener una salida segura, orientada hacia una plataforma amplia. El salto usa un fundido breve y conserva una orientación comprensible.
- **Recuperación propuesta:** una acción de “recoger canicas” disponible desde una ficha o menú corto devuelve ambas al inventario desde cualquier lugar seguro. Funciona antes y después de saltar, y no borra otros avances. Si el usuario está dentro de la transición, la recuperación espera a que termine.
- Esta pareja puede servir para uno o dos saltos, como propone Roi. Si se requiere recolocarla después del primer salto, el jugador debe conservar acceso a las dos canicas y a una superficie de salida válida. Hay que dibujar ese ciclo en el mapa antes de comprometer dos saltos.

### Movimiento y ayudas

- Para los “saltos” del tutorial, recomiendo empezar con pequeños huecos superados mediante teletransporte apuntado y una llegada visible, en vez de pedir al usuario que salte físicamente. Meta aconseja teletransporte en huecos y cambios de altura por comodidad. Un salto virtual con botón podría evaluarse después en las Quest 3.
- La línea fina, el nombre y la invitación a inspeccionar deben probarse dentro del visor. El texto largo aparece solo al pedirlo; el resalte y el nombre corto bastan para explorar sin llenar la vista de paneles.

## Dos direcciones para el final que Claude debería evaluar

1. **Peso suspendido:** cerca de la máquina hay un objeto pesado que puede caer sobre el botón. El jugador debe preparar su trayectoria con una herramienta y cortar o liberar un amarre con un disparo preciso. Es legible porque el objeto, su sombra y el botón pueden verse a la vez. Necesita un mecanismo que aproveche de verdad las dos municiones o las canicas sin convertirse en una secuencia arbitraria.
2. **Disparo a través del enlace de canicas:** el usuario coloca el par para trasladarse o redirigir un proyectil hacia el mecanismo de la máquina. Sería una culminación sorprendente de las canicas y del arco, pero requiere enseñar antes que los proyectiles también cruzan y probar la puntería tras el salto. No se debe prometer como solución final hasta validar su claridad y ejecución en Quest 3.

**Preferencia provisional de Codex:** diseñar primero el peso suspendido como final comprensible y probar el disparo a través de canicas como posible mejora de la misma escena. El final debe exigir habilidad sin pedir una regla nueva en el último minuto.

## Preguntas concretas para Claude

1. Propón una **misión tutorial de aguja y movimiento** que dure poco, muestre la escala y enseñe una habilidad necesaria después. Di qué ocurre si se falla.
2. Decide si el puente previo a la bolsa debe ser obligatorio y diseña su causa y efecto. Comprueba que la bolsa y la montañita de clavos se ven desde un punto que invite a investigar.
3. Coloca el láser antes o después de los clavos y propón **una acción con sentido** para superarlo sin repetir el botón del robot.
4. Evalúa el robot de dos modos y la botella: ¿qué señales permiten deducir la solución?, ¿es justo que el primer “apagado” empeore la situación?, ¿qué sucede si la botella se perfora antes?
5. Diseña una ruta para obtener ambas canicas, lanzarlas, recuperar colocaciones erróneas y completar uno o dos saltos sin quedar atrapado.
6. Propón un final que un jugador pueda explicar en una frase tras verlo y que use al menos dos habilidades aprendidas.
7. Señala si la suma de pasos cabe de forma plausible en 10–12 minutos y qué quitarías o combinarías si no cabe, sin alterar los cuatro objetivos aprobados por Roi.

Claude debería distinguir sus recomendaciones de las decisiones ya tomadas. Cuando Roi las revise, podremos cerrar el mapa lógico y después elaborar el documento final sin alternativas abiertas.

## Fuentes técnicas consultadas el 26/11/2026

- Meta, [locomotion virtual environments](https://developers.meta.com/vr/design/locomotion-virtual-environments/) y [locomotion comfort and usability](https://developers.meta.com/vr/design/locomotion-comfort-usability/): huecos, cambios de altura y comodidad.
- Meta, [comfort](https://developers.meta.com/vr/design/comfort/): interacciones a distancia, legibilidad espacial y adaptación al usuario.
- Meta, [WebXR performance best practices](https://developers.meta.com/vr/documentation/web/webxr-perf-bp/): costes de transparencias, partículas e iluminación.
