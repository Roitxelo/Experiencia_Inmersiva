# MEMORIA del proyecto · Experiencia inmersiva (Meta Quest 3 + WebXR)

Registro paso a paso de todo el trabajo. Cada entrada indica fecha, quién participa, qué se hizo y dónde está guardado.

**Equipo:** Roi (dirección y decisiones), Claude y Codex (asistentes de IA).
**Plazo:** enero de 2027.
**Enunciado:** [docs/Reto - Experiencia inmersiva.docx](docs/Reto%20-%20Experiencia%20inmersiva.docx)

---

## Índice de entradas

| # | Fecha | Tarea | Archivos |
|---|-------|-------|----------|
| 1 | 26/11/2026 | Lectura del enunciado y respuestas a la investigación guiada (Reto 5) | `docs/investigacion/reto5_investigacion_guiada.md` |
| 2 | 26/11/2026 | Preparación del repositorio y forma de trabajo | `README.md`, `.gitignore`, `MEMORIA.md` |
| 3 | 26/11/2026 | Concepto de escala reducida y estudio de viabilidad WebXR con React | `docs/analisis_concepto_y_viabilidad.md` |
| 4 | 26/11/2026 | Opinión de Claude sobre el concepto y opciones para cerrarlo | `docs/debate_concepto_opinion_claude.md` |
| 5 | 26/11/2026 | Decisiones de Roi y propuesta común del concepto para contrastar con Codex | `docs/propuesta_comun_concepto.md` |
| 6 | 26/11/2026 | Respuesta de Codex: viabilidad y recorrido recomendado | `docs/debate_concepto_opinion_codex.md` |
| 7 | 26/11/2026 | Roi aprueba cuatro objetivos y amplía el papel de los pasos intermedios | `docs/estructura_aprobada.md` |
| 8 | 26/11/2026 | Roi aprueba el salto entre canicas y se prepara el cierre de concepto con Claude | `docs/cierre_fase_1_para_roi_y_claude.md` |
| 9 | 26/11/2026 | Roi define municiones, robot, canicas y ayudas; Codex revisa dependencias | `docs/respuesta_roi_y_revision_codex_fase_1.md` |
| 10 | 26/11/2026 | Prompt para Claude y ajuste del efecto de líquido | `docs/prompt_para_claude_cierre_fase_1.md` |
| 11 | 26/11/2026 | Recorrido único propuesto por Claude | `docs/recorrido_propuesto_claude.md` |
| 12 | 26/11/2026 | Decisiones de Roi sobre el recorrido y nuevas opciones (obstáculo de clavos, canicas con arco, péndulo) | `docs/recorrido_propuesto_claude.md` (revisión 1) |
| 13 | 27/11/2026 | Regla-puente, cajonera-escalera y versión provisional final del flujo | `docs/flujo_provisional_final.md` |
| 14 | 27/11/2026 | Revisión técnica y lógica de Codex del flujo provisional de Claude | `docs/revision_codex_flujo_2026-11-27.md` |
| 15 | 27/11/2026 | Decisiones de Roi sobre canicas y cajonera; flujo provisional de Codex | `docs/flujo_provisional_codex.md` |

---

## Entrada 1 · 26/11/2026 · Investigación guiada (Reto 5)

**Participan:** Roi + Claude

**Qué se hizo:**
- Lectura del enunciado (`docs/Reto - Experiencia inmersiva.docx`). Resumen del reto: crear con WebXR una pequeña experiencia inmersiva para Meta Quest 3, accesible desde el navegador de las gafas, con al menos tres objetos 3D que se puedan seleccionar y que respondan visualmente.
- Redacción del borrador de respuestas a las 7 preguntas del apartado 4 (Investigación guiada), con fuentes y fecha de consulta.

**Fuentes consultadas (26/11/2026):** documentación de Meta (WebXR overview, workflow, first steps), MDN Web Docs (WebXR Fundamentals, Startup and shutdown) y documentación de Three.js.

**Ideas que salen de la investigación (pendientes de decidir con Roi):**
- El enunciado menciona una "interfaz React" en las pruebas: habrá que decidir la librería 3D (Three.js puro, React Three Fiber + @react-three/xr, A-Frame o Immersive Web SDK de Meta).
- Para probar en las gafas hará falta HTTPS o ADB (ver pregunta 6).
- Para probar sin gafas: Immersive Web Emulator / IWER (ver pregunta 7).

