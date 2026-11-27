# Cotas y bases para el mapa

Las medidas están en **centímetros reales** y, entre paréntesis, en **metros percibidos** por el jugador (×15). Son **orientativas**: el mapa con medidas las ajustará, pero debe respetar las **relaciones** (qué está a la misma altura, qué conecta con qué y qué no se puede atravesar).

Resuelve E01, E02, E05, E09, E11, E15 y E31.

---

## 1. Escala

- El jugador mide **12 cm** (1,80 m percibidos). Factor **×15**.
- Su peso a esa escala es de unos **20 g** (el peso baja con el cubo del tamaño).

| Objeto | Real | Percibido | Cómo describirlo |
|---|---|---|---|
| Botón de la bata | 2 cm | 30 cm | como una tapa de alcantarilla |
| Dedal | 2 cm alto | 30 cm | como una papelera |
| Aguja de coser (proyectil) | 4 cm | 60 cm | como una jabalina corta |
| Clavo (proyectil) | 3 cm | 45 cm | como una estaca |
| Clip grande abierto (arco) | ~9 cm de punta a punta | ~1,35 m | un arco corto |
| Goma elástica de mercería | ~10 cm | ~1,5 m | cuerda del arco |
| Canica | 1,6 cm | 24 cm | como un balón |
| Regla | 30 cm | 4,5 m | un puente |
| Robot aspirador | 34 × 9 cm | 5,1 × 1,35 m | un coche pequeño |
| Botellín de plástico | 15 cm | 2,25 m | un depósito |
| Plomada | 4 cm, 200 g | 60 cm | pesa unas 10 veces más que tú |
| Botón final | — | — | *"requiere 150 g de presión"* |

---

## 2. Alturas (corte lateral)

```
cm reales
 90 ┤                                   ┌────── MESA DE TRABAJO (Z7) ── máquina, flexo, diana en el borde
    │                                   │
 70 ┤                                   │  ← bandejita con canica 2 colgando del canto (Z6)
    │                                   │
 49 ┤             ┌──┐ alto cajonera    │
 41 ┤             │▭ │ 3 cajones de     │
 33 ┤             │▭ │ subida (Z4)  ┌▭┐ │  ← escalera de cajones abiertos (bajada, lado del robot)
 25 ┤ ┌─MESA BAJA─┤  ├─repisa────┐  │▭│ │      balda con botella a ~35 cm (Z5)
    │ │ (Z2)    ═══regla (Z3)═══ │  │▭│ │
    │ │╲ cartón │   hueco        │  │▭│ │
  0 ┼─┴─╲───────┴───(caída)──────┴──┴▭┴─┴── PASILLO DEL ROBOT (Z5) → BASE DE LA MESA (Z6)
      Z0-Z1 (rincón cerrado)
```

| Nivel | Altura real | Percibida | Qué hay |
|---|---|---|---|
| Suelo del inicio (rincón) | 0 | 0 | Z0 costurero, Z1 pie del cartón y ovillo |
| Mesa baja | 25 | 3,75 m | Z2 bolsa de clavos (encima, en una estantería a ~45 cm) |
| Repisa de la cajonera | 25 | 3,75 m | Llegada de la regla (Z3) e inicio de la subida (Z4) |
| Cajones de subida | 33 / 41 / 49 | 5 / 6,15 / 7,35 m | Peldaños abiertos con clavo |
| Alto de la cajonera | 49 | 7,35 m | Punto seguro frente al robot (Z5) |
| Balda de la botella | ~35 | 5,25 m | Sobre el final del recorrido largo del robot |
| Suelo del pasillo | 0 | 0 | Robot (Z5) y base de la mesa (Z6) |
| Bandejita de la canica 2 | ~70 | 10,5 m | Cuelga del canto del tablero, sobre una esponja |
| Tablero de la mesa de trabajo | 90 | 13,5 m | Diana, zona segura, máquina, flexo (Z7) |

**Cajonera:** dos módulos apilados. El de abajo (0–25 cm) es más ancho y su techo forma la **repisa**. El de arriba (25–49 cm) tiene los cajones.
- **Cara de la mesa baja:** tres cajones cerrados que se abren con clavo (subida).
- **Cara del robot:** cajones **ya abiertos en escalera**, unos 6 escalones de ~8 cm, desde lo alto hasta el suelo del pasillo (bajada).

