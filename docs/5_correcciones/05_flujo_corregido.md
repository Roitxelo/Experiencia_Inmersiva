# Flujo del juego · versión 2 (corregida)

**Proyecto:** Experiencia inmersiva · Meta Quest 3 · WebXR + React
**Fecha:** 27/11/2026
**Estado:** **propuesta corregida, pendiente de revisión de Roi y Codex.** Sustituirá a [`docs/3_diseno/flujo_definitivo.md`](../3_diseno/flujo_definitivo.md) cuando Roi la cierre. Hasta entonces, el definitivo no se toca.
**Corrige:** los errores de la [lista de errores](01_lista_errores.md). Cada cambio lleva su código (E01…E31).
**Documentos de apoyo:** [guía de objetos corregida](06_guia_objetos_corregida.md) · [cotas y mapa](03_cotas_y_mapa.md) · [controles, confort e interfaz](04_controles_confort_interfaz.md).

> Sigue siendo diseño. Las medidas son orientativas y se fijan en el mapa. Los controles y la comodidad se validan en la fase 0 (apartado 11).

---

## 1. Premisa

Despiertas **diminuto (12 cm)** en el **taller de un inventor**. Todo se ve **15 veces más grande** (E05). Al fondo, sobre la mesa de trabajo, una **máquina** brilla y zumba: es la que te devolverá tu tamaño.

Para llegar a ella fabricarás un **arco** con lo que encuentres en el suelo y usarás los objetos del taller a tu favor: cortar, tirar, pulsar y, al final, teletransportarte.

- **Duración objetivo:** 10–12 minutos. La estimación sin medir es de 10–14; se mide en la capa 2 (apartado 8, E22).
- **Un solo salto espacial**, al final: un único par de portales en todo el juego (E14).
- La máquina se ve desde el inicio, la mesa baja y lo alto de la cajonera.

---

## 2. Los cuatro objetivos

| # | Objetivo | Zonas |
|---|---|---|
| 1 | **Montar el arco** y aprender los controles | 0 – 1 |
| 2 | **Conseguir los clavos y aprender a usarlos** (E27) | 2 – 4 |
| 3 | **Detener al robot aspirador** | 5 |
| 4 | **Ascender a la máquina** y activarla | 6 – 7 |

---

## 3. Reglas del juego

### 3.1 Mecánicas

| Acción | Con qué | Se desbloquea en | Se usa en |
|---|---|---|---|
| **Cortar / perforar** | Aguja | Zona 0 | Zonas 2, 5, 6 y 7 (y pista en la 3) |
| **Tirar** | Aguja con hilo atado al ovillo | Zona 1 | Solo zona 1: el ovillo no se transporta (decisión de Roi, E10) |
| **Pulsar / empujar** | Clavo | Zona 2 | Zonas 3, 4, 5 y 7 |
| **Teletransportarse** | Canica pegada con chicle en la cabeza de un clavo | Zona 6 | Solo zona 6 (un salto) |

**Proyectil** es el nombre general de lo que se dispara: una aguja o un clavo. No hay flechas (E17).

### 3.2 Movimiento y controles (E07, E08)
- **Caminar** con el joystick izquierdo, **girar por pasos** con el derecho, **saltar** con A.
- **No hay teletransporte** hasta enlazar las dos canicas en la zona 6.
- Confort por defecto: viñeta al moverse y saltar, y giro por pasos. Opcionales: saltos asistidos, giro suave y modo sentado.
- Mapa completo de mandos en [04](04_controles_confort_interfaz.md).

### 3.3 Inventario
- **Munición ilimitada.** Agujas y clavos salen de un **carcaj detrás del hombro**: llevas la mano atrás, agarras y aparece el proyectil. **La munición se cambia con el botón X**. La punta visible indica cuál está cargada (E07).
- **Cinto:** el **arco** se cuelga en la cadera cuando no se usa. Las **canicas** van en una bolsita.
- **Menú de muñeca:** libreta de objetos descubiertos, **"Recoger canicas"** (solo antes del salto) y **"Volver al último punto seguro"**.

