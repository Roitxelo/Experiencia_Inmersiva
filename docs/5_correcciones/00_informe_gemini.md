# Informe de coherencia y lógica del proyecto «Experiencia Inmersiva»

**Auditoría técnica y de diseño**  
Revisión exhaustiva del apartado de diseño vigente y contraste con la memoria, el enunciado y el histórico de decisiones.

- **Proyecto:** Experiencia inmersiva (WebXR + React · Meta Quest 3)
- **Documentos centrales:** `docs/3_diseno/flujo_definitivo.md` y `docs/3_diseno/guia_objetos.md`
- **Fecha de cierre auditada:** 27/11/2026

---

## 1. Resumen ejecutivo

El proyecto presenta una premisa atractiva y bien acotada en cuatro objetivos principales (montar el arco, obtener clavos, detener el robot aspirador y activar la máquina). Además, la organización documental y el registro de decisiones en `MEMORIA.md` facilitan la trazabilidad del proceso creativo.

Sin embargo, las iteraciones rápidas entre el 26 y el 27 de noviembre de 2026 —en las que se cambiaron varias veces el inicio, la locomoción, el arco y los puzles intermedios— han dejado **errores de lógica espacial, física, de diseño de juego y contradicciones directas entre archivos**. Conviene resolverlos antes de dibujar el mapa con medidas o iniciar la programación.

> **Diagnóstico principal:** El documento `flujo_definitivo.md` figura como cerrado, pero contiene un error topológico grave en las alturas entre las zonas 3, 4 y 5, conflictos de controles en los mandos, casos de fallo sin salida definida (caídas al vacío) y varias contradicciones explícitas frente a `guia_objetos.md` y `MEMORIA.md`.

| Área auditada | Críticos | Moderados | Menores | Impacto principal |
| :--- | :---: | :---: | :---: | :--- |
| Lógica espacial, física y escala | **3** | **2** | 0 | Imposibilidad geométrica y física |
| Diseño de juego, controles y casos límite | **2** | **4** | **1** | Bloqueos, mareo y conflicto de mandos |
| Contradicciones entre documentos vigentes | **1** | **4** | **2** | Reglas ambiguas al implementar |
| Alineación con el enunciado y planificación | **1** | **2** | **2** | Riesgo de incumplir plazo o requisitos |
| **Total de hallazgos detectados** | **7** | **12** | **5** | **24 puntos de revisión** |

---

## 2. Errores de lógica física y coherencia espacial

### 2.1. Contradicción topológica de alturas entre Mesa baja, Cajonera y Suelo (Zonas 3, 4 y 5) — [Crítico]

El flujo definitivo arrastra una inconsistencia de cotas heredada de versiones anteriores:

- En la **Zona 1**, el jugador sube desde el **suelo** hasta la **mesa baja** mediante el cartón-rampa.
- En la **Zona 3**, un hueco separa la **mesa baja** de la **cajonera**. La regla cae en horizontal y deja al jugador en el *zócalo de la cajonera* (por tanto, el zócalo está a la altura de la mesa baja).
- En la **Zona 4**, sube tres cajones desde ese zócalo hasta lo alto de la cajonera.
- En la **Zona 5**, tras detener al robot que patrulla en el suelo, el texto indica: *«Bajas al suelo por los cajones abiertos y recoges la canica 1»*.

**Fallo lógico:** Si el zócalo de la cajonera está a la altura de la mesa baja, bajar por los mismos cajones devuelve al jugador a la altura de la mesa baja, **no al suelo**. A la inversa, si la cajonera reposa en el suelo y su zócalo está a ras de suelo, entonces la regla-puente de la Zona 3 no sería un puente horizontal sobre un hueco, sino una caída pronunciada desde la mesa baja hasta el suelo, haciendo innecesario haber subido a la mesa en la Zona 1.

**Solución recomendada:** Colocar la cajonera apoyada en el suelo pero con la regla-puente llegando a la altura del *primer cajón* o de un estante intermedio, o bien añadir un descenso explícito y seguro desde el lado opuesto de lo alto de la cajonera hacia el suelo del robot (por ejemplo, una pila de libros o una rampa lateral).

### 2.2. Geometría imposible del cartón-rampa al tirar de su base (Zona 1) — [Crítico]

