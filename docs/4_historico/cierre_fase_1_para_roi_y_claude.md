# Cierre de la primera fase · decisiones para Roi y Claude

**Fecha:** 26/11/2026

**Estado:** documento de trabajo para cerrar el concepto antes de escribir el diseño definitivo. Las recomendaciones de Codex no sustituyen las decisiones de Roi.

**Actualización:** Roi respondió a los seis puntos. Sus decisiones, preferencias y los casos que aún requieren solución están en [`respuesta_roi_y_revision_codex_fase_1.md`](respuesta_roi_y_revision_codex_fase_1.md). Esta versión anterior se conserva como historial del debate.

## Lo que ya está decidido

- Experiencia WebXR en Meta Quest 3; React es obligatorio en clase.
- El usuario es diminuto en un taller de inventor o aula de tecnología. Debe sentir el impacto de ver muebles y objetos cotidianos enormes.
- La meta es llegar a la máquina que devuelve el tamaño normal. La historia de fondo no es la prioridad.
- Cuatro objetivos principales: montar el arco y aprender los controles; conseguir una segunda munición con una nueva utilidad; detener un robot aspirador que puede ir y venir bloqueando la zona final; ascender a la máquina y activar su botón de forma especial.
- Entre esos objetivos habrá interacciones con objetos del taller, disparos que resuelvan obstáculos y al menos una interacción con láser; su funcionamiento exacto sigue abierto.
- Dos canicas conectadas producen un salto espacial. No hace falta ver a través de ellas en la primera versión; ese efecto visual puede estudiarse al final.
- Duración orientativa: 10–12 minutos. Se medirá al probar la experiencia.
- Las propuestas y cambios se registran en `MEMORIA.md`. Los commits llevan únicamente a Roitxelo como autor, sin coautores.

## Decisiones de concepto que aún faltan

| Prioridad | Decisión | Propuesta de Codex para debatir | Por qué afecta al diseño |
|---|---|---|---|
| 1 | ¿Qué hace cada munición y cómo se consigue la segunda? | Primera: aguja/palillo puntiagudo que corta o perfora material ligero. Segunda: punta pesada hecha con una tuerca que acciona mecanismos resistentes. La segunda se obtiene al abrir una caja o bolsa suspendida usando la primera. | Define la cadena de puzles y evita pedir un recurso antes de entregarlo. |
| 2 | ¿Qué función concreta tiene el láser? | Un único sensor o barrera del taller protege el acceso a la segunda munición. La primera flecha debe permitir neutralizarlo mediante una pieza del escenario, con reacción clara del emisor. | Decide si el láser es una acción con sentido o solo una decoración peligrosa. |
| 3 | ¿Cómo se detiene el robot y qué sucede si alcanza al jugador? | Patrulla lineal. Una punta pesada acciona su parada de emergencia. Si toca al jugador antes, este vuelve al último punto seguro mediante una transición breve. | Afecta al ritmo, la dificultad y la implementación de estados. |
| 4 | ¿Cómo se activan y usan las canicas? | Una canica se encuentra al superar al robot y se coloca en un soporte; su pareja ya es visible en una plataforma alta. Entrar en el efecto de la canica activa el salto, con fundido corto. Una sola pareja y un salto obligatorio. | Fija el sentido espacial del ascenso y evita que las canicas se conviertan en un sistema de navegación sin límites. |
| 5 | ¿Qué tiene de especial el botón final? | La máquina exige reutilizar una habilidad aprendida para dejar el botón accesible y luego pulsarlo con la mano. Se debe escoger una acción concreta, visible y distinta de una diana más. | Determina el clímax y los objetos que habrá que colocar en la zona final. |
| 6 | ¿Cómo se explica el uso de objetos? | Resalte y nombre al apuntar; ayuda corta opcional al inspeccionar. Pistas visuales en la escena antes que instrucciones largas. | Condiciona la dificultad para alguien que usa las gafas por primera vez. |

La fecha exacta de entrega y la primera oportunidad de probar en Quest 3 siguen pendientes. Son datos de planificación, no decisiones creativas.

## Dos propuestas para el momento final

**A · Seguro de la máquina.** El usuario llega junto a la máquina. Un cierre impide tocar el botón. Una flecha de aguja corta un precinto visible; la cubierta se abre y el usuario presiona físicamente el botón. Reutiliza la primera munición, pero podría resultar demasiado parecido a disparar a cualquier otra atadura.

**B · Circuito de activación.** La máquina tiene un contacto eléctrico fuera de alcance. Un disparo con punta pesada mueve una pieza conductora o un interruptor; la máquina se enciende, baja su botón hacia el jugador y este lo presiona con la mano. Reutiliza la segunda munición y ofrece una transformación visible, pero exige diseñar el mecanismo para que se entienda de un vistazo.

**Preferencia provisional de Codex:** B, si Claude encuentra un mecanismo visual claro y plausible dentro del taller. Si requiere explicaciones largas, A será más eficaz.

## Encargo concreto para Claude

Revisa este documento y [`estructura_aprobada.md`](estructura_aprobada.md). Respeta las decisiones de Roi y responde a las seis decisiones abiertas. Para cada una, propone **una solución principal** y explica en una o dos frases qué gana la experiencia y cuál es el riesgo. Comprueba que el jugador obtiene cada objeto antes de necesitarlo y que los láseres, el robot y las canicas tienen funciones distintas. Sugiere un final que sorprenda sin introducir una mecánica completamente nueva en el último minuto. Señala cualquier decisión que deba tomar Roi antes de dibujar el mapa. No empieces todavía el documento final ni des por aprobadas tus propuestas.

## Qué haremos después de este intercambio

1. Roi elige o modifica las soluciones que faltan. Se anotan como decisiones, separadas de las alternativas.
2. Se dibuja el mapa lógico y físico: posiciones, alturas, rutas, visibilidad de la máquina y lugares seguros para saltos espaciales.
3. Se escribe la lista de objetos, estados e interacciones y se construye una prueba técnica en Quest 3.
4. Cuando el concepto y esas secciones estén cerrados, se redactará un **documento final de diseño** con el flujo completo y detallado, sin debates ni propuestas abiertas. `MEMORIA.md` conservará la historia de cómo se llegó a él.

## Referencias técnicas consultadas

- Meta, [ejemplo WebXR con React](https://developers.meta.com/vr/documentation/web/web-sample-webxr-first-steps-react/): base de mandos y disparo.
- Meta, [buenas prácticas de locomoción](https://developers.meta.com/vr/design/locomotion-best-practices/): comodidad en cambios de posición.
- Three.js, [Raycaster](https://threejs.org/docs/pages/Raycaster): detección de blancos e intersecciones.
