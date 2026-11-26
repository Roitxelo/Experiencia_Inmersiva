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