En la Zona 1, un cartón plano está *«casi vertical, apoyado contra el canto de la mesa baja»*. El jugador clava una aguja con hilo en su base y tira hacia sí para inclinarlo como una escalera y formar una rampa transitable.

**Fallo geométrico:** Si el cartón mide lo justo para llegar al canto de la mesa estando casi vertical, al desplazar su base hacia atrás la parte superior resbala por debajo del borde y cae al suelo (por geometría básica, una tabla de longitud igual a la altura de la mesa nunca puede alcanzar el borde estando inclinada). Para formar una rampa caminable (~30°), el cartón tendría que medir casi el **doble** de la altura de la mesa y sobresalir enormemente por encima del tablero al inicio. Además, clavar una aguja en cartón y tirar con fuerza del peso de una plancha gigante a esa escala rasgaría el cartón o desclavaría la aguja.

### 2.3. Física incoherente del arco de clip e interferencia de la canica en la culata (Zonas 0 y 6) — [Crítico]

Existen dos problemas físicos directos ligados a la herramienta central:

- **Ausencia de elasticidad (Zona 0):** El arco se fabrica abriendo manualmente un clip metálico y atándole hilo de un ovillo de costura. Como ya advirtió el propio equipo en `MEMORIA.md` (Entrada 19), un alambre que se dobla plásticamente con las manos **no recupera su forma**, y el hilo de algodón tampoco es elástico. En la práctica, ningún elemento almacena energía para lanzar proyectiles. Si se mantiene el clip por estética o por el buen tutorial a dos manos, conviene usar una **goma elástica** en lugar de hilo de coser como cuerda.
- **Punto de apoyo ocupado en la Zona 6:** Para disparar las canicas, Roi decidió pegar cada canica con chicle *«detrás de un clavo»*. Sin embargo, la parte trasera del clavo (la cabeza) es exactamente el punto donde apoya la cuerda del arco al tensar. Si la canica ocupa la culata, el clavo no puede apoyarse en la cuerda de forma verosímil.

### 2.4. Desajuste matemático de la escala declarada (12 cm / ×15) — [Moderado]

Ambos documentos de diseño fijan la estatura del jugador en **12 cm** (todo se ve **15 veces más grande**). Sin embargo, varias descripciones del escenario contradicen ese factor:

| Objeto | Tamaño real aproximado | Tamaño percibido (×15) | Descripción en diseño (desajuste) |
| :--- | :--- | :--- | :--- |
| Botón de bata | 1,5 – 2 cm | 22 – 30 cm (un plato) | «Botones del tamaño de mesas» (requeriría ×75) |
| Dedal de costura | 2 cm de alto | 30 cm (una papelera) | «Un dedal como un barril» (requeriría ×45) |
| Plomada pequeña | 150 – 500 g | No equivale a 2 kg | Botón exige «2 kg de presión»; ficha compara peso directo |

Este desajuste no rompe la jugabilidad, pero generará confusión inmediata al pasar al mapa con medidas y modelar los objetos en 3D si no se decide si el jugador mide 12 cm (×15) o ~3–4 cm (×45).

### 2.5. Mecanismo físico incompleto del péndulo final (Zona 7) — [Moderado]

En la Zona 7, la plomada cuelga de un hilo sujeta por un pestillo y, al golpear el pestillo con un clavo, empieza a balancearse. Para que un péndulo comience a oscilar al soltar un pestillo debe estar retenido en un **extremo elevado y oblicuo** (no colgando en vertical). Además, la sección 5 describe una única plomada colgada de un flexo, pero la tabla de fallos introduce de repente un *«cajón»* y un *«carrete»* que baja plomadas infinitas, contradiciendo también la petición de Roi en `MEMORIA.md` (Entrada 12) de diseñar el péndulo *«sin que el objeto pueda caer donde no es»*.

---

## 3. Errores de diseño de juego, controles y casos límite

### 3.1. Conflicto directo de controles en Meta Quest 3 y riesgo de mareo — [Crítico]

El documento `flujo_definitivo.md` asigna funciones incompatibles al mismo control y elimina las medidas de confort recomendadas por Meta:

