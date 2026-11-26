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
