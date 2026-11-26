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