- **Colisión del joystick:** La sección 3.2 indica movimiento continuo y giro por pasos (que en Quest 3 ocupan el joystick izquierdo para caminar y el derecho para girar), mientras que la sección 3.3 establece que *«el joystick cambia de munición»*. No se especifica cómo conviven ambas acciones sin activar giros o desplazamientos accidentales al cambiar entre aguja y clavo.
- **Riesgo alto de mareo (*cybersickness*):** Tras eliminar el teletransporte hasta la Zona 6, el jugador debe subir una rampa inclinada, cruzar una regla estrecha sobre un vacío y realizar tres saltos verticales con botón sobre cajones pequeños. Las propias fuentes de Meta citadas en el proyecto desaconsejan el salto con botón y los desniveles sin teletransporte para usuarios noveles.

### 3.2. Caídas al vacío no contempladas en las zonas elevadas (Zonas 2, 3 y 4) — [Crítico]

Desde la Zona 2 hasta la Zona 5 el jugador se desplaza por superficies elevadas (mesa baja, regla-puente sobre un hueco y tres cajones estrechos). La tabla *«7. Qué pasa si fallas»* de `flujo_definitivo.md` cubre doce situaciones, pero **omite por completo qué ocurre si el jugador se cae**.

Si cae al suelo y debe volver caminando a la Zona 1 para subir de nuevo por la rampa y recorrer todo el taller, el ritmo se rompe y la duración se dispara. Si existen muros invisibles, el salto por los cajones pierde sentido de habilidad. Debe definirse explícitamente un sistema de reaparición rápida al último borde seguro con fundido breve.

### 3.3. Mecánica de un solo uso («aguja con hilo») que rompe los principios del proyecto — [Moderado]

La mecánica de atar el hilo del ovillo a una aguja, clavarla como arpón y tirar físicamente del hilo tenso se usa **exclusivamente en la Zona 1** y jamás vuelve a emplearse. Esto vulnera el principio fijado en `estructura_aprobada.md` (reutilizar cada habilidad aprendida) y añade una complejidad técnica desproporcionada en WebXR (simulación de cuerda tensa, detección de dirección de tirón y arrastre) para apenas 60 segundos de juego.

### 3.4. Huecos lógicos en el encuentro con el robot (Zona 5) — [Moderado]

- **Salto accidental del puzle:** El robot patrulla en línea recta de ida y vuelta. Si no hay una barrera o un pasillo suficientemente estrecho, un jugador puede bajar de la cajonera y cruzar corriendo cuando el robot esté en el extremo opuesto, entrando en la Zona 6 sin haberlo detenido (para luego quedar bloqueado al descubrir que le falta la Canica 1).
- **Inspección en movimiento:** La pista clave (*«¡No usar sobre superficies mojadas!»*) está en una pegatina del robot. Apuntar con precisión a un objeto móvil desde lo alto de una cajonera para pulsar el botón de inspección y leer texto en VR resulta incómodo si no se congela o desacopla la ficha.
- **Falta de señal si la botella se perfora antes:** Aunque se admite perforar la botella antes de pulsar OFF, el diseño definitivo no heredó la recomendación de Codex (`revision_codex_flujo_2026-11-27.md`) de mostrar claramente que el charco queda fuera del recorrido normal del robot para guiar al jugador hacia el botón OFF.

### 3.5. Ambigüedades y casos límite en el sistema de canicas (Zona 6) — [Moderado]

- **«Un solo salto» frente a enlace permanente:** Las secciones 1, 3.1 y 6 insisten en que las canicas permiten *«un solo salto»*, pero la sección 7 afirma que *«después del salto, el enlace se mantiene para poder volver»*. Además, una vez sobre la mesa de la máquina no existe ninguna necesidad de volver abajo, y si el jugador pulsa «Recoger canicas» estando ya arriba, el enlace desaparecería igualmente.
- **Orden de disparo y superficies válidas:** El texto asume que el jugador dispara primero a la madera cercana y después a la diana de corcho, sin aclarar si el orden inverso funciona. Tampoco contempla qué ocurre si el jugador dispara **ambas canicas** al suelo o a patas de madera abajo (crearía un enlace inútil) ni cómo «entra» el jugador en un portal anclado en una superficie plana del suelo frente a una diana vertical.

