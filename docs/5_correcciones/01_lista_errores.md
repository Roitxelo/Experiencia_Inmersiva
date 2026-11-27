# Lista de errores del informe de Gemini

**Fuente:** [informe de Gemini](00_informe_gemini.md) (27/11/2026), sobre `docs/3_diseno/flujo_definitivo.md` y `docs/3_diseno/guia_objetos.md`.
**Revisión:** Claude, 27/11/2026. Roi pidió valorar también si Gemini malinterpretó ideas o escalas.

Gemini contó 24 hallazgos. Aquí se separan los que mezclaban varios problemas (29 en total) y se añaden 2 que Gemini no vio (E30 y E31).

## Cómo leer la tabla

- **Valoración:** *Real* (el error existe), *Parcial* (hay algo real, pero Gemini lo exagera o supone algo que el diseño no dice) o *Malentendido* (Gemini interpretó mal una idea o una decisión de Roi).
- **Gravedad revisada:** la nuestra, que a veces no coincide con la de Gemini.
- **Estado:**
  - ✅ **Resuelto en v2**: la solución ya está escrita en el [flujo corregido](05_flujo_corregido.md) y la [guía corregida](06_guia_objetos_corregida.md).
  - 🧪 **Prueba en Quest**: la solución está escrita, pero hay que confirmarla en el visor.
  - 👤 **Pendiente de Roi**: necesita una decisión o una tarea de Roi.
- **Detalle:** solución por pasos en [02_soluciones_por_pasos.md](02_soluciones_por_pasos.md).

## Tabla

