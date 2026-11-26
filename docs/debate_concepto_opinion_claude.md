# Debate del concepto · Opinión de Claude y propuestas para decidir

**Fecha:** 26/11/2026
**Responde a:** [`analisis_concepto_y_viabilidad.md`](analisis_concepto_y_viabilidad.md) (Codex)
**Estado:** propuesta. Roi decide; nada queda cerrado hasta que elija.

---

## 1. Mi opinión sobre el análisis de Codex

**Estoy de acuerdo con lo esencial:**
- La idea es viable con WebXR en Quest 3.
- **React Three Fiber + `@react-three/xr`** es la ruta lógica: React es obligatorio y el IWSDK de Meta no está pensado para escenas con componentes React. Yo la fijaría ya, sin más comparación, para no perder semanas.
- Empezar con una **prueba pequeña en las gafas** antes de diseñar todo es la decisión más importante del documento.
- Los riesgos están bien elegidos (escala, confort, rendimiento, complejidad del arco).

**Lo que añadiría o cambiaría:**

1. **Física: usar una librería ligera en vez de evitarla.** Agarrar, soltar y que las cosas caigan "bien" es más fácil con `@react-three/rapier` que programándolo a mano. Propongo incluirla en la prueba de viabilidad para medir su coste, en lugar de dejarla para el final.
2. **El arco es la parte más cara.** Tensar una cuerda con dos manos es difícil de hacer creíble. Propongo una alternativa que encaja mejor con una habitación y es más fácil: un **tirachinas** (una horquilla de lápiz o de clip + una goma elástica). Se usa casi igual (sujetar, tirar, soltar) pero con un solo punto de tensión.
3. **Ser diminuto ayuda con la accesibilidad.** Si el jugador mide ~10–15 cm, un clip o una goma tienen el tamaño de un brazo o una mochila. Los objetos útiles pueden estar a la altura de la cintura *real* del jugador, sobre "plataformas" (un libro tumbado, una caja de cerillas), y así no hay que agacharse.
4. **Recorrido por "islas" con teletransporte.** En vez de caminar por un suelo enorme, el jugador salta entre zonas pequeñas y bien decoradas. Así solo hay que modelar con detalle lo que está cerca, se evita el mareo y el rendimiento mejora.
5. **Tiempo.** Hay unas 8 semanas (según el registro de avance del enunciado). Recomiendo una **experiencia corta y pulida de 5–7 minutos** con 3–4 zonas, en lugar de una exploración larga.

---

## 2. Decisiones para cerrar el concepto

Para cada pregunta propongo opciones y marco la que recomiendo (⭐). Roi puede elegir, mezclar o proponer otra.

### A. ¿Qué habitación?
| Opción | Por qué |
|---|---|
| **A1 ⭐ Taller de un inventor** (desván o garaje) | La máquina de encoger "pertenece" ahí. Herramientas, tornillos, gomas, cables: materiales naturales para fabricar cosas. |
| A2 Dormitorio infantil | Juguetes gigantes, muy visual y reconocible. Menos lógico para una máquina. |
| A3 Cocina | Muy reconocible, pero los objetos (platos, cubiertos) dan menos juego para fabricar herramientas. |

### B. ¿Qué historia?
| Opción | Resumen |
|---|---|
| **B1 ⭐ El experimento fallido** | Eres el ayudante del inventor. La máquina de encoger se dispara por accidente y te reduce. La máquina para revertirlo está en lo alto de la mesa de trabajo. Tienes que llegar antes de que vuelva el inventor (o antes de que pase el robot aspirador). |
| B2 Misión de rescate | Te encoges a propósito para recuperar algo pequeño (una pieza, un anillo) y luego volver. |
| B3 Sin historia | Exploración libre. Más simple, pero menos memorable. |

### C. ¿Qué obstáculo principal?
| Opción | Por qué |
|---|---|
| **C1 ⭐ Robot aspirador que patrulla** | Fácil de modelar y animar (es un disco que se mueve), da tensión, y puede tener un botón al que disparar para detenerlo. |
| C2 Gato o araña | Más impacto emocional, pero animar un animal creíble cuesta mucho más. |
| C3 Solo obstáculos fijos (huecos, alturas) | Lo más fácil; menos emoción. |

### D. ¿Herramienta central?
| Opción | Por qué |
|---|---|
| **D1 ⭐ Tirachinas** (lápiz/horquilla + goma) | Misma sensación que el arco, mucho más fácil de hacer bien. |
| D2 Arco y flechas | Idea original de Roi; más espectacular pero más arriesgado. Podría ser ampliación si sobra tiempo. |
| D3 Varias herramientas pequeñas | Más variedad, pero cada una necesita su propia interacción. |

### E. ¿Duración?
- **E1 ⭐ 5–7 minutos, muy pulida** · E2 10–15 minutos, más sistemas.

---

## 3. Borrador de recorrido (si se eligen las opciones ⭐)

| Zona | Qué pasa | Interacción | Cumple del enunciado |
|---|---|---|---|
| **0 · Despertar bajo la mesa** | Fundido desde negro. Muebles gigantes, polvo flotando. Arriba, la máquina parpadea. | Mirar alrededor. Seleccionar 3 objetos (un clip, un tornillo, una pila) que se iluminan al apuntarlos. | Escena 3D, sesión inmersiva, ≥3 objetos, selección con respuesta visual |
| **1 · El suelo del taller** | Entre tornillos y virutas están una goma elástica y un lápiz roto. | Agarrar las dos piezas y unirlas en un punto marcado → aparece el tirachinas (sonido + vibración). Disparar a una lata para practicar. | Interacción con objetos, respuesta visual y sonora |
| **2 · La torre de libros** | Para subir hay que tumbar un libro que hace de rampa. El robot aspirador patrulla. | Disparar al libro para que caiga. Teletransportarse entre libros. Esquivar el robot o dispararle a su botón de pausa. | Obstáculo, consecuencias visibles |
| **3 · La mesa de trabajo** | La máquina está apagada: le falta la pila (recogida en la zona 0) o hay que pulsar el botón desde lejos. | Colocar la pila / disparar al botón → la máquina se activa. | Interacción final |
| **Final** | Fundido a blanco; el mundo "se encoge" alrededor. Vuelves a tu tamaño junto a la mesa. | – | Cierre de la historia |

---

## 4. Propuesta de siguiente paso

1. Roi elige A–E (o las cambia).
2. Con eso, escribo el **documento de diseño** (historia, guion de cada zona, lista de objetos, interacciones y flujo) en `docs/diseno/`.
3. En paralelo, la **prueba de viabilidad** de Codex con R3F + `@react-three/xr` + `@react-three/rapier`: zona 0 y el montaje del tirachinas, probada en las Quest 3.