### 3.6. Indeterminación en la Zona 0: ¿qué ocurre si se intenta usar el ovillo o la aguja antes de montar el arco? — [Moderado]

En la Zona 0, la ficha del ovillo dice desde el primer segundo: *«Átalo al clip para hacer un arco, o a una aguja para tirar de algo»*. Esto adelanta la solución de la Zona 1 antes de ver el cartón y permite que un jugador intente atar el hilo a una aguja antes de haber abierto el clip o montado el arco, un estado no previsto en el flujo.

### 3.7. Terminología inconsistente entre «flecha» y «aguja/clavo» — [Menor]

En las primeras propuestas existía una flecha base con puntas intercambiables. En el diseño definitivo esa flecha desapareció y se disparan agujas y clavos directamente, pero `flujo_definitivo.md` (secciones 3.3 y 7) y `guia_objetos.md` siguen refiriéndose a ellos como *«la flecha»*. Conviene unificar el vocabulario para no inducir a error al modelar o programar.

---

## 4. Contradicciones directas entre documentos vigentes

Al contrastar `flujo_definitivo.md`, `guia_objetos.md`, `README.md` y `MEMORIA.md` aparecen siete discrepancias directas que deben unificarse en una única fuente de verdad:

| Elemento | Qué dice un documento | Qué dice otro documento | Severidad y corrección |
| :--- | :--- | :--- | :--- |
| **Botella de líquido (Zona 5)** | `flujo_definitivo.md` (3.1 y Zona 5): se perfora con **aguja**. | `guia_objetos.md` (Botella): se perfora con **aguja (o clavo)**. | **Crítico.** Limitar a aguja para no anular el cambio de munición en Zona 5. |
| **Desbloqueo de agujas** | `flujo_definitivo.md` (6): se desbloquean al abrir el clip y atar el hilo. | `guia_objetos.md` (1 y 2): se desbloquean «al empezar» al agarrar el acerico. | **Moderado.** Definir si las agujas entran al carcaj al tocar el acerico y aclarar que requieren arco. |
| **Desbloqueo del chicle** | `flujo_definitivo.md` (6): se desbloquea al cortar la bandejita de la Canica 2. | `guia_objetos.md` (1 y 2): material fijo sin desbloqueo, ya abierto junto a la bandejita. | **Moderado.** Quitar el chicle del evento de corte; está disponible al llegar a Zona 6. |
| **Clasificación en guía de objetos** | `guia_objetos.md` (1): Ovillo, Chicle y Diana figuran como «No se llevan» o «Escenario». | `guia_objetos.md` (2): los tres están redactados dentro de la sección *«2. Objetos que llevas»*. | **Moderado.** Mover Ovillo, Chicle y Diana de corcho a la sección 3 (Objetos del escenario). |
| **Duración del juego** | `README.md` y `flujo_definitivo.md` (1): duración objetivo de **10–12 min**. | `flujo_definitivo.md` (8): estimación oficial ya es de **10–14 min** sin probar en VR. | **Moderado.** Aplicar recortes o asumir que el alcance actual superará los 12 minutos. |
| **Estado del clip-arco** | `MEMORIA.md` (Entrada 20): Roi elige el clip como arco **provisional**. | `flujo_definitivo.md`: lo presenta como cerrado y **definitivo** sin advertencia. | **Menor.** Marcar si sigue pendiente de prueba en Quest 3 o si ya es definitivo. |
| **Objetivo 2 (alcance)** | `flujo_definitivo.md` (2): agrupa Zonas 2–4 bajo «Conseguir segunda munición». | `flujo_definitivo.md` (5): los clavos se consiguen en Zona 2; Zonas 3 y 4 son tránsito. | **Menor.** Renombrar el objetivo o indicar «Conseguir y dominar la segunda munición». |

---

## 5. Coherencia con el enunciado del reto y riesgos de viabilidad

### 5.1. Desproporción de alcance y falta de comprobación técnica previa — [Crítico]

El enunciado (`docs/1_enunciado/Reto - Experiencia inmersiva.docx`) plantea un proyecto de **8 semanas** cuyo mínimo funcional es una escena 3D con al menos 3 objetos seleccionables y respuesta visual. Además, incluye una advertencia destacada en el apartado 6: *«O modelo exacto dos visores está pendente. Antes de comprometer o desenvolvemento, comproba que o navegador e o dispositivo admiten a sesión WebXR prevista.»*

