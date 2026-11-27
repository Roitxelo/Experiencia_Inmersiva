# Flujo definitivo del juego

**Proyecto:** Experiencia inmersiva · Meta Quest 3 · WebXR + React
**Fecha de cierre:** 27/11/2026
**Estado:** **definitivo** (cerrado por Roi). Cualquier cambio posterior se registrará en `MEMORIA.md` y en este documento.
**Documento complementario:** [Guía de objetos](guia_objetos.md): qué es cada objeto, dónde está, cuándo se desbloquea, cómo se usa y qué pasa si fallas.
**Historial del debate:** [`docs/4_historico/`](../4_historico/README.md).

> Sigue siendo una versión de diseño: el mapa con medidas, la lista de modelos 3D y el guion técnico vendrán después. Los tiempos y la comodidad se validarán en las Quest 3.

---

## 1. Premisa

Despiertas **diminuto (unos 12 cm)** en el **taller de un inventor**. Todo es unas 15 veces más grande que tú. Al fondo, sobre la mesa de trabajo, una **máquina** brilla y zumba: es la que te devolverá tu tamaño.

Para llegar a ella fabricarás un **arco** con lo que encuentres en el suelo y usarás los objetos del taller a tu favor: cortar, tirar, pulsar y, al final, teletransportarte.

- **Duración objetivo:** 10–12 minutos (estimación actual: 10–14; ver apartado 8).
- **Un solo salto espacial**, al final.
- La máquina es la referencia constante: se ve desde casi todo el recorrido.

---

## 2. Los cuatro objetivos

| # | Objetivo | Zonas |
|---|---|---|
| 1 | **Montar el arco** y aprender los controles | 0 – 1 |
| 2 | **Conseguir la segunda munición** (clavos) | 2 – 4 |
| 3 | **Detener al robot aspirador** | 5 |
| 4 | **Ascender a la máquina** y activarla | 6 – 7 |

---

## 3. Reglas del juego

### 3.1 Mecánicas

| Acción | Con qué | Se desbloquea en | Se usa en |
|---|---|---|---|
| **Cortar** | Aguja | Zona 0 | Zonas 2, 5, 6 y 7 (y pista en la 3) |
| **Tirar** | Aguja con hilo atado al ovillo | Zona 1 | Solo zona 1 (el ovillo no se transporta) |
| **Pulsar / empujar** | Clavo | Zona 2 | Zonas 3, 4, 5 y 7 |
| **Teletransportarse** | Canica pegada con chicle detrás de un clavo | Zona 6 | Solo zona 6 (un salto) |

### 3.2 Movimiento
- **Caminar y saltar** de forma normal desde el principio. El control exacto (joystick, botón de salto, giro por pasos y opciones de comodidad) se fijará al probar en Quest 3.
- **No hay teletransporte** hasta enlazar las dos canicas en la zona 6.

### 3.3 Inventario
- **Munición ilimitada.** Agujas y clavos salen de un **carcaj detrás del hombro**: se lleva la mano atrás, se agarra y aparece la flecha. El joystick cambia de munición; la punta visible indica cuál está cargada.
- **Cinto:** el **arco** se cuelga en la cadera cuando no se usa; las **canicas** van en una bolsita.
- **Menú de muñeca:** libreta con los objetos descubiertos y la acción **"Recoger canicas"**.

### 3.4 Ayudas
- Al apuntar a un objeto interactuable: **se resalta** y una **línea fina** lo une a su **nombre**.
- Un botón permite **inspeccionarlo**: ficha breve con qué hace, cómo se usa y con qué se combina (textos en la [guía de objetos](guia_objetos.md)).

### 3.5 Fallos
- Nunca se pierde munición ni progreso. Todo puzle se puede reintentar sin límite.
- Lo que se abre o cae (rampa, regla, cajones) **se queda así**.
- Si el robot te alcanza, vuelves a lo alto de la cajonera.

---

## 4. Mapa lógico

```
SUELO                                MESA BAJA                         CAJONERA
[0 Costurero] -> [1 Rampa de cartón] -> [2 Bolsa de clavos] -> [3 Regla-puente] -> [4 Cajones: subir]
                                                                                        |
                                                                          (bajar por los cajones)
                                                                                        v
MESA DE TRABAJO                                 SUELO
[7 Máquina y plomada] <== salto con canicas == [6 Base de la mesa] <- [5 Robot aspirador]
```

---

## 5. El recorrido, de principio a fin

### Zona 0 · El costurero volcado — inicio (Objetivo 1)
**Contexto:** el inventor estaba cosiendo un botón de su bata, que sigue colgada en la silla de al lado. El costurero se cayó y quedó volcado en el suelo; junto a él, un clip caído del banco.