**Estado:** borrador pendiente de revisión por Roi.

---

## Entrada 2 · 26/11/2026 · Preparación del repositorio

**Participan:** Roi + Codex

**Qué se hizo:**
- Se comprobó que el proyecto está en el repositorio Git interior `Experiencia_Inmersiva/`, cuya rama `main` tiene como remoto `origin` el repositorio de GitHub indicado por Roi. La carpeta contenedora también tiene un repositorio Git, sin commits; se evitará usarlo para este proyecto.
- Se revisó el enunciado y se actualizó `README.md` con el objetivo mínimo, el estado y la organización del trabajo. Se añadió `.gitignore` para excluir `.DS_Store`.
- Se guardó el commit `f50b990` y se subió a `origin/main`. El primer intento falló por falta de resolución de `github.com` en el entorno restringido; la subida posterior se completó correctamente.
- El archivo `docs/investigacion/reto5_investigacion_guiada.md` estaba sin seguimiento durante este trabajo y no se incluyó en ese commit ni se modificó.

**Pendiente de decidir con Roi:** fecha exacta de entrega, tema de la experiencia, si React es requisito obligatorio, disponibilidad de las Meta Quest 3 para pruebas y modo de acceso HTTPS.

---

## Entrada 3 · 26/11/2026 · Concepto y viabilidad

**Participan:** Roi + Codex. La opinión de Claude queda pendiente de incorporar; no se le ha consultado directamente desde este chat.

**Aportación de Roi:** crear una experiencia ambiciosa que sorprenda incluso a usuarios habituales de VR. El usuario empieza reducido de tamaño en una habitación con muebles gigantes, recoge y fusiona objetos cotidianos para fabricar herramientas como un arco y flechas, y podría intentar alcanzar una máquina que revierta su tamaño. React es un requisito confirmado de clase.

**Trabajo realizado:** se contrastó la viabilidad de WebXR con documentación actual de Meta, MDN y React Three Fiber. Se redactó `docs/analisis_concepto_y_viabilidad.md` con una conclusión provisional, dos rutas técnicas posibles, riesgos, una primera prueba en Quest 3 y preguntas de diseño. Las fuentes y la fecha de consulta constan en ese archivo.

**Conclusión provisional:** WebXR con React es suficiente para el núcleo propuesto. WebXR no aporta por sí solo modelos, física ni lógica de fabricación; esas partes requieren bibliotecas y desarrollo. React Three Fiber con React Three XR es la opción inicial más directa por el requisito React, pero no se ha elegido definitivamente. La dificultad principal será lograr interacciones creíbles, confort y buen rendimiento dentro del plazo.

**Pendiente:** debatir el concepto con Roi y Claude, decidir habitación y objetivo, confirmar fecha exacta de enero y realizar una prueba pequeña en las Meta Quest 3 antes de cerrar el alcance.

---

## Entrada 4 · 26/11/2026 · Opinión de Claude sobre el concepto

**Participan:** Roi + Claude

**Qué se hizo:** Claude revisó `docs/analisis_concepto_y_viabilidad.md` (Codex) y escribió `docs/debate_concepto_opinion_claude.md` con su opinión y opciones concretas para cerrar el concepto.

**Opinión de Claude:**
- De acuerdo con la viabilidad y con React Three Fiber + `@react-three/xr`; propone fijar esta ruta ya.
- Propone incluir física ligera (`@react-three/rapier`) en la prueba de viabilidad.
- Propone un tirachinas como herramienta central (más fácil que el arco) y dejar el arco como ampliación.
- Propone recorrido por "islas" con teletransporte y objetos a la altura de la cintura real, por confort y rendimiento.
- Propone una experiencia corta y pulida de 5–7 minutos.

**Opciones planteadas a Roi (recomendada entre paréntesis):** habitación (taller de un inventor), historia (experimento fallido), obstáculo (robot aspirador), herramienta (tirachinas), duración (5–7 min). Incluye un borrador de recorrido en 4 zonas.

**Pendiente:** que Roi elija las opciones A–E; después, documento de diseño y prueba de viabilidad en Quest 3.