A pesar de ello, toda la documentación da por confirmadas unas **Meta Quest 3** y cierra un diseño de **8 zonas, 18 objetos interactivos y 4 sistemas mecánicos complejos** sin haber realizado todavía la prueba técnica mínima (Semana 2 del registro de avance). Comprometer un diseño tan extenso antes de validar arco a dos manos, locomoción sin mareo y rendimiento en el visor real supone el mayor riesgo del proyecto.

### 5.2. Ausencia de la interfaz React en el diseño — [Moderado]

El apartado 7 del enunciado (*Probas*) exige comprobar específicamente la **«Resposta da interface React»** (Prueba 3), y la Semana 3 del calendario se dedica a dicha interfaz. Aunque el proyecto usa React Three Fiber, ni `flujo_definitivo.md` ni `guia_objetos.md` definen qué elementos componen la interfaz React fuera o dentro de VR (pantalla de inicio, selector de opciones de comodidad, menú de reinicio o depuración).

### 5.3. Pendientes de la investigación guiada y detalles documentales — [Moderado / Menor]

- **Investigación guiada sin personalizar [Moderado]:** El archivo `docs/2_investigacion/reto5_investigacion_guiada.md` sigue en estado de *«borrador para revisar por Roi»* redactado por Claude, cuando el enunciado exige responder *«coas túas palabras»*.
- **Idioma del entregable [Menor]:** El enunciado está redactado en **gallego** y toda la documentación del repositorio en **castellano**. Conviene confirmar si el centro exige entregar la memoria e investigación en gallego.
- **Texto de enlace desactualizado [Menor]:** En la cabecera de `MEMORIA.md`, el texto visible del enlace al enunciado todavía muestra la ruta antigua `docs/Reto - Experiencia inmersiva.docx` (aunque el destino del enlace sí apunta correctamente a `docs/1_enunciado/`).

---

## 6. Plan de corrección priorizado antes de la siguiente fase

Antes de pasar al mapa con medidas, la lista de modelos 3D o la programación, se recomienda cerrar estas siete decisiones y actualizar `docs/3_diseno/`:

1. **Resolver la topología de las Zonas 3–5:** Fijar en un croquis de cotas la altura exacta del suelo, la mesa baja, la cajonera y la mesa de trabajo, eliminando la contradicción entre el zócalo de la cajonera y la bajada al suelo del robot.
2. **Rediseñar el cartón-rampa (Zona 1) o eliminar la mecánica de un solo uso:** Si se mantiene el cartón, especificar que sobresale de la mesa o sustituir el gesto de «tirar» por una solución que reutilice la aguja (cortar) o que la mecánica de tirar se vuelva a usar al menos una vez más (por ejemplo, en la Zona 6).
3. **Corregir la física del arco y la canica:** Sustituir el hilo de costura por una **goma elástica** para dar credibilidad al arco de clip, y recolocar la canica con chicle en el lateral o la punta del clavo para dejar libre la culata donde apoya la cuerda.
4. **Definir el mapeo completo de mandos y la política de caídas:** Resolver la colisión entre locomoción y cambio de munición en el joystick, añadir una opción de confort (teletransporte accesible o ayuda en saltos) y documentar la recuperación automática ante caídas desde la mesa baja, la regla y los cajones.
5. **Unificar las reglas entre `flujo_definitivo.md` y `guia_objetos.md`:** Restringir la botella de la Zona 5 solo a la aguja, aclarar el desbloqueo de agujas y chicle, corregir las secciones de `guia_objetos.md` y unificar el uso de «proyectil» frente a «flecha».
6. **Ajustar las referencias de escala:** Comprobar si la escala real elegida es 12 cm (×15) y adaptar las descripciones de botones, dedal y peso del botón final (2 kg) para que los modelos 3D sean coherentes.
7. **Ejecutar ya la prueba técnica mínima en el visor real:** Verificar el modelo exacto de gafas disponible, validar la entrada en `immersive-vr` y probar un prototipo mínimo de arco a dos manos y movimiento antes de construir las 8 zonas completas.