### 3.4 Ayudas
- Al apuntar a un objeto interactuable, **se resalta** y una **línea fina** lo une a su **nombre**.
- Con B lo **inspeccionas**: aparece una ficha breve, fija en el espacio, con qué hace, cómo se usa y con qué se combina (E12).
- Solo se resalta lo que se puede usar en ese momento (E06, E16).

### 3.5 Fallos y caídas (E09)
- Nunca se pierde munición ni progreso. Todo puzle se puede reintentar sin límite.
- Lo que se abre o cae (rampa, regla, cajones) **se queda así**.
- **Si caes fuera del recorrido** o el robot te alcanza: fundido de 0,5 s y vuelves al **último punto seguro**. Bajar un solo peldaño no cuenta como caída.

---

## 4. Mapa lógico

```
SUELO (rincón cerrado)        MESA BAJA (25 cm)                 CAJONERA
[0 Costurero] -> [1 Rampa] -> [2 Bolsa de clavos] -> [3 Regla] -> [repisa 25] -> [4 tres cajones: subir a 49]
                                                                                        |
                                                                (escalera de cajones abiertos, lado del robot)
                                                                                        v
MESA DE TRABAJO (90 cm)                         SUELO (pasillo)
[7 Máquina y plomada] <== portal de canicas == [6 Base de la mesa] <- [5 Pasillo del robot]
```

Medidas, planta y reglas de conexión en [03_cotas_y_mapa.md](03_cotas_y_mapa.md) (E01, E31).

---

## 5. El recorrido, de principio a fin

### Zona 0 · El costurero volcado: inicio (Objetivo 1)
**Contexto:** el inventor estaba cosiendo un botón de su bata, que sigue colgada en la silla de al lado. El costurero se cayó y quedó volcado en el suelo, y junto a él hay un clip caído del banco. Es un **rincón cerrado** por la pared, el costurero, la silla con la bata hasta el suelo y una caja grande. La única salida es la rampa de cartón (E31).

1. **Fundido desde negro.** Estás en el suelo, entre botones como tapas de alcantarilla y un dedal como una papelera (E05). Al fondo brilla la máquina.
2. **Aprendes a mirar, caminar, apuntar, inspeccionar y agarrar** con los tres objetos que tienes a pocos pasos: **acerico con agujas**, **goma elástica** y **clip** (E03).
3. **Agarras el acerico:** las agujas pasan al carcaj (E19).
4. **Abres el clip:** agarras cada punta con una mano y las separas hasta que toma forma de arco. Un contorno indica la forma final, y hay crujido metálico y vibración en ambos mandos.
5. **Estiras la goma** entre las dos puntas: **ya tienes el arco**. Ahora puedes disparar las agujas (E03, E19).
6. **Primer disparo** a un blanco evidente (un carrete vacío). Aprendes a tensar y soltar.

*Aprendes:* a moverte, agarrar, usar las dos manos a la vez y disparar. *Obtienes:* arco y agujas.

### Zona 1 · La rampa de cartón: tirar del hilo (Objetivo 1)
1. Ves un **cartón casi vertical**, apoyado contra el canto de la mesa baja y **sobresaliendo por encima del tablero** como una valla: demasiado empinado. Abajo tiene un **asa** recortada (E02).
2. Al pie del cartón está el **ovillo**, que rodó hasta allí. Con el arco montado, su ficha sugiere: *"Atado a una aguja, podrías tirar de algo"* (E16).
3. **Atas su hilo a una aguja:** aguja con hilo.
4. **Disparas al asa:** la aguja la atraviesa y se traba, y el hilo queda tenso hasta tu mano.
5. **Tiras del hilo** hacia ti: la base se desliza hasta un tope y el cartón queda a unos 35°, apoyado en el borde de la mesa.
6. **Subes caminando** a la mesa baja. El ovillo se queda abajo.