| ID | Hallazgo | Informe | Gemini | Valoración | Revisada | Estado | Solución en una línea |
|---|---|---|---|---|---|---|---|
| E01 | Alturas incoherentes entre mesa baja, cajonera y suelo (zonas 3–5) | 2.1 | Crítico | Real | Crítico | ✅ | Cotas fijadas: la regla llega a una repisa intermedia; se baja al suelo por cajones abiertos del lado del robot. |
| E02 | El cartón no puede quedar como rampa al tirar de su base | 2.2 | Crítico | Parcial | Moderado | ✅ | El cartón es más largo que la altura de la mesa y sobresale por encima del tablero; la aguja lo atraviesa y se traba. |
| E03 | El arco de clip e hilo no tiene elasticidad | 2.3 | Crítico | Parcial | Moderado | ✅ | **Decidido por Roi:** cuerda de goma elástica del costurero. |
| E04 | La canica "detrás del clavo" ocupa el punto donde apoya la cuerda | 2.3 | Crítico | Malentendido | Menor | ✅ | Se mantiene detrás: la canica hace de culata y la cuerda empuja la canica. |
| E05 | Descripciones que no cumplen la escala ×15 (botones, dedal, 2 kg) | 2.4 | Moderado | Real | Moderado | ✅ | Tabla de escala única; textos y peso del botón recalculados. |
| E06 | El péndulo no explica cómo empieza a oscilar y la tabla de fallos inventa cajón y carrete | 2.5 | Moderado | Real | Moderado | ✅ | El pestillo retiene la plomada elevada a un lado; toda la oscilación cae sobre la bandeja; se eliminan cajón y carrete. |
| E07 | El joystick no puede mover al jugador y cambiar de munición a la vez | 3.1 | Crítico | Real | Crítico | 🧪 | Mapa de mandos completo: la munición cambia con un botón. |
| E08 | Riesgo de mareo sin teletransporte (rampa, regla, saltos) | 3.1 | Crítico | Parcial | Moderado | 🧪 | Opciones de confort (viñeta, giro por pasos, saltos asistidos) sin tocar la decisión de teletransporte tardío. |
| E09 | No se define qué pasa si te caes | 3.2 | Crítico | Real | Crítico | ✅ | Fundido y reaparición en el último punto seguro; lista de puntos seguros. |
| E10 | La aguja con hilo solo se usa una vez | 3.3 | Moderado | Malentendido | Menor | ✅ | Decisión consciente de Roi (entrada 18); se mantiene y se abarata su programación. |
| E11 | Se puede esquivar al robot sin detenerlo | 3.4 | Moderado | Real | Moderado | ✅ | El robot ocupa todo el ancho de un pasillo que es el único camino. |
| E12 | Es difícil inspeccionar un robot en movimiento | 3.4 | Moderado | Real | Menor | ✅ | La base de carga, quieta, repite la pegatina; la ficha queda fija al abrirse. |
| E13 | Si perforas la botella antes, nada te guía hacia el OFF | 3.4 | Moderado | Real | Menor | ✅ | Franja limpia en el suelo: el charco cae fuera del recorrido normal y se ve. |
| E14 | "Un solo salto" choca con "el enlace se mantiene para volver" | 3.5 | Moderado | Parcial | Menor | ✅ | Un solo par de portales; "Recoger canicas" desaparece tras el salto. |
| E15 | Orden de disparo, superficies válidas y cómo se entra al portal | 3.5 | Moderado | Real | Moderado | ✅ | Orden libre; una canica en la pata de la mesa y otra en la diana vertical; si las dos quedan abajo, no se enlazan. |
| E16 | La ficha del ovillo adelanta la zona 1 y permite atar la aguja antes de tiempo | 3.6 | Moderado | Real | Moderado | ✅ | Con la goma, el ovillo pasa a la zona 1; la aguja con hilo solo existe con el arco montado. |
| E17 | Se sigue diciendo "flecha" | 3.7 | Menor | Real | Menor | ✅ | Vocabulario único: "proyectil" (aguja o clavo). |
| E18 | Botella: aguja en un documento, "aguja (o clavo)" en otro | 4 | Crítico | Real | Menor | ✅ | Solo aguja. Gemini sobrevalora la gravedad. |
| E19 | Agujas: se desbloquean al empezar o al montar el arco | 4 | Moderado | Real | Menor | ✅ | Pasan al carcaj al agarrar el acerico; se disparan cuando hay arco. |
| E20 | Chicle: desbloqueo o material fijo | 4 | Moderado | Real | Menor | ✅ | Material fijo de la zona 6; no se desbloquea. |
| E21 | Ovillo, chicle y diana están en "Objetos que llevas" | 4 | Moderado | Real | Menor | ✅ | Pasan a "Objetos del escenario". |
| E22 | Duración 10–12 frente a estimación 10–14 | 4 | Moderado | Malentendido | Menor | ✅ | Objetivo y estimación son cosas distintas y ya estaban documentadas; se añade cuándo medir. |
| E23 | Diseño muy amplio sin prueba técnica previa en el visor | 5.1 | Crítico | Real | Crítico | 👤🧪 | Fase 0 de prueba técnica antes del mapa y construcción por capas. Roi confirma el modelo de visor. |
| E24 | No se define la interfaz React | 5.2 | Moderado | Parcial | Moderado | ✅ | Pantalla de inicio, opciones, menú de muñeca, pantalla final y panel de depuración. |
| E25 | Investigación guiada sin personalizar | 5.3 | Moderado | Real | Moderado | 👤 | Roi la reescribe con sus palabras. No es del flujo. |
| E26 | El clip figura como definitivo cuando Roi lo eligió como provisional | 4 | Menor | Real | Menor | ✅ | "Definitivo en diseño; se valida en el prototipo de la fase 0". |
| E27 | El objetivo 2 abarca zonas que no dan munición | 4 | Menor | Real | Menor | ✅ | Objetivo 2: "Conseguir los clavos y aprender a usarlos". |
| E28 | Idioma del entregable (enunciado en gallego) | 5.3 | Menor | No es error | Menor | 👤 | Roi pregunta al profesor. |
| E29 | El texto del enlace al enunciado en MEMORIA muestra la ruta antigua | 5.3 | Menor | Real | Menor | ✅ | Corregido en `MEMORIA.md`. |
| E30 | **No lo vio Gemini:** la zona 2 dice 2 hilos y la guía 3 | — | — | Real | Moderado | ✅ | Son 3 hilos (entrada 16). Pasar a 2 es el recorte n.º 2, aún no aplicado. |
| E31 | **No lo vio Gemini:** nada impide ir andando por el suelo desde el inicio hasta el robot o la mesa de trabajo | — | — | Real | Crítico | ✅ | El inicio es un rincón cerrado; todo suelo fuera del recorrido cuenta como caída. |

## Resumen

| Valoración | Nº |
|---|---|
| Real | 22 |
| Parcial | 5 (E02, E03, E08, E14, E24) |
| Malentendido | 3 (E04, E10, E22) |
| No es error | 1 (E28) |
| **Total** | **31** |

**Malentendidos de Gemini, en breve:**
- **E04:** Roi decidió que la canica va en la parte trasera del clavo. Gemini supone que entonces la cuerda no tiene dónde apoyar, pero la cuerda puede empujar la canica, que a su vez empuja el clavo.
- **E10:** la aguja con hilo de un solo uso no es un descuido. Roi lo decidió porque el ovillo no se transporta.
- **E22:** 10–12 min es el objetivo y 10–14 la estimación sin medir. Que no coincidan es un riesgo conocido, no una contradicción.
- **E02, E03 y E08 (parciales):** Gemini supone medidas o materiales que el diseño no fijaba (un cartón tan largo como la altura de la mesa, un clip sin ningún efecto muelle), o pide teletransporte cuando Roi ya decidió que llega al final.

**Lo que sigue pendiente de Roi:** E23 (confirmar el modelo de visor y hacer la fase 0), E25 (investigación con sus palabras) y E28 (idioma). Ninguno bloquea el mapa.
