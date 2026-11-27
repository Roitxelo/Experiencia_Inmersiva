# Flujo del juego · versión definitiva provisional

**Fecha:** 27/11/2026
**Redacta:** Claude, a partir de su [`flujo_provisional_final.md`](flujo_provisional_final.md), el [`flujo_provisional_codex.md`](flujo_provisional_codex.md) corregido, la [`revision_codex_flujo_2026-11-27.md`](revision_codex_flujo_2026-11-27.md) y las decisiones de Roi en `MEMORIA.md` (entradas 12–17).
**Estado:** **definitiva provisional**. Roi la revisa, la modifica si quiere y se cierra como definitiva. Después vendrán el mapa con medidas, la lista de objetos y el guion técnico.

Leyenda: **[Roi]** decidido por Roi · **[Codex]** aportación de Codex que se adopta · **[Nuevo]** propuesta de Claude en esta versión · **[Pendiente]** falta que Roi lo confirme.

---

## 1. Comparación de las dos versiones y qué se queda

| Tema | Flujo de Claude (27/11) | Flujo de Codex (corregido) | En esta versión |
|---|---|---|---|
| Teletransporte | Desde el principio | Solo al enlazar las dos canicas | **Codex [Roi]**: solo al final. Antes, caminar y saltar. |
| Canicas | Flecha con dedal | Canica pegada con chicle detrás de un clavo | **Codex [Roi]**: clavo + chicle. |
| Inicio | Caja de herramientas | Caja de herramientas | **[Roi + Nuevo]**: costurero volcado en el suelo. |
| Rampa | Solapa atada; la aguja corta el hilo y bajas | Igual | **[Roi + Nuevo]**: aguja con hilo que se clava en un cartón; **tiras** del hilo y la rampa **sube**. |
| Llegar al puente | Sin resolver (estabas en el suelo) | Señalado como problema | **Resuelto**: la rampa sube a la mesa baja, desde donde sale la regla-puente. |
| Bolsa de clavos | 3 hilos | 3 hilos (restaurado) | 3 hilos **[Roi]**. |
| Regla-puente | Calzo de goma desplazado con clavo | Igual | Igual. |
| Cajonera | 3 cajones | 3 cajones, alternando disparo y subida | **Codex [Roi]**: disparo → subir → disparo → subir… |
| Robot | Trampa + botella; reinicio al punto seguro | Igual; la aguja abre el punto frágil de la botella | Igual. |
| Tras el salto | "Recoger canicas" | El enlace se mantiene para poder volver | **Codex**: el enlace se queda; nunca quedas atrapado. |
| Plomada | Se repone si falla | Además: si se corta antes de balancear, se reinicia | **Codex**. |

---

## 2. Premisa y reglas

**Premisa:** despiertas diminuto (10–15 cm) en el **taller de un inventor**. Al fondo, sobre la mesa de trabajo, una **máquina** brilla y zumba: es la que te devolverá tu tamaño. **[Roi]**
**Duración objetivo:** 10–12 minutos **[Roi]**, sin medir todavía.

**Mecánicas [Roi]:**
| Acción | Con qué | Ejemplo |
|---|---|---|
| **Cortar** | Aguja | Hilos de la bolsa, botella, hilo de la plomada |
| **Tirar** | Aguja con hilo atado **[Roi, nueva]** | Arrastrar el cartón para formar la rampa |
| **Pulsar / empujar** | Clavo | Calzo de la regla, cajones, OFF del robot, pestillo |
| **Teletransporte** | Canica + clavo con chicle | Un único salto a la mesa de la máquina |

**Inventario [Roi]:** munición ilimitada. Agujas y clavos en un **carcaj detrás del hombro**. **Arco** y **canicas** en el **cinto**. El hilo sale del carrete y no se gasta.

**Movimiento [Roi]:** caminar y saltar de forma normal; el control exacto (joystick, botón de salto, opciones de comodidad) se prueba en Quest 3. **El teletransporte no existe hasta la zona 6.**

**Ayudas [Roi]:** resalte + línea fina con el nombre al apuntar; botón para inspeccionar y ver una ficha breve.

**Fallos:** nunca se pierde munición ni progreso; todo se puede reintentar. Si el robot te alcanza, vuelves a lo alto de la cajonera.

---

## 3. Mapa lógico

```
SUELO                         MESA BAJA                      CAJONERA
[0 Costurero] -> [1 Rampa] -> [2 Bolsa de clavos] -> [3 Regla-puente] -> [4 Cajones: subir]
                                                                              |
                                                                              v  (bajar por los cajones)
MESA DE TRABAJO                          SUELO
[7 Máquina] <== salto con canicas == [6 Base de la mesa] <- [5 Robot]
```

La máquina se ve desde las zonas 0, 2, 4 y 6.

---

## 4. Flujo zona por zona

