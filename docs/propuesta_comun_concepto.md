# Propuesta común del concepto (Roi + Claude) · para contrastar con Codex

**Fecha:** 26/11/2026
**Parte de:** las decisiones de Roi sobre [`debate_concepto_opinion_claude.md`](debate_concepto_opinion_claude.md) y el análisis de Codex en [`analisis_concepto_y_viabilidad.md`](analisis_concepto_y_viabilidad.md).
**Estado:** propuesta. Las marcas **[Decidido]** son decisiones de Roi; **[Propuesta]** son ideas de Claude pendientes de validar con Roi y Codex.

---

## 1. Resumen en una frase

Eres diminuto en un **taller de inventor / aula de tecnología**. Con **una única herramienta lanzadora** y **municiones distintas** que encuentras y combinas, resuelves una **cadena de puzles** usando objetos de la sala a tu favor, hasta llegar a la **máquina que te devuelve tu tamaño**. Duración orientativa: **10–12 minutos**.

---

## 2. Decisiones de Roi y cómo las concreto

### 2.1 Espacio · [Decidido] taller de inventor
- La decoración es secundaria. **Lo importante son las zonas interactuables** y cómo se encadenan.
- [Propuesta] Diseñar **primero el puzle y después el decorado**: cada zona nace de "qué problema hay" y "qué objeto de la sala lo resuelve". Los muebles sin función son solo fondo (geometría simple, poco detalle).

### 2.2 Objetivo · [Decidido] volver a la máquina que revierte el tamaño
- La historia de fondo no es prioritaria. El objetivo debe tener sentido por sí solo: *eres pequeño → la máquina te devuelve tu tamaño*.
- [Propuesta] La máquina se ve **desde el primer segundo**, en lo alto de la mesa, con una luz parpadeante. Así el jugador siempre sabe hacia dónde va. Para activarla hacen falta 2 cosas que se consiguen por el camino (ver recorrido), lo que da sentido a la cadena de puzles.

### 2.3 Obstáculos · [Decidido] algo que mantenga alerta, que se pueda apagar (no derrotar)

**Viabilidad de un "enemigo" móvil:**

| Obstáculo | Cómo se haría | Dificultad | Valor |
|---|---|---|---|
| **Robot aspirador** | Sigue una ruta fija de puntos (sin inteligencia artificial). Si te toca, te "aspira" y vuelves al último punto de control. Tiene un botón de apagado arriba: se apaga acertándole con munición pesada. | **Media-baja.** Es un disco que se mueve y gira; modelo sencillo. Detección por distancia. | Alto: tensión real, se mueve, y apagarlo es satisfactorio. |
| **Rayos láser / sensores** del sistema de seguridad del inventor | Haces de luz fijos o que se encienden y apagan con un ritmo. Si los cruzas, suena la alarma y vuelves al punto de control. Se apagan cortando su alimentación (un cable o interruptor al que disparar) o **bloqueando/desviando** el rayo con un objeto (p. ej. una arandela brillante como espejo). | **Baja.** Son líneas de luz y una comprobación de cruce. | Alto: muy "de inventor", da puzles de ingenio. |
| Gato | Animación de animal creíble, comportamiento impredecible. | **Alta.** | Alto, pero poco integrable (de acuerdo con Roi). Descartado. |

**[Propuesta]** usar **los dos**, en zonas distintas: **láseres** como puzle de ingenio (zona intermedia) y **robot aspirador** como amenaza móvil (zona de suelo amplia). Ambos son viables en el plazo.

### 2.4 Herramienta · [Decidido] una única herramienta lanzadora; la munición da el juego

Me parece la mejor idea del proyecto: **una sola mecánica que se domina, y cada munición nueva cambia lo que puedes hacer**. Es fácil de enseñar, escala bien y da sensación de descubrimiento.

**Debate arco vs. tirachinas:**

| | **Arco** | **Tirachinas** |
|---|---|---|
| Épica | ⬆ Más espectacular e icónico. | Menos épico, más "ingenioso". |
| Fabricación con objetos del taller | Regla de plástico flexible o varilla + hilo / goma. | Horquilla (pinza, lápiz partido) + goma elástica. |
| Cómo se usa en VR | Una mano sujeta el arco; la otra agarra la cuerda, tira hacia atrás y suelta. Es un gesto muy conocido en VR y muy satisfactorio. | Igual, pero la goma tira desde un único punto. |
| Dificultad técnica | Media. **El truco:** la cuerda no se simula, se dibuja como dos líneas rectas que van a la mano. Eso basta para que sea creíble. Apuntar requiere coordinar dos manos. | Baja-media. |
| **Encaje con "la munición da el juego"** | Dispara **flechas**: encaja con clavos y agujas. Para tuercas, botones o canicas, hay que **montarlos en la punta de la flecha** → nace una mecánica de **combinar** (flecha + punta). | Dispara **cualquier objeto** directamente: tuercas, botones, canicas… Más flexible, menos combinación. |

**Mi opinión (cambio respecto a la propuesta anterior):** el arco es **viable** si la cuerda se simplifica como describo. Y encaja muy bien con tu idea de combinar: **la flecha es la base y lo que cambia es la punta**. Recomiendo **arco con flechas modulares**.

**Plan de seguridad:** en la prueba de viabilidad probar primero el arco. Si apuntar con dos manos resulta incómodo en las Quest 3, el tirachinas usa casi el mismo código, así que el cambio sería barato.