*Aprendes:* que el hilo sirve para tirar. *Llegas a:* la mesa baja.

### Zona 2 · La bolsa de clavos (Objetivo 2)
1. Desde la mesa baja ves, justo encima, una **bolsa de clavos** que sobresale de una estantería, colgando de **3 hilos deshilachados** (E30).
2. **Cortas los 3 hilos con agujas.**
3. La bolsa se vuelca: **lluvia de clavos** y una montañita a tus pies.

*Obtienes:* clavos ilimitados en el carcaj. Con X cambias entre aguja y clavo.

### Zona 3 · La regla-puente (Objetivo 2)
1. Un **hueco** separa la mesa baja de la **repisa** de la cajonera, que está a la misma altura. En la repisa hay una **regla de madera** de pie, inclinada hacia ti, frenada por una **goma de borrar** que hace de calzo (E01).
2. Si disparas una aguja a la goma, **se clava pero no la mueve**. Es la pista de que hace falta algo más pesado.
3. **Un clavo desplaza la goma:** la regla cae sobre el hueco y forma un puente.
4. **Cruzas caminando.** Si caes al hueco, vuelves al último punto seguro (E09).

*Aprendes:* que el clavo empuja lo que la aguja no puede mover.

### Zona 4 · La cajonera-escalera (Objetivo 2)
1. Desde la repisa ves, encima, el módulo de **cajones de tornillería**, que se abren al presionar. El primero está entreabierto como pista.
2. **Clavo al primer cajón:** se abre y **saltas encima**.
3. Desde ahí, **clavo al segundo** y saltas. Igual con el **tercero**.
4. Llegas a **lo alto de la cajonera** (49 cm): un punto seguro desde el que se domina el pasillo del robot.

### Zona 5 · El robot aspirador (Objetivo 3)
1. Desde arriba ves al **robot** ir y venir por un **pasillo** que lleva a la base de la mesa de trabajo. **Ocupa todo el ancho**, así que no hay forma de pasar (E11). Deja una **franja limpia** en el polvo que marca su recorrido normal (E13).
2. Más allá del final de la franja, en una balda, hay una **botella de plástico con líquido de color**. Junto a la pared, la **base de carga** del robot, quieta, lleva la pegatina *"¡No usar sobre superficies mojadas!"* (E12), que también está en el propio robot.
3. **Clavo al botón OFF:** es una **trampa**. Luces rojas y ruido de avería: el robot acelera y **alarga su recorrido** hasta pasar bajo la botella.
4. **Aguja al punto frágil de la botella** (solo aguja; el clavo rebota, E18): chorro de color y **charco**.
5. El robot pisa el charco: **saltan chispas y se para para siempre**. Su tapa salta y rueda fuera la **canica 1**, que era su fuente de energía.
6. **Bajas** al pasillo por la **escalera de cajones abiertos** del otro lado de la cajonera y recoges la canica 1 (E01).

*Orden libre:* si perforas la botella antes de pulsar OFF, el charco se queda **fuera de la franja limpia**, y la ficha dice *"El robot nunca llega hasta aquí"* (E13).
*Si bajas antes de pararlo:* el robot te alcanza y vuelves a lo alto de la cajonera.

### Zona 6 · La base de la mesa: las canicas (Objetivo 4)
1. Del canto de la mesa de trabajo cuelga una **bandejita** con la **canica 2**, encima de una esponja. Junto a la pata hay un **paquete de chicles** abierto (E20). Arriba, **de pie en el borde del tablero y de cara al suelo**, una **diana de corcho** (E15).
2. **Aguja al hilo de la bandejita:** la canica 2 cae sobre la esponja.
3. **Pegas cada canica con chicle en la cabeza de un clavo.** Al tensar, la goma empuja la canica, que hace de culata (E04).
4. **Disparas una canica a una pata de madera** de la mesa y **otra a la diana**, en cualquier orden. La primera abre un portal **inactivo**. Con la segunda, los portales **se enlazan**: **se desbloquea el teletransporte** (E15).
5. **Caminas hacia el portal** (un disco vertical en la pata): fundido y apareces en una zona segura y amplia del tablero, mirando a la máquina.