---

## Entrada 5 · 26/11/2026 · Decisiones de Roi y propuesta común del concepto

**Participan:** Roi + Claude

**Decisiones de Roi:**
- **Espacio:** taller de inventor / aula de tecnología. La decoración es secundaria; lo importante son las zonas interactuables encadenadas tipo puzle, usando objetos de la sala a favor del jugador (romper una bolsa de clavos, tirar una lámpara para hacer rampa…).
- **Objetivo:** volver a la máquina que revierte el tamaño. La historia de fondo no es prioritaria.
- **Obstáculos:** algo que mantenga alerta y se pueda apagar (no derrotar): láseres, sensores o robot aspirador. El gato se descarta por difícil de integrar.
- **Herramienta:** una única herramienta lanzadora (preferencia por el arco frente al tirachinas, abierto a debate). **La munición es la que da el juego.** Otras herramientas solo si mejoran el juego.
- **Inventos:** objetos científicos como canicas portal, con cuadros de texto que expliquen cómo usarlos y combinarlos.
- **Duración:** 10–12 minutos orientativos.
- **Commits:** deben aparecer solo como hechos por Roitxelo, sin coautores de Claude ni Codex.

**Propuesta de Claude** (`docs/propuesta_comun_concepto.md`):
- Arco viable si la cuerda se dibuja como dos líneas rectas; flechas con **puntas intercambiables** (aguja, clavo, tuerca, clavo + hilo, canica portal). Tirachinas como plan de reserva.
- Usar láseres (puzle) y robot aspirador con ruta fija y botón de apagado (amenaza móvil); ambos viables.
- Canicas portal como teletransporte con fundido; fichas de ayuda al apuntar/coger objetos y libreta del inventor.
- Borrador de recorrido en 6 zonas (0–5) donde cada zona da la munición necesaria para la siguiente.

**Pendiente:** contrastar la propuesta con Codex (lista de puntos técnicos en el apartado 4 del documento) y que Roi responda a las preguntas abiertas.

---

## Entrada 6 · 26/11/2026 · Respuesta de Codex a la propuesta común

**Participan:** Roi + Codex. Documento preparado para que Roi y Claude lo revisen.

**Trabajo realizado:** se leyó la propuesta común y la opinión previa de Claude; se consultaron las fuentes actuales de Meta y Poimandres sobre WebXR con React, mandos, física, rendimiento y locomoción. Se escribió `docs/debate_concepto_opinion_codex.md` con respuesta a las seis preguntas técnicas, una propuesta de recorrido de cuatro tramos y decisiones recomendadas. Las fuentes y la fecha de consulta figuran en ese archivo.

**Hallazgos:** el arco con dos manos es programable, pero su comodidad y precisión requieren prueba real en Quest 3; Rapier puede ayudar con pocos objetos físicos, sin convertir todos los puzles en simulaciones. Robot, láseres y teletransporte son técnicamente posibles. La propuesta común usa una tuerca antes de entregarla al jugador y acumula más mecánicas de las que conviene introducir en 10–12 minutos.

**Recomendación, aún pendiente de aprobación de Roi:** mantener taller, máquina visible, arco modular, robot y duración orientativa; empezar con dos puntas de flecha y cuatro tramos conectados. Reservar láseres, portales y puente de hilo para una ampliación. Fijar React + React Three Fiber + React Three XR como base del prototipo y probar física selectiva con Rapier.

**Sincronización:** se comprobó `origin/main` antes de esta entrada; el repositorio local solo tenía por subir el commit `4808d40` de Roi y Claude. La subida del conjunto queda registrada por el estado final de Git de esta sesión.

---

## Entrada 7 · 26/11/2026 · Cuatro objetivos aprobados

**Participan:** Roi + Codex

**Decisión de Roi:** quedan aprobados cuatro objetivos antes de detallar el mapa: (1) buscar piezas, aprender controles y montar el arco; (2) conseguir una segunda munición que abra otra mecánica; (3) detener un robot aspirador que puede patrullar hacia delante y atrás bloqueando la zona final; (4) ascender hasta la máquina y pulsar su botón de una forma especial. Roi quiere estudiar láseres, portales, herramientas del taller y pequeños obstáculos como pasos entre esos objetivos, no relegarlos automáticamente a ampliaciones.

