# Soluciones por pasos

Cada solución respeta las decisiones de Roi registradas en `MEMORIA.md` y deja fijado lo que necesitará el mapa. Las medidas concretas están en [03_cotas_y_mapa.md](03_cotas_y_mapa.md). Los controles, las caídas y la interfaz están en [04_controles_confort_interfaz.md](04_controles_confort_interfaz.md).

**Decisiones de Roi que se mantienen:** clip como arco que se abre tirando de las puntas; aguja con hilo solo en la rampa inicial (el ovillo no se transporta); canica 2 bajada cortando su hilo; regla-puente con calzo de goma de borrar; cajonera como peldaños con tres cajones; robot de dos modos con botella y charco; canicas con chicle en la parte trasera de un clavo; teletransporte solo al final y un único salto; final con plomada y bandeja embudo; munición ilimitada; 3 hilos en la bolsa; orden de recortes.

**Decisión nueva de Roi (27/11/2026):** la cuerda del arco es una **goma elástica del costurero** (E03).

---

## Críticos

### E01 · Alturas de las zonas 3–5
**Problema real:** si la regla deja al jugador en el zócalo de la cajonera a la altura de la mesa baja, bajar "por los mismos cajones" no lleva al suelo.

1. Fijar tres niveles: **suelo (0)**, **nivel de la mesa baja (25 cm)** y **lo alto de la cajonera (49 cm)**.
2. La cajonera está apoyada en el suelo. En su cara que mira a la mesa baja tiene una **repisa intermedia** a 25 cm (un hueco sin cajón, como un estante). La regla está de pie en esa repisa y, al caer, une la mesa baja con la repisa por encima del hueco.
3. **Subida (cara de la mesa baja):** desde la repisa, tres cajones de 8 cm llevan a lo alto (33 → 41 → 49 cm). Son los tres que se abren con clavos.
4. **Bajada (cara del robot):** la cara opuesta tiene una **escalera de cajones ya abiertos** y llenos de tornillos (el inventor los dejó así) que baja de lo alto hasta el suelo del pasillo del robot. Se ve desde arriba y es el camino evidente.
5. Bajar antes de parar al robot lleva al pasillo, donde el robot te alcanza y vuelves a lo alto de la cajonera. Es la regla de fallo que ya existía, y ahora tiene sentido (ver E11).

### E02 · Geometría del cartón-rampa
**Parcial:** el diseño no decía cuánto medía el cartón. Gemini supuso que medía lo mismo que la altura de la mesa.

1. El cartón mide **50 cm** y la mesa baja **25**. Al principio está casi vertical, con la base a pocos centímetros del pie de la mesa, y **sobresale unos 24 cm por encima del tablero**, como una valla. Se ve claramente demasiado empinado.
2. Al tirar, la base se desliza por el suelo liso y el cartón **baja apoyado en el borde de la mesa**. Se detiene a unos **35°**, cuando la base choca con un **tope** (un taco de madera en el suelo). En esa posición sobresalen todavía unos 6 cm por encima del borde, así que no se cae.
3. Abajo, en la base, el cartón tiene un **agujero de asa**, como los de las cajas de mudanza. La aguja con hilo pasa por el asa y se traba de lado. Así no hace falta que la aguja aguante clavada en el cartón (lo que preocupaba a Gemini), y el asa es un blanco claro.
4. Ficha del cartón: *"Cartón. Demasiado empinado para subir. Tiene un asa abajo."*