*Si las dos canicas quedan abajo:* brillan pero no se enlazan, y la ficha dice *"Una tiene que quedar arriba"*. "Recoger canicas" las devuelve.

### Zona 7 · La máquina y la plomada: final (Objetivo 4)
1. La máquina tiene un **pulsador de seta grande** en el centro de una **bandeja en embudo**. Su ficha: *"Botón de seguridad. Requiere 150 g de presión."* Tú pesas unos 20 g (E05).
2. Del brazo de un flexo cuelga una **plomada** de 200 g. Un **pestillo** la retiene **levantada y apartada a un lado** (E06).
3. **Clavo al pestillo:** la plomada se suelta y se balancea despacio, siempre en la misma línea, **por encima de la bandeja**.
4. Ahora el hilo se resalta. **Aguja al hilo** mientras oscila. El botón se ilumina cuando la plomada pasa por el centro, como ayuda. La plomada cae en la bandeja, rueda al centro y **pulsa el botón**.
5. **Final:** destello blanco, el taller "encoge" a tu alrededor y vuelves a tu tamaño. Pantalla final con tu tiempo.

> **El final en una frase:** "Solté la plomada con un clavo y, mientras se balanceaba sobre el botón, corté su hilo con una aguja."

---

## 6. Calendario de desbloqueos

| Momento | Se desbloquea | Queda disponible hasta |
|---|---|---|
| Zona 0 · inicio | Mirar, caminar, saltar, agarrar, inspeccionar | Final |
| Zona 0 · agarrar el acerico | **Agujas** en el carcaj (E19) | Final |
| Zona 0 · clip abierto + goma | **Arco**: ya se pueden disparar agujas (cortar) | Final |
| Zona 1 · atar una aguja al ovillo (con arco) | **Aguja con hilo** (tirar) | Fin de la zona 1 |
| Zona 2 · caída de la bolsa | **Clavos** (pulsar / empujar) | Final |
| Zona 5 · cortocircuito del robot | **Canica 1** | Final (recuperable) |
| Zona 6 · cortar la bandejita | **Canica 2** | Final (recuperable hasta el salto) |
| Zona 6 · enlazar las canicas | **Teletransporte** (un salto) | Final |

El chicle no se desbloquea: es material fijo de la zona 6 (E20).

---

## 7. Qué pasa si fallas

| Situación | Qué ocurre |
|---|---|
| Fallas un disparo | El proyectil cae o se clava; sacas otro del carcaj. |
| Sueltas el clip a medio abrir | Se queda así; puedes seguir abriéndolo. |
| Intentas atar el ovillo sin tener arco | El ovillo no se resalta como combinable (E16). |
| La aguja con hilo no entra en el asa | El hilo se recoge solo; reintentas. |
| Tiras del hilo en mala dirección | El cartón tiembla sin moverse: es la pista para tirar en línea recta. |
| El clavo da en la regla y no en la goma | La regla tiembla; la goma sigue visible. |
| Disparas a un cajón que no es peldaño | Se abre un poco y vuelve a cerrarse. |
| **Caes fuera del recorrido** | Fundido y vuelves al último punto seguro (E09). |
| Bajas al pasillo con el robot en marcha | Te alcanza: vuelves a lo alto de la cajonera, con todo lo resuelto. |
| Perforas la botella antes de pulsar OFF | El charco se queda fuera de la franja limpia; funciona igual después del OFF (E13). |
| El clavo da en la botella | Rebota sin efecto (E18). |
| Una canica no se ancla | Vuelve al cinto a los 2 s. |
| Las dos canicas quedan abajo | No se enlazan; "Recoger canicas" las devuelve (E15). |
| Después del salto | El enlace se mantiene, pero ya no se pueden recoger las canicas: nunca quedas atrapado (E14). |
| Disparas al hilo de la plomada antes de soltar el pestillo | No se resalta ni se corta (E06). |
| Fallas el hilo mientras oscila | Sigue oscilando; vuelves a disparar. |