1. **Fundido desde negro.** Estás en el suelo entre botones del tamaño de mesas y un dedal como un barril. Al fondo brilla la máquina.
2. **Aprendes a mirar, caminar, apuntar, inspeccionar y agarrar** con los tres objetos que tienes a pocos pasos: **acerico con agujas**, **ovillo de hilo** y **clip**.
3. **Abres el clip:** agarras cada punta con una mano y las separas hasta que toma forma de arco (un contorno indica la forma final; crujido metálico y vibración en ambos mandos).
4. **Atas el hilo** del ovillo a las dos puntas: **ya tienes el arco**. Las agujas pasan al carcaj.

*Aprendes:* moverte, agarrar, usar las dos manos a la vez. *Obtienes:* arco y agujas.

### Zona 1 · La rampa de cartón — tirar del hilo (Objetivo 1)
1. Ves un cartón plano **casi vertical**, apoyado contra el canto de la mesa baja: demasiado empinado para subir.
2. Junto al ovillo, **atas su hilo a una aguja**: aguja con hilo.
3. **Disparas a la base del cartón:** la aguja se clava y el hilo queda tenso hasta tu mano.
4. **Tiras del hilo** hacia ti: la base se desliza y el cartón queda inclinado como una escalera apoyada en una pared.
5. **Subes caminando** a la mesa baja. El ovillo se queda abajo.

*Aprendes:* disparar y que el hilo sirve para tirar. *Llegas a:* la mesa baja.

### Zona 2 · La bolsa de clavos (Objetivo 2)
1. Desde la mesa baja ves, justo encima, una **bolsa de clavos** que sobresale de una estantería colgando de **2 hilos deshilachados**.
2. **Cortas los 2 hilos con agujas.**
3. La bolsa se vuelca: **lluvia de clavos** y montañita a tus pies.

*Obtienes:* clavos ilimitados en el carcaj.

### Zona 3 · La regla-puente (Objetivo 2)
1. Un **hueco** separa la mesa baja de la cajonera. Al otro lado, una **regla de madera** de pie, inclinada hacia ti, frenada por una **goma de borrar** que hace de calzo.
2. Si disparas una aguja a la goma, **se clava pero no la mueve** (pista: hace falta algo más pesado).
3. **Un clavo desplaza la goma**: la regla cae sobre el hueco y forma un puente.
4. **Cruzas caminando.**

*Aprendes:* el clavo empuja lo que la aguja no puede mover.

### Zona 4 · La cajonera-escalera (Objetivo 2)
1. La regla te deja en el zócalo de una **cajonera de tornillería** con cajones que se abren al presionar. El primero está entreabierto como pista.
2. **Clavo al primer cajón** → se abre → **saltas encima**.
3. Desde ahí, **clavo al segundo** → saltas. Igual con el **tercero**.
4. Llegas a lo **alto de la cajonera**: punto seguro desde el que se domina el suelo del robot.

### Zona 5 · El robot aspirador (Objetivo 3)
1. Desde arriba ves al **robot** ir y venir delante de la base de la mesa de trabajo, bloqueando el paso. Sobre el extremo de su recorrido, en una balda, una **botella de plástico con líquido de color**. La pegatina del robot avisa: *"¡No usar sobre superficies mojadas!"*.
2. **Clavo al botón OFF** → **trampa**: luces rojas, ruido de avería; el robot acelera y **alarga su recorrido** hasta pasar bajo la botella.
3. **Aguja al punto frágil de la botella** → chorro de color → **charco**.
4. El robot pisa el charco → **chispas y se para para siempre**. Su tapa salta y rueda fuera la **canica 1**, que era su fuente de energía.
5. **Bajas** al suelo por los cajones abiertos y recoges la canica 1.

*Orden libre:* si perforas la botella antes de pulsar OFF, el charco espera; el robot solo llega a él en modo descontrolado.

### Zona 6 · La base de la mesa: las canicas (Objetivo 4)
1. Bajo el canto de la mesa de trabajo cuelga una **bandejita** con la **canica 2**. Junto a ella, un **paquete de chicles** abierto. Arriba, en el tablero, una **diana de corcho**.
2. **Aguja al hilo de la bandejita** → la canica 2 cae sobre una esponja.
3. **Pegas cada canica con chicle** detrás de un clavo.
4. **Disparas la primera** a una superficie de madera cercana → portal **inactivo**.
5. **Disparas la segunda** a la diana de corcho → los portales **se enlazan**. **Se desbloquea el teletransporte.**
6. **Entras en el portal** → fundido → apareces en una zona segura y amplia de la mesa, mirando a la máquina.