### Zona 0 · El costurero volcado (inicio) — Objetivo 1: montar el arco [Roi + Nuevo]
- **Por qué está ahí:** el inventor estaba cosiendo un botón de su bata, que sigue colgada en la silla de al lado. El **costurero** se cayó de la silla y quedó volcado en el suelo.
- **Ve:** fundido desde negro. Estás tumbado entre botones del tamaño de mesas y un dedal como un barril. Al fondo, la máquina brilla sobre la mesa de trabajo.
- **Hace:** aprende a mirar, caminar, apuntar, inspeccionar y agarrar. Encuentra tres cosas del costurero:
  - un **acerico** con **agujas** (munición),
  - un **carrete de hilo** (cuerda del arco y, después, hilo para tirar),
  - una **ballena de costura**: la varilla flexible de plástico que se cose en los cuellos de camisa o los corsés. A tu escala es como la vara de un arco. **[Pendiente: confirmar el objeto flexible]**
- **Combina:** ballena + hilo = **arco**.
- **Obtiene:** arco y agujas.

### Zona 1 · La rampa del cartón — tirar del hilo [Roi + Nuevo]
- **Ve:** un trozo plano de cartón está **casi vertical**, apoyado contra el canto de la mesa baja. Así no se puede subir: está demasiado empinado.
- **Hace:**
  1. Combina **aguja + hilo del carrete** = **aguja con hilo** (una especie de arpón).
  2. Dispara a la **base** del cartón: la aguja **se clava** y el hilo queda tenso entre el cartón y tu mano.
  3. **Mecánica nueva: tirar.** Agarra el hilo y tira hacia ti (o mantén un botón para recogerlo). La base del cartón **se desliza hacia ti** y la parte alta baja apoyada en el canto: el cartón queda **inclinado como una rampa**.
  4. Sube caminando a la mesa baja.
- **Aprende:** con hilo puedes **tirar** de las cosas hacia ti, no solo cortar.
- **Falla:** si la aguja no se clava (da en el suelo o en la mesa), el hilo se recoge solo y se reintenta. Si se tira de lado, el cartón no se mueve y tiembla: pista para tirar en línea recta.
- **Lógica física:** es como una escalera apoyada en una pared; si alejas su base, queda más tumbada.

### Zona 2 · La bolsa de clavos — Objetivo 2: segunda munición [Roi]
- **Ve:** desde lo alto de la mesa baja, una bolsa de clavos sobresale de una estantería justo encima, colgando de **3 hilos** deshilachados.
- **Hace:** corta los 3 hilos con agujas. La bolsa se vuelca: **lluvia de clavos** y montañita sobre la mesa baja.
- **Obtiene:** clavos ilimitados en el carcaj.

### Zona 3 · La regla-puente [Roi]
- **Ve:** un hueco entre la mesa baja y la cajonera. Al otro lado, una **regla de madera** de pie, inclinada hacia ti, frenada por un **calzo** (una goma de borrar).
- **Hace:** una aguja se clava en la goma sin moverla (pista). Un **clavo** la desplaza de un golpe: la regla cae sobre el hueco. **Cruza caminando** por ella.
- **Falla:** si el clavo da en la regla, solo tiembla; la goma siempre sigue visible.

### Zona 4 · La cajonera-escalera [Roi + Codex]
- **Ve:** la regla te deja en el zócalo de una **cajonera de tornillería** con cajones que se abren al presionar. El primero está entreabierto como pista; su ficha dice: *"Se abre al presionar"*.
- **Hace:** clavo al primer cajón → se abre → **salta** encima. Desde ahí, clavo al segundo → salta. Igual con el tercero. Cada disparo se hace desde una altura distinta. **[Codex]**
- **Llega a:** lo alto de la cajonera, **punto seguro** desde el que se domina el suelo del robot.
- **Falla:** los cajones abiertos se quedan abiertos; los que no son peldaño se abren un poco y se cierran.

### Zona 5 · El robot aspirador — Objetivo 3: detenerlo [Roi]
- **Ve:** el robot va y viene delante de la base de la mesa de trabajo. Encima del extremo de su recorrido, una **botella de plástico con líquido de color**. Su pegatina: *"¡No usar sobre superficies mojadas!"*.
- **Hace:**
  1. **Clavo al OFF** → **trampa**: luces rojas, ruido de avería; va más rápido y alarga su recorrido hasta pasar bajo la botella.
  2. **Aguja al punto frágil** de la botella → chorro de color → charco.
  3. El robot pisa el charco → chispas, se para **para siempre**, y rueda fuera la **canica 1**.
- **Orden libre:** si la botella se perfora antes, el charco espera; el robot solo lo alcanza en modo descontrolado.
- **Falla:** si bajas y el robot te toca → vuelves a lo alto de la cajonera; lo resuelto se conserva.
- **Después:** bajas al suelo por los cajones abiertos.