---

## 8. Ritmo y duración

| Zona | Acción principal | Minutos (estimados, sin medir) |
|---|---|---|
| 0 · Costurero | Buscar, combinar, aprender a moverse y disparar | 2,0 – 2,5 |
| 1 · Rampa | Disparar y tirar | 1,0 – 1,5 |
| 2 · Bolsa | Cortar con puntería | 1,0 – 1,5 |
| 3 · Regla-puente | Deducir y cruzar | 0,5 – 1,0 |
| 4 · Cajonera | Pulsar y saltar | 1,0 – 1,5 |
| 5 · Robot | Observar, deducir y bajar | 2,0 – 2,5 |
| 6 · Canicas | Cortar, combinar, teletransportarse | 1,5 – 2,0 |
| 7 · Máquina | Puntería con el momento justo | 1,0 – 1,5 |
| **Total** | | **10 – 14** |

**Cuándo medir:** al terminar la capa 2 (zonas 0–3) con dos o tres personas. Si esas zonas ya pasan de 5 min, se aplican recortes.

**Recortes si nos pasamos** (orden aprobado por Roi):
1. La canica 2 ya está en el suelo (sin bandejita).
2. La bolsa cuelga de 2 hilos en vez de 3.
3. La cajonera tiene 2 cajones de subida en vez de 3.

---

## 9. Requisitos del enunciado cubiertos

| Requisito del reto | Dónde se cumple |
|---|---|
| Escena 3D | Todo el taller |
| Acceso desde el navegador del visor | Aplicación WebXR (React Three Fiber + `@react-three/xr`), servida por HTTPS |
| Iniciar una sesión inmersiva | Pantalla de inicio con comprobación de compatibilidad y botón "Entrar en VR" |
| Al menos tres objetos | Zona 0: acerico, goma elástica y clip (y muchos más después) |
| Seleccionar o activar un objeto | Resalte, inspección y agarre desde la zona 0 |
| Respuesta visual a la selección | Resalte, línea con nombre y ficha; cada puzle tiene una consecuencia visible |
| Respuesta visual o sonora (hito 5) | Crujido del clip, lluvia de clavos, chispas del robot, destello final |
| Respuesta de la interfaz React (prueba 3) | Inicio, opciones, menú de muñeca, pantalla final ([04](04_controles_confort_interfaz.md#4-interfaz-react), E24) |

---

## 10. Estado de las decisiones

- **Clip como arco:** definitivo en diseño; se valida en el prototipo de la fase 0 (E26).
- **Cuerda de goma elástica:** decidida por Roi el 27/11/2026 (E03).
- **Mapa de mandos y confort:** propuesta; se valida en la fase 0 (E07, E08).

---

## 11. Siguiente paso: fase 0 antes del mapa (E23)

1. Confirmar con el profesor el modelo de visor y si la memoria va en gallego (E28).
2. Prototipo mínimo en el visor: escena con 3 objetos seleccionables, arco a dos manos contra una diana, caminar y saltar entre dos plataformas con viñeta, y medir los FPS.
3. Con el resultado, cerrar el mapa de mandos y el confort y pasar al mapa con medidas ([03](03_cotas_y_mapa.md)).
4. Construir por capas: capa 1 = zona 0 · capa 2 = zonas 1–3 · capa 3 = zonas 4–5 · capa 4 = zonas 6–7.