**Otras herramientas (espada, etc.):** de acuerdo con Roi, solo si un puzle concreto las justifica. Por ahora, ninguna.

### 2.5 Municiones · [Propuesta] catálogo inicial

Base: **flecha** (palillo, aguja de tejer pequeña o cerilla). Cada punta se consigue en una zona y desbloquea nuevas soluciones.

| Munición (punta) | Dónde se consigue | Qué hace | Ejemplo de uso |
|---|---|---|---|
| **Aguja / alfiler** | Acerico del taller (inicio) | Perfora y revienta | Pinchar una bolsa, un globo, cortar un hilo tenso. |
| **Clavo** | Bolsa de clavos rota (ver recorrido) | Se queda clavado en madera o cartón | Crear asideros o puntos de anclaje. |
| **Tuerca / botón** | Caja de tornillería, costurero | Golpe con peso, no se clava | Pulsar botones e interruptores a distancia; apagar el robot. |
| **Clavo + hilo** (combinación) | Clavo + carrete de hilo | Deja un hilo tensado entre tú y el impacto | **Puente o tirolina** para cruzar un hueco. |
| **Canica portal** (invento) | Frasco del inventor | Dos canicas = dos portales | Lanzar una a un sitio inaccesible y teletransportarte a ella. |

### 2.6 Inventos científicos · [Propuesta] canicas portal

- **Versión viable:** en vez de "ver a través" del portal (caro de dibujar), el portal es un **anillo brillante**: entras y apareces en la otra canica, con un fundido rápido. Así se usa el teletransporte (que además evita mareos).
- Otros inventos posibles si sobra tiempo: **imán** (atrae objetos metálicos lejanos), **ventilador** (empuja objetos ligeros).

### 2.7 Textos de ayuda · [Decidido] cuadro de texto con los objetos interactuables
[Propuesta] de funcionamiento:
- Al **apuntar** a un objeto interactuable: se ilumina y aparece una etiqueta corta con su nombre.
- Al **cogerlo**: se abre una ficha pequeña junto a la mano con **qué hace**, **cómo se usa** y **con qué se combina** (p. ej. "Clavo — se clava en madera. Combínalo con hilo para hacer una cuerda").
- Una **libreta del inventor** en la muñeca recoge lo descubierto, por si el jugador olvida algo.

### 2.8 Duración · [Decidido] 10–12 minutos orientativos
[Propuesta] reparto: **5 zonas de ~2 minutos** cada una, 1–2 puzles por zona. Se ajustará al probar con personas.

---

## 3. Borrador de recorrido tipo puzle (para discutir)

La idea es que cada zona dé **una munición o una pieza nueva** que se necesita en la siguiente.

| # | Zona | Problema | Solución (objetos de la sala a tu favor) | Obtienes |
|---|---|---|---|---|
| 0 | **Despertar bajo el banco de trabajo** | Eres diminuto; todo es enorme. La máquina parpadea arriba. | Tutorial: mirar, apuntar y coger 3 objetos con sus fichas de ayuda (cumple el mínimo del enunciado). | Regla flexible, hilo, agujas del acerico. |
| 1 | **Construir el arco** | Necesitas alcanzar cosas lejanas. | Combinar regla + hilo → **arco**. Practicar con agujas contra una diana improvisada. | **Arco** + agujas. |
| 2 | **La bolsa de clavos** | Una bolsa de clavos cuelga de un gancho. | Disparar una aguja → la bolsa se rompe y los clavos caen al suelo. | **Clavos**. Con el carrete cercano: **clavo + hilo**. |
| 3 | **El pasillo de láseres** | El paso hacia la estantería está bloqueado por sensores. | Disparar una tuerca al interruptor de la regleta, o colocar una arandela-espejo que desvía un rayo. | Paso libre + **tuercas**. |
| 4 | **El territorio del robot aspirador** | Para cruzar el suelo amplio, el robot patrulla. | Esquivarlo siguiendo su ruta o **apagarlo** acertando una tuerca en su botón. Disparar a la **lámpara**: cae y hace de **rampa** hacia la mesa. | Acceso a la mesa. |
| 5 | **La mesa del inventor y la máquina** | La máquina está en lo alto de una pila de libros, al otro lado de un hueco. | **Clavo + hilo** para tender un puente, o **canicas portal** (encontradas en la mesa) para llegar arriba. Activar la máquina con un último disparo a su botón. | **Final**: fundido y vuelves a tu tamaño. |

---

## 4. Puntos a verificar con Codex (técnicos)

1. **Arco con dos manos** en `@react-three/xr`: agarrar la cuerda, tensión según distancia, soltar con el gatillo. ¿Es cómodo en Quest 3?
2. **Física** con `@react-three/rapier`: caída de la lámpara, bolsa que se rompe, flechas que se clavan. ¿Rendimiento aceptable?
3. **Robot aspirador** con ruta de puntos y detección por distancia.
4. **Láseres** con comprobación de cruce y desvío con un espejo (raycast).
5. **Canicas portal** como teletransporte con fundido.
6. **Fichas de ayuda** en 3D legibles en las gafas (tamaño y distancia del texto).

## 5. Preguntas abiertas para Roi

- ¿Te encaja la cadena de 6 zonas o quieres cambiar/añadir puzles?
- ¿Arco con puntas intercambiables, o prefieres que cada munición sea un objeto completo distinto?
- ¿Canicas portal como solución alternativa en la zona 5 o como mecánica que aparezca antes?
- Si el robot te toca: ¿vuelves al punto de control o solo te empuja?