### Zona 7 · La máquina y la plomada — final (Objetivo 4)
1. La máquina tiene un **pulsador de seta grande** en el centro de una **bandeja en embudo**. Su ficha: *"Botón de seguridad. Requiere 2 kg de presión"*: tú no pesas tanto.
2. Del brazo de un flexo cuelga una **plomada** sujeta por un hilo y frenada por un **pestillo**.
3. **Clavo al pestillo** → la plomada se balancea despacio, siempre en la misma línea, sobre la máquina.
4. Cuando el botón **se ilumina** (la plomada está encima), **aguja al hilo** → la plomada cae en la bandeja, rueda al centro y **pulsa el botón**.
5. **Final:** destello blanco, el taller "encoge" a tu alrededor y vuelves a tu tamaño.

> **El final en una frase:** "Solté la plomada con un clavo y, cuando pasó sobre el botón, corté el hilo con una aguja."

---

## 6. Calendario de desbloqueos

| Momento | Se desbloquea | Queda disponible hasta |
|---|---|---|
| Zona 0 · inicio | Mirar, caminar, saltar, agarrar, inspeccionar | Final |
| Zona 0 · abrir el clip y atar hilo | **Arco** + **agujas** (cortar) | Final |
| Zona 1 · atar la aguja al ovillo | **Aguja con hilo** (tirar) | Fin de la zona 1 |
| Zona 2 · caída de la bolsa | **Clavos** (pulsar / empujar) | Final |
| Zona 5 · cortocircuito del robot | **Canica 1** | Final (recuperable) |
| Zona 6 · cortar la bandejita | **Canica 2** + **chicle** | Final (recuperable) |
| Zona 6 · enlazar las canicas | **Teletransporte** (un salto) | Final |

---

## 7. Qué pasa si fallas

| Situación | Qué ocurre |
|---|---|
| Fallas un disparo | La flecha cae o se clava; sacas otra del carcaj. |
| La aguja con hilo no se clava en el cartón | El hilo se recoge solo; reintentas. |
| Tiras del hilo en mala dirección | El cartón tiembla sin moverse: pista para tirar en línea recta. |
| El clavo da en la regla y no en la goma | La regla tiembla; la goma sigue visible. |
| Disparas a un cajón que no es peldaño | Se abre un poco y vuelve a cerrarse. |
| El robot te alcanza | Fundido: vuelves a lo alto de la cajonera, con todo lo resuelto. |
| Perforas la botella antes de pulsar OFF | El charco se queda; funciona igual. |
| Una canica no se ancla | Vuelve al cinto a los 2 s. |
| Canicas mal colocadas | "Recoger canicas" (menú de muñeca) las devuelve. |
| Después del salto | El enlace se mantiene para poder volver: nunca quedas atrapado. |
| Cortas la plomada antes de soltar el pestillo | El mecanismo se reinicia. |
| La plomada cae fuera de la bandeja | Rueda a un cajón y baja otra. |

---

## 8. Ritmo y duración

| Zona | Acción principal | Minutos (estimados, sin medir) |
|---|---|---|
| 0 · Costurero | Buscar, combinar, aprender a moverse | 2,0 – 2,5 |
| 1 · Rampa | Disparar y tirar | 1,0 – 1,5 |
| 2 · Bolsa | Cortar con puntería | 1,0 – 1,5 |
| 3 · Regla-puente | Deducir y cruzar | 0,5 – 1,0 |
| 4 · Cajonera | Pulsar y saltar | 1,0 – 1,5 |
| 5 · Robot | Observar y deducir | 2,0 – 2,5 |
| 6 · Canicas | Cortar, combinar, teletransportarse | 1,5 – 2,0 |
| 7 · Máquina | Sentido del momento | 1,0 – 1,5 |
| **Total** | | **10 – 14** |

**Recortes si al medir nos pasamos** (orden aprobado por Roi; se pueden ampliar más adelante):
1. La canica 2 ya está en el suelo (sin bandejita).
2. La bolsa cuelga de 2 hilos en vez de 3.
3. La cajonera tiene 2 cajones en vez de 3.

---

## 9. Requisitos del enunciado cubiertos

| Requisito del reto | Dónde se cumple |
|---|---|
| Escena 3D | Todo el taller |
| Acceso desde el navegador del visor | Aplicación WebXR (React Three Fiber + `@react-three/xr`), servida por HTTPS |
| Iniciar una sesión inmersiva | Botón "Entrar en VR" antes de la zona 0 |
| Al menos tres objetos | Zona 0: acerico, ovillo y clip (y muchos más después) |
| Seleccionar o activar un objeto | Resalte, inspección y agarre desde la zona 0 |
| Respuesta visual a la selección | Resalte, línea con nombre, ficha; cada puzle tiene consecuencia visible |
| Respuesta visual o sonora (hito 5) | Crujido del clip, lluvia de clavos, chispas del robot, destello final |

---

## 10. Pendiente fuera del diseño
- Fecha exacta de entrega y primera prueba en las Quest 3.
- Mapa con medidas, lista de modelos 3D y guion técnico (siguiente fase).