**Trabajo realizado:** se creó `docs/estructura_aprobada.md` como referencia actual del diseño. Distingue objetivos ya aprobados de posibles funciones de los pasos intermedios y de las decisiones que siguen abiertas. Se actualizó `README.md` y se añadió una nota de corrección al debate anterior de Codex para que su recomendación de aplazar láseres y portales no se confunda con el alcance vigente.

**Pendiente:** concretar con Roi y Claude las dos municiones, la función del láser y del portal, la acción final en la máquina y la geometría del mapa. Probar las interacciones principales en Meta Quest 3 antes de prometer una presentación visual definitiva de los portales.

---

## Entrada 8 · 26/11/2026 · Salto espacial y preparación del cierre de concepto

**Participan:** Roi + Codex. Se prepara un documento para la siguiente aportación de Claude.

**Decisión de Roi:** le gusta una pareja de canicas conectadas que permita un salto espacial. Ver a través del portal no es esencial en la primera versión y puede estudiarse al final.

**Trabajo realizado:** se actualizó `docs/estructura_aprobada.md` con esa decisión. Se redactó `docs/cierre_fase_1_para_roi_y_claude.md`: separa lo decidido de seis decisiones de concepto todavía abiertas, presenta dos posibilidades para el final y formula un encargo concreto para que Claude responda sin reabrir los cuatro objetivos ya aprobados. El documento final detallado se redactará más adelante, cuando mapa, mecánicas, objetos y flujo estén cerrados; `MEMORIA.md` seguirá conservando el debate y las decisiones paso a paso.

**Pendiente:** recibir y contrastar la opinión de Claude y las elecciones de Roi sobre municiones, láser, robot, activación de canicas, final y ayudas. Confirmar fecha de entrega y disponibilidad de Quest 3 para pruebas.

---

## Entrada 9 · 26/11/2026 · Nuevas decisiones de Roi y revisión de mecánicas

**Participan:** Roi + Codex. Se prepara la siguiente revisión de Claude.

**Decisiones y propuestas de Roi:** primera munición de agujas; segunda de clavos obtenidos al disparar a los últimos hilos de una bolsa que sobresale de una mesa y crea un alijo infinito al caer. Antes habrá un tutorial guiado de aguja y movimiento y posiblemente un puente de acceso. El láser debe tener una función con sentido. El robot patrulla en línea: un clavo pulsa un falso apagado que lo descontrola; la solución posterior consiste en perforar una botella para que el agua caiga sobre su recorrido y lo cortocircuite. Tras el robot se obtiene una canica que era su fuente de poder y se ve la segunda en una plataforma; lanzar ambas activa el enlace espacial. El botón final debe pulsarse de forma indirecta, con puntería y lógica. Los objetos se resaltan, muestran el nombre mediante una línea fina y permiten inspección voluntaria con descripción breve.

**Trabajo realizado:** se redactó `docs/respuesta_roi_y_revision_codex_fase_1.md`, diferenciando decisiones, propuestas y cuestiones pendientes. Codex planteó reglas para munición y canicas que eviten quedarse sin recursos o atrapado; señaló la necesidad de hacer justa la trampa del robot, de decidir qué sucede si la botella se perfora antes y de comprobar si el recorrido cabe en 10–12 minutos. Se añadieron preguntas concretas para Claude y referencias a pautas técnicas de Meta.

**Pendiente:** revisión de Claude y decisiones de Roi sobre tutorial, puente, láser, recarga, botella, recuperación de canicas y mecanismo final. La comodidad de saltos, agarre, puntería y texto deberá comprobarse en Quest 3.

---

## Entrada 10 · 26/11/2026 · Prompt para Claude y líquido coloreado

**Participan:** Roi + Codex

**Aclaración de Roi:** el líquido que cortocircuita el robot puede tener otro color; no necesita parecer agua transparente.

**Trabajo realizado:** se actualizó `docs/respuesta_roi_y_revision_codex_fase_1.md` para proponer un chorro opaco y estilizado, sin simulación completa de fluido. Se creó `docs/prompt_para_claude_cierre_fase_1.md`, un encargo breve para que Claude proponga un único recorrido coherente, revise fallos y recuperación de recursos, estime la duración y plantee a Roi solo las decisiones imprescindibles.