**Cartón:** 50 cm. Al empezar está casi vertical y sobresale unos 24 cm por encima de la mesa baja. Al tirar queda a unos 35°, frenado por un tope de madera en el suelo. Tiene un **asa** en la base, que es el blanco de la aguja con hilo.

**Regla:** 30 cm, sobre un hueco de unos 25 cm (3,75 m percibidos). El suelo del hueco es zona de caída.

---

## 3. Planta (vista desde arriba)

```
 PARED ───────────────────────────────────────────────────────────────────────
 │  estantería (bolsa de clavos)        base de carga        balda (botella)
 │  ┌───────────┐ hueco ┌──────────┐ ║═════════ PASILLO DEL ROBOT ═══════════║
 │  │ MESA BAJA │═regla═│ CAJONERA │ ║  ◄── recorrido normal (franja limpia) ─► ║·· recorrido largo
 │  │   Z2      │  Z3   │  Z4 / Z5 │ ║══════════════════════════╗           ║
 │  └─────▲─────┘       └──────────┘                            ║ MESA DE    ║
 │   cartón Z1   ovillo                                         ║ TRABAJO    ║
 │  ┌──────────────────────┐                                    ║ Z6 abajo   ║
 │  │ RINCÓN DE INICIO  Z0 │  ← cerrado por costurero, silla    ║ Z7 arriba  ║
 │  │ costurero · silla    │    con bata y caja grande          ╚════════════╝
 │  └──────────────────────┘
```

**Reglas de conexión (lo que el mapa no puede romper):**
1. Del rincón de inicio solo se sale por la rampa de cartón (E31).
2. De la mesa baja solo se sale por la regla.
3. Del alto de la cajonera solo se baja por la escalera de cajones abiertos, que llega al pasillo.
4. El pasillo es el único camino hacia la base de la mesa, y el robot ocupa todo su ancho (E11).
5. La botella está más allá del final de la franja limpia (E13).
6. A la mesa de trabajo solo se llega por el portal.
7. La máquina se ve desde el rincón de inicio, la mesa baja y lo alto de la cajonera: la mesa de trabajo es el mueble más alto y el flexo la ilumina.

---

## 4. Puntos seguros y zonas de caída

Si caes fuera del recorrido: fundido de 0,5 s y reapareces en el último punto seguro alcanzado. Caer un solo peldaño (≤ 8 cm) es un paso normal.

| Punto seguro | Dónde | Se guarda al |
|---|---|---|
| PS0 | Rincón de inicio, junto al costurero | Empezar |
| PS1 | Alto de la rampa, en la mesa baja | Pisar la mesa baja |
| PS2 | Junto a la montañita de clavos | Recoger los clavos |
| PS3 | Repisa de la cajonera | Cruzar la regla |
| PS4a–c | Cada cajón de subida | Pisarlo |
| PS5 | Alto de la cajonera | Llegar arriba |
| PS6 | Base de la mesa, delante de la bandejita | Llegar con el robot parado |
| PS7 | Zona segura del tablero, mirando a la máquina | Salir del portal |

| Zona de caída | Reapareces en |
|---|---|
| Suelo alrededor de la mesa baja y bajo la regla | El último punto entre PS1 y PS3 |
| Suelo junto a la cara de subida de la cajonera | El último cajón alcanzado o PS3 |
| Pasillo, con el robot en marcha | PS5 (igual que si el robot te alcanza) |
| Suelo desde el tablero de la mesa de trabajo | PS7 |

---

## 5. Lo que debe salir de aquí para el mapa

- [ ] Plano de planta con medidas, respetando las reglas de conexión del apartado 3.
- [ ] Corte de alturas con las cotas del apartado 2.
- [ ] Posición de los 8 puntos seguros y los colisionadores de caída.
- [ ] Líneas de visión hacia la máquina desde Z0, Z2 y Z5.
- [ ] Lista de modelos 3D a partir de la [guía corregida](06_guia_objetos_corregida.md).