### E07 · Choque del joystick
1. Joystick izquierdo para caminar y derecho para girar por pasos. El joystick **ya no cambia la munición**.
2. La munición cambia con el **botón X**. El proyectil que hay en la mano se transforma, suena distinto y la punta del carcaj cambia de color.
3. Mapa completo en [04](04_controles_confort_interfaz.md#1-mapa-de-mandos-propuesta-para-validar). Se valida en la fase 0.

### E09 · Caídas
1. **Regla:** cualquier caída fuera del recorrido provoca un **fundido de 0,5 s** y la reaparición en el **último punto seguro**. No se pierde nada.
2. Los puntos seguros se guardan al llegar a ellos: inicio, alto de la rampa, junto a la montañita de clavos, extremo de la regla, cada cajón alcanzado, lo alto de la cajonera, base de la mesa y zona segura sobre la mesa de trabajo (lista con cotas en [03](03_cotas_y_mapa.md#4-puntos-seguros-y-zonas-de-caída)).
3. Una caída de hasta un peldaño (unos 8 cm reales) es un paso normal y no cuenta como caída.
4. Los bordes llevan un **reborde visible** (listón, borde de bandeja o canto del cajón) para que el jugador vea el límite. No hay muros invisibles, así que el salto sigue pidiendo habilidad.

### E23 · Alcance y prueba técnica
1. **Fase 0, antes del mapa con medidas:** confirmar el modelo de visor (Roi pregunta en clase) y hacer un prototipo con la escena mínima del enunciado (3 objetos con resalte), el arco a dos manos disparando a una diana, caminar y saltar entre dos plataformas con viñeta, y medir los FPS.
2. **Construcción por capas:** capa 1 = zona 0 (ya cumple el mínimo del enunciado); capa 2 = zonas 1–3; capa 3 = zonas 4–5; capa 4 = zonas 6–7. Cada capa se puede entregar por sí sola.
3. Los recortes ya aprobados se aplican si la fase 0 o la capa 2 van lentas.

### E31 · El suelo de inicio no puede llevar al resto (no lo vio Gemini)
1. La zona 0 es un **rincón cerrado** entre la pared, el costurero volcado, la silla con la bata hasta el suelo y una caja grande. La única salida es la rampa de cartón.
2. El suelo bajo el hueco de la regla y el que rodea la mesa baja son **zonas de caída** (E09).
3. El suelo del pasillo del robot solo se alcanza bajando desde lo alto de la cajonera.

---

## Moderados

### E03 · Elasticidad del arco
**Decidido por Roi:** la cuerda es una **goma elástica de mercería** que está en el costurero.
1. El clip abierto da la forma rígida y la goma guarda la energía, como en un tirachinas. Por eso el disparo es creíble.
2. Zona 0: acerico, **goma elástica** y clip siguen siendo los tres objetos del enunciado.
3. El **ovillo** pasa a la zona 1: rodó hasta el pie del cartón. Solo sirve para la aguja con hilo, así que su ficha ya no adelanta nada en la zona 0 (resuelve E16).

### E05 · Escala
Escala única: el jugador mide 12 cm y todo es **×15**. Su peso a esa escala es de unos **20 g**.
- Botones de la bata (2 cm): *"como tapas de alcantarilla"*. Dedal (2 cm): *"como una papelera"*.
- Botón final: *"requiere 150 g de presión"*. La plomada pesa 200 g, unas diez veces más que tú.
- Tabla completa en [03](03_cotas_y_mapa.md#1-escala).

### E06 · Péndulo
1. El **pestillo retiene la plomada levantada y apartada a un lado** del brazo del flexo. Al soltarlo, oscila en un plano fijo.
2. **Toda la oscilación pasa por encima de la bandeja embudo.** Cortes cuando cortes, cae dentro, rueda al centro y pulsa el botón. Esto cumple la condición de Roi (entrada 12): *"sin que el objeto pueda caer donde no es"*.
3. La dificultad está en **acertar con una aguja a un hilo que se mueve**. El botón se ilumina cuando la plomada pasa por el centro, como ayuda para elegir el momento.
4. Mientras el pestillo la retiene, el hilo va pegado al brazo del flexo y **no se puede seleccionar** (no se resalta). No se puede cortar antes de tiempo.
5. Se eliminan de la tabla de fallos el "cajón" y el "carrete".

### E08 · Mareo
1. Se mantiene la decisión de Roi: sin teletransporte hasta las canicas.
2. Confort por defecto: viñeta al moverse y al saltar, giro por pasos de 30° y velocidad moderada.
3. Opción de **saltos asistidos**: apuntas al borde del siguiente peldaño, pulsas saltar y el salto sigue una parábola fija hasta ese borde.
4. Se prueba en la fase 0. Si aun así marea, se plantea a Roi en ese momento (hay una pregunta abierta en [04](04_controles_confort_interfaz.md)).

### E11 · Robot esquivable
1. El robot patrulla un **pasillo** entre la pared y el costado de la mesa de trabajo. Es el único camino desde la cajonera hasta la base de la mesa.
2. El robot **ocupa todo el ancho** del pasillo (5 m percibidos), y el recorrido normal lo cubre de punta a punta. No hay hueco para pasar mientras patrulla.
3. Si te alcanza, fundido y vuelves a lo alto de la cajonera.

### E15 · Canicas: orden y superficies
1. **Superficies válidas:** madera o corcho. Arriba, la **diana de corcho**, de pie en el borde del tablero y de cara al suelo. Abajo, las **patas de madera** de la mesa de trabajo.
2. **Orden libre:** el enlace se activa cuando una canica está abajo y la otra en la diana, en cualquier orden.
3. Si las dos quedan abajo (o las dos arriba), brillan pero no se enlazan, y la ficha dice: *"Una tiene que quedar arriba."* "Recoger canicas" las devuelve.
4. El portal es un **disco vertical** sobre la superficie. Se entra caminando hacia él.

### E16 · Estados de la zona 0
1. Con la goma, en la zona 0 ya no hay ovillo (E03).
2. La aguja con hilo solo se puede hacer con el arco montado. Antes, el ovillo no se resalta como combinable.
3. La ficha del ovillo es progresiva. Primero: *"Ovillo de hilo. Largo y resistente."* Al mirar el cartón con el arco montado: *"Atado a una aguja, podrías tirar de algo."*

### E24 · Interfaz React
Se define en [04](04_controles_confort_interfaz.md#4-interfaz-react). Incluye pantalla de inicio con comprobación de WebXR, opciones de confort, menú de muñeca, pantalla final y panel de depuración.

### E25 · Investigación guiada 👤
Tarea de Roi: reescribir `docs/2_investigacion/reto5_investigacion_guiada.md` con sus palabras. No afecta al flujo.

### E30 · Hilos de la bolsa (no lo vio Gemini)
La zona 2 del flujo decía 2 hilos y la guía 3. Roi restauró los 3 hilos (entrada 16), y pasar a 2 es el recorte n.º 2. En la v2 son **3 hilos**.

---

## Menores

| ID | Pasos |
|---|---|
| E04 | Se mantiene la canica pegada con chicle en la parte trasera (cabeza) del clavo. Al tensar, **la cuerda empuja la canica**, que hace de culata. El chicle forma una muesca donde encaja la goma. Gemini lo interpretó como un obstáculo. |
| E10 | Se mantiene (decisión de Roi, entrada 18). Para abaratarla, el hilo es una línea dibujada, no una cuerda física. "Tirar" se detecta cuando la mano que agarra el hilo retrocede 30 cm en la dirección correcta, y eso lanza una animación del cartón. |
| E12 | La **base de carga** del robot, quieta junto a la pared, lleva la misma pegatina. Las fichas quedan fijas en el espacio al abrirse y se cierran con B. El área de selección de objetos que se mueven es más grande. |
| E13 | El robot deja una **franja limpia** en el polvo del suelo, que marca su recorrido normal. La botella está más allá del final de esa franja. Si se perfora antes, el charco queda visiblemente fuera y la ficha dice: *"El robot nunca llega hasta aquí."* |
| E14 | "Un solo salto" significa **un solo par de portales** en todo el juego. El enlace se mantiene por seguridad, pero "Recoger canicas" desaparece del menú tras el salto, así que el enlace no se puede deshacer. |
| E17 | "Proyectil" es el término general y se dice "aguja" o "clavo" cuando importa cuál. "Flecha" desaparece. |
| E18 | La botella se perfora solo con aguja. El clavo rebota en ella (pista). |
| E19 | Al agarrar el acerico, las agujas pasan al carcaj. Se pueden disparar en cuanto hay arco. |
| E20 | El chicle es material fijo de la zona 6. No figura en el calendario de desbloqueos. |
| E21 | Ovillo, chicle y diana pasan a la sección de objetos del escenario. |
| E22 | Objetivo de 10–12 min y estimación de 10–14. Se mide en la capa 2 y se aplican recortes si hace falta. |
| E26 | El clip es definitivo en diseño y se valida en el prototipo de la fase 0. |
| E27 | Objetivo 2: "Conseguir los clavos y aprender a usarlos" (zonas 2–4). |
| E28 | 👤 Roi pregunta si la memoria se entrega en gallego. |
| E29 | Se corrige el texto del enlace en `MEMORIA.md`. |
