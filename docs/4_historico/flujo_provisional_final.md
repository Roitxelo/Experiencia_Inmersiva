# Flujo del juego · versión provisional final (Claude)

**Fecha:** 27/11/2026
**Base:** [`estructura_aprobada.md`](estructura_aprobada.md), [`recorrido_propuesto_claude.md`](recorrido_propuesto_claude.md) (revisiones 0 y 1) y las decisiones de Roi registradas en `MEMORIA.md` (entradas 12 y 13).
**Estado:** versión **provisional final** del flujo. Siguiente paso: Codex la revisa con Roi y cierra las dudas del apartado 9; después se cierra como definitiva. **No es todavía el documento de diseño** (mapa con medidas, lista de modelos, guion técnico).

Leyenda: **[Roi]** decidido por Roi · **[Pendiente]** falta confirmar.

---

## 1. Premisa

Despiertas diminuto (unos 10–15 cm) en el **taller de un inventor**. Al fondo, sobre la mesa de trabajo, una **máquina** brilla y zumba: es la que te devolverá tu tamaño. **[Roi]** Para llegar a ella fabricarás un arco y usarás los objetos del taller a tu favor.

**Duración orientativa:** 10–12 minutos **[Roi]**. **Saltos con canicas:** uno **[Roi]**.

---

## 2. Reglas comunes

### Controles e inventario **[Roi]**
- **Movimiento:** teletransporte apuntado y giro por pasos (comodidad).
- **Carcaj detrás del hombro:** agujas y clavos, **munición ilimitada**. Llevar la mano atrás y agarrar saca una flecha; el joystick cambia de munición y la punta visible indica cuál está cargada.
- **Cinto:** el **arco** se cuelga en la cadera cuando no se usa; las **canicas** van en una bolsita del cinto.
- **Menú de muñeca:** libreta de objetos descubiertos y acción "Recoger canicas".

### Ayudas **[Roi]**
- Al apuntar a un objeto interactuable: **se resalta** y una **línea fina** lo une a su **nombre**.
- Un botón permite **inspeccionarlo**: ficha breve con qué hace, cómo se usa y con qué se combina.

### Las dos municiones
| | **Aguja** | **Clavo** |
|---|---|---|
| Propiedad | Fina y afilada: **corta y perfora** cosas ligeras (hilo, plástico fino, globo). | Gruesa y pesada: **golpea y empuja** cosas resistentes. |
| No sirve para | Mover nada pesado: se clava o rebota sin efecto. | Cortar hilos finos (es demasiado gruesa: el hilo se dobla y no se rompe). |

### Al fallar
- Nunca se pierde munición ni progreso.
- Tocar el robot = fundido y vuelves al último punto seguro.
- Todo puzle se puede reintentar sin límite.

---

## 3. Mapa lógico

```
[0 Caja de herramientas] -> [1 Rampa de cartón] -> [2 Bolsa de clavos] -> [3 Regla-puente]
                                                                              |
                                                                              v
[7 Máquina] <== salto ==  [6 Base de la mesa] <- [5 Robot] <- [4 Cajonera-escalera]
```

La máquina es visible desde las zonas 0, 1, 4 y 6.

---

## 4. Flujo zona por zona

### Zona 0 · La caja de herramientas (inicio) — Objetivo 1: montar el arco
- **Ve:** fundido desde negro. Paredes de metal, tornillos del tamaño de troncos. Por encima del borde, la máquina al fondo.
- **Hace:** aprende a mirar, teletransportarse entre compartimentos, apuntar, inspeccionar y agarrar. Encuentra **regla de plástico flexible**, **carrete de hilo** y **acerico con agujas**. Combina regla + hilo = **arco**.
- **Obtiene:** arco y agujas.

### Zona 1 · La rampa de cartón — Tutorial de aguja y movimiento
- **Ve:** la caja está junto a una caja de cartón; una de sus **solapas** está levantada y atada con un hilo.
- **Hace:** primer disparo real: **aguja al hilo** → la solapa cae y forma una **rampa** hasta el suelo. Baja teletransportándose. Al pie, contempla la escala del taller: la bolsa de clavos asoma de una mesa baja, se oye el robot a lo lejos.
- **Aprende:** la aguja corta hilos; las cosas caídas cambian el camino.

