# Experiencia inmersiva

Proyecto de clase para crear una pequeña experiencia de realidad virtual accesible desde el navegador de unas Meta Quest 3.

El enunciado original está en [docs/Reto - Experiencia inmersiva.docx](docs/Reto%20-%20Experiencia%20inmersiva.docx). El objetivo mínimo es mostrar una escena 3D con al menos tres objetos, entrar en modo inmersivo, seleccionar o activar un objeto y mostrar una respuesta visual.

## Estado

Fase de diseño: Roi ha aprobado cuatro objetivos principales para una experiencia a escala reducida en un taller: montar un arco, conseguir una segunda munición, detener un robot aspirador y ascender a la máquina que revierte el tamaño. Los pasos intermedios y el mapa están pendientes de concretar. React es un requisito de clase.

## Organización

- `docs/`: enunciado y futura documentación de investigación, diseño y pruebas.
- [`docs/analisis_concepto_y_viabilidad.md`](docs/analisis_concepto_y_viabilidad.md): estudio provisional de la idea y de WebXR con React.
- [`docs/propuesta_comun_concepto.md`](docs/propuesta_comun_concepto.md): decisiones de Roi y propuesta de Claude.
- [`docs/debate_concepto_opinion_codex.md`](docs/debate_concepto_opinion_codex.md): respuesta técnica y recorrido recomendado por Codex, pendiente de debate.
- [`docs/estructura_aprobada.md`](docs/estructura_aprobada.md): cuatro objetivos aprobados y pasos intermedios para debatir.
- [`docs/cierre_fase_1_para_roi_y_claude.md`](docs/cierre_fase_1_para_roi_y_claude.md): decisiones abiertas y preguntas concretas para cerrar el concepto con Roi y Claude.
- [`docs/respuesta_roi_y_revision_codex_fase_1.md`](docs/respuesta_roi_y_revision_codex_fase_1.md): respuestas recientes de Roi, riesgos de diseño y preguntas para la siguiente revisión de Claude.
- [`docs/prompt_para_claude_cierre_fase_1.md`](docs/prompt_para_claude_cierre_fase_1.md): encargo breve para que Claude proponga el cierre del concepto.
- [`docs/flujo_provisional_final.md`](docs/flujo_provisional_final.md): versión provisional de Claude con ocho zonas.
- [`docs/revision_codex_flujo_2026-11-27.md`](docs/revision_codex_flujo_2026-11-27.md): revisión de dependencias, fallos, duración y viabilidad, pendiente de dos decisiones de Roi.
- `MEMORIA.md`: registro cronológico de decisiones, avances, pruebas e incidencias.
- Código y recursos: se incorporarán cuando se acuerde la estructura técnica.

## Forma de trabajo

Cada hito tendrá una propuesta comprensible, una decisión compartida, una implementación pequeña y una comprobación. Se registrará el resultado en `MEMORIA.md` y se guardará en Git. Las funciones de realidad virtual se validarán también en las Meta Quest 3.