**Pendiente:** recibir la propuesta de Claude, contrastarla con Roi y cerrar las decisiones antes de redactar el documento final de diseño.

---

## Entrada 11 · 26/11/2026 · Recorrido único propuesto por Claude

**Participan:** Roi + Claude

**Trabajo realizado:** Claude leyó `docs/estructura_aprobada.md`, `docs/respuesta_roi_y_revision_codex_fase_1.md` y las entradas 6–10, y redactó `docs/recorrido_propuesto_claude.md`: un único recorrido de 7 zonas que conecta los cuatro objetivos aprobados.

**Recorrido propuesto:** caja de herramientas (montar arco y aprender controles) → puente obligatorio cortando un hilo con aguja → bolsa de clavos (3 hilos) → pasillo de cortadora láser (la aguja se funde; un clavo clavado en un taco de madera bloquea el haz) → robot de dos modos (clavo al OFF activa la trampa y alarga su recorrido bajo una botella; el charco de color lo cortocircuita y suelta la canica 1) → base de la mesa (aguja libera la canica 2; las canicas se disparan con el arco y un salto lleva a la mesa) → máquina (un clavo suelta una llave inglesa que se balancea y una aguja corta su hilo cuando pasa sobre el botón).

**Comprobaciones:** ningún recurso se pide antes de entregarlo; cada munición se reutiliza al menos dos veces; ningún fallo deja al jugador atascado (munición ilimitada, fundido al punto seguro, botella válida en cualquier orden, canicas recuperables, tres herramientas para el final). Estimación: 9–12,5 minutos, con lista de recortes si se excede.

**Decisiones pendientes de Roi:** final (péndulo u otra opción de Codex), función del láser, canicas disparadas con arco o lanzadas a mano, munición ilimitada o limitada, uno o dos saltos.

---

## Entrada 12 · 26/11/2026 · Decisiones de Roi sobre el recorrido

**Participan:** Roi + Claude

**Decisiones de Roi:**
1. **Final con péndulo**, con botón grande u objeto pequeño, sin que el objeto pueda caer donde no es.
2. **Se elimina el láser:** el obstáculo de la zona 3 debe superarse *gracias a* un clavo, pero sin usar el clavo como tapón.
3. **Canicas disparadas con el arco**, pero de una forma lógica (disparar una esfera con un arco no lo es).
4. **Munición ilimitada:** proyectiles en un carcaj detrás del hombro; arco y canicas colgados del cinto.
5. **Un solo salto** con las canicas.

**Trabajo realizado:** Claude actualizó `docs/recorrido_propuesto_claude.md` (revisión 1, apartado 11):
- Péndulo: plomada pequeña, pulsador de seta grande en una bandeja en forma de embudo que guía la plomada al botón, balanceo lento en línea fija, el botón se ilumina cuando la plomada está encima, y reposición sin límite.
- Tres alternativas al láser: **balancín de contrapeso** (recomendada; peso del clavo), **peldaños de clavos** (quedarse fijo) y **circuito cortado** (conducir).
- Tres formas de disparar canicas: **flecha con dedal** (recomendada; el portal se abre donde se clava la flecha), **arco de bodoques** con bolsita en la cuerda y canica pegada con plastilina.
- Munición, inventario y número de saltos actualizados según lo decidido.

**Pendiente:** que Roi elija el obstáculo de la zona 3 y la forma de disparar las canicas. Sigue sin ser el diseño final.

---

## Entrada 13 · 27/11/2026 · Regla-puente, peldaños y flujo provisional final

**Participan:** Roi + Claude

**Decisiones de Roi:**
- Implementar dos ideas en lugar del láser:
  1. Una prueba para **hacer caer una regla y formar un puente** (no un balancín que gana peso).
  2. Subir **saltando por peldaños**, pero los peldaños **no pueden ser clavos o flechas** disparados por el jugador, porque no sería lógico que aguantasen su peso.
- Pedir una versión provisional final del flujo del juego. Después Codex la revisará con Roi, se verificará y se cerrará como definitiva.