### Zona 2 · La bolsa de clavos — Objetivo 2: segunda munición **[Roi]**
- **Ve:** encima, una bolsa de clavos sobresale del borde de la mesa colgando de **3 hilos** deshilachados.
- **Hace:** corta los 3 hilos con agujas. La bolsa se vuelca: **lluvia de clavos** y montañita a sus pies.
- **Obtiene:** **clavos** ilimitados en el carcaj.

### Zona 3 · La regla-puente **[Roi: hacer caer una regla para formar un puente]**
- **Ve:** un **hueco** (entre la mesa baja y la cajonera). Al otro lado, una **regla de madera** grande está de pie, inclinada hacia el jugador; no cae porque un **calzo** (una goma de borrar) frena su base.
- **Hace:** disparar una aguja a la goma: **se clava sin moverla** (enseña que la aguja no empuja). Disparar un **clavo** a la goma: el golpe **la desplaza**, la regla pierde el apoyo y **cae sobre el hueco** → puente. Cruzar.
- **Aprende:** la propiedad nueva del clavo, **golpear y empujar**, que necesitará después.
- **Falla:** si el clavo da en la regla en vez de en la goma, solo tiembla; se reintenta.

### Zona 4 · La cajonera-escalera **[Roi: peldaños, no clavos]**
- **Ve:** una **cajonera de tornillería** alta, de cajoncitos de plástico, con cajones **de apertura por presión** (se abren al empujarlos, como los muebles modernos). En lo alto, un borde seguro desde el que se domina el suelo del robot.
- **Hace:** disparar **clavos** a 3 frentes de cajón, de abajo arriba: cada golpe hace que el cajón **salte hacia fuera** y se convierte en un **peldaño**. Subir teletransportándose de cajón en cajón. Las agujas no abren los cajones: no empujan lo suficiente.
- **Peldaños lógicos:** son cajones de verdad, que sí soportan tu peso; los clavos solo los activan.
- **Falla:** un cajón mal escogido no bloquea nada; los que no son peldaño solo se abren un poco y vuelven a cerrarse.
- **Llega a:** lo alto de la cajonera, **punto seguro** frente al robot.

### Zona 5 · El robot aspirador — Objetivo 3: detenerlo **[Roi]**
- **Ve:** el robot va y viene delante de la base de la mesa, bloqueando el paso. Encima del extremo de su recorrido, en una balda, una **botella de plástico con líquido de color**. La pegatina del robot (al inspeccionarlo): *"¡No usar sobre superficies mojadas!"*.
- **Hace:**
  1. **Clavo al botón OFF** → **trampa**: botón hundido, luces de verde a rojo, ruido de avería; el robot va más rápido y **alarga su recorrido** hasta pasar bajo la botella.
  2. **Aguja (o clavo) a la botella** → chorro de color → charco.
  3. El robot pisa el charco → **chispas, se para**; la tapa salta y rueda fuera la **canica 1**.
- **Orden libre:** si perfora la botella antes, el charco se queda y el robot lo pisa al entrar en modo descontrolado.
- **Falla:** si baja al suelo y el robot le toca → fundido, vuelve a lo alto de la cajonera.
- **Obtiene:** canica 1. El jugador baja al suelo (teletransporte hacia abajo).

### Zona 6 · Base de la mesa · canicas — Objetivo 4: ascender
- **Ve:** la **canica 2** brilla en una bandejita colgada de un hilo bajo el canto de la mesa. Junto a ella, un **costurero** con un **dedal**. Arriba, en el tablero, una **diana de corcho**.
- **Hace:**
  1. **Aguja** al hilo de la bandejita → la canica 2 cae sobre una esponja.
  2. Combina **dedal + flecha** = **flecha portacanicas** **[Pendiente de confirmar: opción 2A]**.
  3. Dispara la canica 1 al suelo de madera → portal inactivo. Dispara la canica 2 a la diana de corcho → **se enlazan**.
  4. Entra en el portal → **fundido** → aparece sobre la mesa, frente a la máquina.
- **Regla:** el portal se abre **donde se clava la flecha** (madera o corcho). Si no se clava, la canica vuelve al cinto a los 2 s. "Recoger canicas" las devuelve siempre.