### Zona 6 · Base de la mesa · canicas — Objetivo 4: ascender [Roi + Codex]
- **Ve:** la **canica 2** brilla en una bandejita colgada bajo el canto de la mesa de trabajo. Junto a ella, un **paquete de chicles** abierto. Arriba, en el tablero, una **diana de corcho**.
- **Hace:**
  1. Consigue la canica 2. **[Pendiente]** Recomiendo reutilizar la **aguja con hilo**: clavarla en la bandejita y **tirar** para bajarla (así la mecánica de tirar se usa dos veces). Alternativa: cortar su hilo con una aguja, como en la versión anterior.
  2. Pega cada canica con **chicle** detrás de un clavo.
  3. Dispara la primera a una superficie de madera cercana → portal **inactivo**.
  4. Dispara la segunda a la diana de corcho → **se enlazan**. **Se desbloquea el teletransporte.**
  5. Entra en el portal → fundido → apareces en una **zona segura y amplia** junto a la diana, mirando a la máquina.
- **Falla:** si una canica no se ancla, vuelve al cinto. "Recoger canicas" (menú de muñeca) las devuelve. Tras el salto, el enlace **se mantiene** para poder volver; nunca quedas atrapado. **[Codex]**

### Zona 7 · La máquina — Final [Roi: péndulo]
- **Ve:** **pulsador de seta grande** en el centro de una **bandeja en embudo**. Ficha: *"Botón de seguridad. Requiere 2 kg de presión"*. Del brazo de un flexo cuelga una **plomada** sujeta por un hilo y frenada por un **pestillo**.
- **Hace:** clavo al pestillo → la plomada se balancea despacio, siempre en la misma línea. Cuando el botón **se ilumina**, aguja al hilo → la plomada cae en la bandeja, rueda al centro y pulsa el botón.
- **Falla:** si cae fuera, rueda a un cajón y baja otra. Si se corta el hilo antes de soltar el pestillo, el mecanismo se reinicia. **[Codex]**
- **Final:** destello blanco, el taller "encoge" a tu alrededor y vuelves a tu tamaño.

---

## 5. Orden de los recursos y mecánicas

| Recurso / mecánica | Se obtiene | Primer uso | Usos posteriores |
|---|---|---|---|
| Aguja (cortar) | 0 | 2 (hilos de la bolsa) | 3 (pista), 5 (botella), 7 (hilo plomada) |
| Aguja con hilo (tirar) | 1 | 1 (rampa) | 6 (bandejita) **[Pendiente]** |
| Clavo (pulsar) | 2 | 3 (calzo) | 4 (3 cajones), 5 (OFF), 7 (pestillo) |
| Canicas + chicle (teletransporte) | 5 y 6 | 6 | Enlace de vuelta |

Ningún recurso se pide antes de tenerlo.

---

## 6. Ritmo

| Zona | Acción principal |
|---|---|
| 0 | Buscar, combinar, aprender a moverse |
| 1 | **Tirar** (mecánica nueva) y subir |
| 2 | Cortar con puntería |
| 3 | Deducir (aguja no, clavo sí) y cruzar |
| 4 | Pulsar y saltar, alternando |
| 5 | Observar y deducir |
| 6 | Combinar, tirar y teletransportarse |
| 7 | Sentido del momento |

---

## 7. Duración estimada (sin medir)

| Zona | Minutos |
|---|---|
| 0 · Costurero y arco | 2,0 – 2,5 |
| 1 · Rampa (tirar) | 1,0 – 1,5 |
| 2 · Bolsa | 1,0 – 1,5 |
| 3 · Regla-puente | 0,5 – 1,0 |
| 4 · Cajonera | 1,0 – 1,5 |
| 5 · Robot | 2,0 – 2,5 |
| 6 · Canicas | 1,5 – 2,0 |
| 7 · Máquina | 1,0 – 1,5 |
| **Total** | **10 – 14** |

La mecánica nueva de tirar añade algo de tiempo; el extremo alto pasa de los 12 minutos. **Recortes posibles si al medir nos pasamos**, de menos a más impacto:
1. La canica 2 está ya en el suelo (sin bandejita).
2. La bolsa cuelga de 2 hilos en vez de 3.
3. La cajonera tiene 2 cajones en vez de 3.

---

## 8. Lo que Roi debe decidir para cerrar

1. **Objeto flexible del arco:** ¿**ballena de costura** (recomendada: es de costura y es flexible), aguja de tejer de bambú, u otro?
2. **Canica 2:** ¿bajarla **tirando** con la aguja con hilo (recomendado, reutiliza la mecánica nueva) o **cortando** su hilo?
3. **Recortes de tiempo:** ¿te parece bien el orden del apartado 7 para cuando midamos?

Lo demás queda cerrado según tus decisiones. Siguen pendientes, como datos de planificación, la fecha exacta de entrega y la primera prueba con las Quest 3.