**Propuesta de Claude** (`docs/flujo_provisional_final.md`):
- **Regla-puente:** una regla de madera, de pie al otro lado de un hueco, frenada por una goma de borrar que hace de calzo. La aguja se clava en la goma sin moverla; un clavo la desplaza y la regla cae formando el puente.
- **Cajonera-escalera:** cajones de apertura por presión. Cada clavo hace saltar un cajón, que sirve de peldaño real. Lo alto de la cajonera es el punto seguro frente al robot.
- El puente de la zona 1 pasa a ser una **rampa de cartón** (solapa atada con hilo), para no repetir la regla que cae.
- Flujo completo en 8 zonas (0–7), con reglas comunes, orden de recursos, ritmo, duración estimada (9,5–13,5 min) y recortes posibles.
- Canicas: se mantiene la **flecha con dedal**, pendiente de que Roi la confirme.

**Pendiente:** revisión con Codex de las dudas del apartado 9 del documento; luego, verificación de Roi y cierre como definitivo.

---

## Entrada 14 · 27/11/2026 · Revisión inicial de Codex del flujo provisional

**Participan:** Roi + Codex

**Sincronización inicial:** antes de revisar el contenido, se subieron a `origin/main` los tres commits locales pendientes (`7f64a6a`, `b544c28` y `5f574f9`), siguiendo el orden solicitado por Roi.

**Trabajo realizado:** se leyeron `docs/flujo_provisional_final.md`, `docs/estructura_aprobada.md` y las entradas 11–13 de esta memoria. Se contrastó la viabilidad con documentación actual de Meta y React Three XR. Se escribió `docs/revision_codex_flujo_2026-11-27.md`, que revisa orden de recursos, fallos, recuperación de canicas, duración y riesgos técnicos en Quest 3.

**Hallazgos principales:** los recursos se entregan antes de su uso. Falta explicar cómo se sube desde el suelo a la mesa baja para cruzar la regla-puente. La duración estimada de 9,5–13,5 minutos supera el objetivo por el extremo alto y todavía no se ha medido con usuarios. El arco, el carcaj, la colocación de portales, los cambios de altura y las ayudas deben probarse en Quest 3. Conviene definir el comportamiento si se corta el hilo de la plomada antes de liberar su balanceo y asegurar que recuperar las canicas no deje al jugador sin salida tras el salto.

**Pendiente de respuesta de Roi antes de escribir la versión provisional de Codex:** flecha con dedal para las canicas y posible repetición entre la regla-puente y los tres cajones accionados con clavos. El flujo de Claude se conserva sin modificaciones.

---

## Entrada 15 · 27/11/2026 · Respuestas de Roi y versión provisional de Codex

**Participan:** Roi + Codex

**Decisiones de Roi:** se descarta la flecha con dedal. Cada canica se adhiere con chicle a la parte trasera de un clavo; el chicle no exige recolección. Se mantienen los tres disparos de clavo para abrir la cajonera. La regla de mecánicas es: aguja para cortar, clavo para pulsar y canica más clavo con chicle para teletransporte. Roi pidió repartir estas acciones entre las pruebas para reducir la sensación de repetición.

**Trabajo realizado:** se redactó `docs/flujo_provisional_codex.md` como versión separada de la de Claude. Conserva las ocho zonas y cuatro objetivos; hace que la regla-puente caiga al pulsar un cierre con clavo, alterna cada disparo de la cajonera con un ascenso, ancla las canicas con clavo y chicle, y define reintentos, recuperación de canicas y reinicio de la plomada. Corrige la conexión física entre el suelo tras la bolsa y la regla-puente situando un canal de cables entre dos superficies a la misma altura. Propone dos costuras en vez de tres para la bolsa; Roi aún debe verificar ese ajuste.

**Viabilidad y límites:** el orden de recursos es coherente y las acciones descritas pueden plantearse en React/WebXR. La estimación de 10–12 minutos no está validada: la tabla previa abarca 9,5–13,5 minutos y el arco, los tres cajones y las canicas pueden ampliar el tiempo. Hay que probar comodidad, puntería, texto, destinos de teletransporte y rendimiento en Meta Quest 3.

**Pendiente:** verificación de Roi, contraste con Claude y elaboración del mapa medido y guion técnico. Esta versión sigue siendo provisional.

