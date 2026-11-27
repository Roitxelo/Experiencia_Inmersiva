# Controles, confort, caídas e interfaz React

Resuelve E07, E08, E09 (regla general), E12 y E24. **Es una propuesta para validar en la fase 0** en el visor real.

---

## 1. Mapa de mandos (propuesta para validar)

Para jugadores diestros. En las opciones hay un modo para zurdos que intercambia las manos.

| Control | Acción |
|---|---|
| Joystick izquierdo | Caminar (continuo, velocidad moderada) |
| Joystick derecho ← → | Giro por pasos de 30° (en las opciones, giro suave) |
| Joystick derecho ↑ ↓ | Nada, para evitar acciones por accidente |
| A | Saltar |
| B | Inspeccionar lo que se apunta y cerrar la ficha |
| X | Cambiar de munición: aguja ↔ clavo |
| Y | Abrir o cerrar el menú de muñeca (también se abre al mirar la muñeca) |
| Agarre (grip) | Agarrar: el arco del cinto, un proyectil del carcaj, el clip, la goma, el hilo o una canica |
| Gatillo | Señalar con el rayo (resalte e interfaz) |

**Disparar:** la mano izquierda agarra el arco. La derecha va al hombro y agarra un proyectil, lo lleva a la goma, tensa y **suelta el agarre** para disparar. La vibración aumenta con la tensión.

**Canica:** con un clavo en la mano, se toca el paquete de chicles y después la canica del cinto. La canica queda pegada en la cabeza del clavo y se dispara igual.

---

## 2. Confort

| Medida | Por defecto | Opción |
|---|---|---|
| Viñeta (túnel) al moverse y al saltar | Activada | Intensidad o desactivar |
| Giro | Por pasos de 30° | Suave |
| Velocidad al caminar | Moderada | Lenta / normal |
| Saltos asistidos | Desactivados | Al apuntar a un borde y pulsar A, el salto sigue una parábola fija hasta él |
| Postura | De pie | Sentado (sube la cámara) |

**Pregunta abierta para después de la fase 0:** si los saltos siguen mareando con la viñeta y la ayuda, ¿se ofrece un modo de confort que convierta los saltos entre cajones en un desplazamiento corto con fundido? No contradice la decisión de Roi, porque no es el teletransporte de las canicas, pero Roi tendrá que aprobarlo.

---

## 3. Caídas y reaparición

- Si caes a una zona de caída, hay un fundido a negro de 0,5 s y reapareces en el último punto seguro. Todo lo resuelto se queda.
- Lista de puntos seguros y zonas de caída en [03](03_cotas_y_mapa.md#4-puntos-seguros-y-zonas-de-caída).
- Los bordes llevan un reborde visible. No hay muros invisibles en los saltos.

## 3.1 Fichas de inspección
- Al pulsar B, la ficha aparece **fija en el espacio**, a 1 m de la vista. No sigue al objeto aunque se mueva.
- Los objetos en movimiento (el robot, la plomada) tienen un área de selección más grande.

---

## 4. Interfaz React

Lo que exige la prueba 3 del enunciado ("Resposta da interface React"):

| Pantalla | Dónde | Contenido |
|---|---|---|
| **Inicio** | Navegador, en 2D | Título, comprobación de compatibilidad (`navigator.xr.isSessionSupported('immersive-vr')`) con un mensaje claro si falla, botón **Entrar en VR** y opciones de confort |
| **Opciones** | Inicio y menú de muñeca | Las medidas del apartado 2, modo zurdo y volumen |
| **Menú de muñeca** | En VR | Libreta de objetos descubiertos (con sus fichas), "Recoger canicas" (solo antes del salto), "Volver al último punto seguro", opciones y salir |
| **Final** | En VR y en 2D al salir | Tiempo total, botón "Jugar otra vez" |
| **Depuración** | Solo en desarrollo | FPS, ir a una zona, mostrar colisionadores y puntos seguros |

El estado del juego (zona, desbloqueos, punto seguro, opciones) vive en un único almacén de React, como `zustand`. Lo leen tanto la interfaz 2D como la escena 3D.