### Zona 7 · La máquina — Final **[Roi: péndulo]**
- **Ve:** la máquina tiene un **pulsador de seta grande** en el centro de una **bandeja en embudo**. Inspección: *"Botón de seguridad. Requiere 2 kg de presión"*. Del brazo de un flexo cuelga una **plomada** sujeta por un hilo y frenada por un **pestillo**.
- **Hace:** **clavo al pestillo** → la plomada se balancea despacio, siempre en la misma línea, sobre el botón. Cuando el botón **se ilumina**, **aguja al hilo** → la plomada cae en la bandeja, rueda al centro y pulsa el botón.
- **Falla:** si cae fuera de la bandeja, rueda a un cajón y baja otra plomada del carrete.
- **Final:** la máquina se activa, destello blanco, el taller "encoge" a tu alrededor y vuelves a tu tamaño.

> **El final en una frase:** "Solté la plomada con un clavo y, cuando pasó sobre el botón, corté el hilo con una aguja."

---

## 5. Orden de los recursos

| Recurso | Se obtiene | Primer uso | Usos posteriores |
|---|---|---|---|
| Aguja | Zona 0 | Zona 1 (hilo solapa) | 2 (hilos bolsa), 5 (botella), 6 (hilo canica), 7 (hilo plomada) |
| Clavo | Zona 2 | Zona 3 (calzo) | 4 (cajones), 5 (OFF), 7 (pestillo) |
| Canica 1 | Zona 5 | Zona 6 | Recuperable |
| Canica 2 + dedal | Zona 6 | Zona 6 | Recuperable |

Ningún recurso se pide antes de obtenerlo, y cada munición se usa al menos dos veces después de aprenderla.

---

## 6. Ritmo: alternancia de acciones

| Zona | Acción principal |
|---|---|
| 0 | Buscar y combinar |
| 1 | Disparar (cortar) y moverse |
| 2 | Puntería con consecuencia |
| 3 | Deducir (aguja no / clavo sí) |
| 4 | Disparar y escalar |
| 5 | Observar y deducir (trampa y botella) |
| 6 | Combinar y saltar |
| 7 | Puntería y sentido del momento |

---

## 7. Duración estimada (sin medir)

| Zona | Minutos |
|---|---|
| 0 · Caja y arco | 2,0 – 2,5 |
| 1 · Rampa | 0,5 – 1,0 |
| 2 · Bolsa | 1,0 – 1,5 |
| 3 · Regla-puente | 0,5 – 1,0 |
| 4 · Cajonera | 1,0 – 1,5 |
| 5 · Robot | 2,0 – 2,5 |
| 6 · Canicas | 1,5 – 2,0 |
| 7 · Máquina | 1,0 – 1,5 |
| **Total** | **9,5 – 13,5** |

Con dos zonas de clavos seguidas (3 y 4) el total roza el límite alto. **Recortes posibles, en este orden:** quitar la bandejita colgada de la canica 2 (dejarla en el suelo); reducir la cajonera a 2 cajones; fusionar zonas 1 y 2 (la rampa deja la bolsa a tiro).

---

## 8. Cambios respecto a la revisión 1

- El láser se elimina. **[Roi]**
- Nueva zona 3: regla que cae al quitar su calzo con un clavo. **[Roi]**
- Nueva zona 4: peldaños que son **cajones de apertura por presión**, no clavos. **[Roi]**
- El puente de la zona 1 pasa a ser una **rampa de cartón**, para no repetir "una regla que cae" dos veces.
- El punto seguro frente al robot es lo alto de la cajonera (antes, un libro).

---

## 9. Dudas abiertas para Codex y Roi

1. **Canicas:** confirmar la **flecha con dedal** (2A). Roi no la ha elegido explícitamente.
2. **Zona 1:** ¿rampa de cartón con hilo, o prefiere Roi el globo que mencionó al principio?
3. **Zonas 3 y 4 seguidas con clavos:** ¿se nota repetición? Alternativa: invertir el orden de la cajonera y la regla, o mover la cajonera después del robot.
4. **Cajones de apertura por presión:** ¿se entienden sin texto? Propuesta: el primero ya está entreabierto y la ficha dice "Se abre al presionar".
5. **Bajar de la cajonera tras el robot:** teletransporte hacia abajo directo. Confirmar que es cómodo.
6. **Técnicas:** caída de la regla, cajones y plomada como animaciones controladas (no física libre); comprobar la legibilidad de las fichas en Quest 3.
7. **Planificación:** fecha exacta de entrega y primera prueba con las Quest 3.
