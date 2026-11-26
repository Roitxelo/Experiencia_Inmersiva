# Reto 5 · Investigación guiada (apartado 4)

> **Estado:** borrador para revisar por Roi.
> **Fecha de consulta de todas las fuentes:** 26/11/2026.
> El enunciado pide responder "con tus palabras": este texto es una propuesta para que Roi la revise, la ajuste y la haga suya.

---

## 1. ¿Qué es WebXR?

WebXR es una tecnología de la web (una API del navegador) que permite que una página web se conecte a unas gafas de realidad virtual (VR) o de realidad aumentada (AR). Gracias a ella, una web normal puede "entrar" en las gafas: sabe dónde está la cabeza del usuario, dónde están sus mandos y muestra una imagen para cada ojo.

La gran ventaja es que **no hace falta instalar ninguna app**: basta con abrir una dirección web en el navegador de las gafas (en Meta Quest 3, el navegador *Meta Quest Browser*).

Importante: WebXR **no dibuja el 3D por sí mismo**. Solo hace de puente con las gafas. Para crear los objetos 3D se usa otra librería, por ejemplo **Three.js**, A-Frame o el Immersive Web SDK de Meta.

**Fuentes:**
- MDN Web Docs, *Fundamentals of WebXR*: https://developer.mozilla.org/en-US/docs/Web/API/WebXR_Device_API/Fundamentals (consulta: 26/11/2026)
- Meta, *WebXR overview*: https://developers.meta.com/vr/documentation/web/webxr-overview/ (consulta: 26/11/2026)

---

## 2. ¿Qué diferencia hay entre una página 3D y una experiencia inmersiva?

- **Página 3D:** ves el contenido 3D *dentro de un rectángulo* (la pantalla del ordenador o del móvil). Lo mueves con el ratón o el dedo, pero sigues "fuera", mirando una ventana. En WebXR a esto se le llama modo `inline`.
- **Experiencia inmersiva:** el contenido 3D *sustituye todo lo que ves*. Llevas las gafas puestas, cada ojo recibe su imagen, la escena se mueve cuando giras la cabeza o caminas, y usas los mandos (o las manos) para interactuar. Tienes la sensación de *estar dentro*.

Ejemplo sencillo: una página 3D es como mirar una maqueta de una sala a través de una ventana; la experiencia inmersiva es entrar en la sala.

**Fuente:** MDN Web Docs, *Fundamentals of WebXR* (modos `inline` e `immersive-vr`), enlace arriba (consulta: 26/11/2026).

---

## 3. ¿Qué son una escena, una cámara y un objeto 3D?

Se puede pensar como si rodáramos una película:

- **Escena:** es el "plató". El espacio virtual donde colocamos todo: objetos, luces, suelo, fondo…
- **Cámara:** es el "punto de vista". Decide desde dónde y hacia dónde se mira la escena. En VR, la cámara va pegada a la cabeza del usuario: las gafas la mueven automáticamente cuando giras la cabeza.
- **Objeto 3D:** cada cosa que hay en la escena (un cubo, una esfera, una silla…). Normalmente se compone de:
  - una **geometría** (la forma),
  - un **material** (el color o aspecto de la superficie),
  - y una **posición, rotación y tamaño** dentro de la escena.

Además hay un **renderizador**, que es el que "saca la foto" de la escena desde la cámara y la muestra en pantalla (o en las gafas) muchas veces por segundo.

**Fuente:** Documentación de Three.js (`Scene`, `PerspectiveCamera`, `Mesh`, `WebGLRenderer`): https://threejs.org/docs/ (consulta: 26/11/2026)

---

## 4. ¿Qué función tienen los controles del visor?

Los mandos (controladores) de las Meta Quest 3 son la forma de **interactuar** con el mundo virtual. Tienen dos funciones principales:

1. **Saber dónde están:** las gafas detectan la posición y la orientación de cada mando en el espacio. Así podemos dibujar una mano o un "rayo láser" que sale del mando para apuntar a objetos.
2. **Recibir acciones:** los botones (gatillo, botón de agarre, botones A/B/X/Y, joystick) envían eventos. En WebXR, el más importante es la **selección** (`select`), que normalmente es apretar el gatillo. Con eso podemos, por ejemplo, cambiar el color de un objeto al apuntarlo y pulsar.

También pueden dar **vibración** (respuesta háptica). Las Quest 3 permiten además usar las **manos** sin mandos (hand tracking), aunque para empezar es más sencillo usar los mandos.

**Fuentes:**
- Meta, *WebXR first steps* (capítulo de interacción con controladores): https://developers.meta.com/vr/documentation/web/webxr-first-steps/ (consulta: 26/11/2026)
- MDN Web Docs, *WebXR Device API*: https://developer.mozilla.org/en-US/docs/Web/API/WebXR_Device_API (consulta: 26/11/2026)

---

## 5. ¿Qué es una sesión `immersive-vr`?

Una **sesión** es el "periodo" en el que la página está conectada a las gafas. WebXR tiene varios tipos de sesión:

- `inline`: el 3D se ve dentro de la página, sin gafas.
- `immersive-vr`: **realidad virtual completa**. La escena ocupa toda la vista y el mundo real desaparece.
- `immersive-ar`: realidad aumentada; los objetos virtuales se mezclan con el mundo real (en Quest 3, gracias a sus cámaras a color "passthrough").

Para nuestro proyecto usaremos `immersive-vr`. Funciona así:
1. La página comprueba si las gafas lo admiten (`navigator.xr.isSessionSupported("immersive-vr")`).
2. Muestra un botón tipo **"Entrar en VR"**.
3. Cuando el usuario pulsa el botón, se pide la sesión (`navigator.xr.requestSession("immersive-vr")`). El navegador **obliga** a que sea el usuario quien la inicie con un clic, por seguridad.
4. Al salir (botón de menú de las gafas), la sesión termina y se vuelve a la página normal.

**Fuente:** MDN Web Docs, *Starting up and shutting down a WebXR session*: https://developer.mozilla.org/en-US/docs/Web/API/WebXR_Device_API/Startup_and_shutdown (consulta: 26/11/2026)

---

## 6. ¿Por qué puede ser necesaria una conexión segura HTTPS?

Porque WebXR accede a datos sensibles del usuario: la posición de su cabeza y de sus manos, el espacio de su habitación, etc. Por eso los navegadores **solo activan WebXR en páginas "seguras"**:

- páginas servidas con **HTTPS** (conexión cifrada), o
- páginas abiertas desde el propio ordenador (`http://localhost`).

Si abrimos la página con `http://` normal desde otra dirección (por ejemplo, desde las gafas a la IP del ordenador: `http://192.168.1.20:8081`), **WebXR ni siquiera aparece** (`navigator.xr` no existe) y el botón "Entrar en VR" no funcionará.

En la práctica esto significa que para probar en las Quest 3 necesitaremos una de estas opciones:
- un servidor de desarrollo con HTTPS (aceptando el aviso de certificado en las gafas),
- redirigir el puerto por cable USB con ADB para que las gafas vean la página como `localhost`,
- o publicar la web en un sitio con HTTPS (por ejemplo, GitHub Pages).

**Fuentes:**
- MDN Web Docs, *Starting up and shutting down a WebXR session* ("A WebXR compatible environment starts with a securely-loaded document"), enlace arriba (consulta: 26/11/2026)
- Meta, *WebXR first steps* (acceso desde el visor por IP o por ADB, aviso de certificado), enlace arriba (consulta: 26/11/2026)

---

## 7. ¿Cómo probar parte del desarrollo sin utilizar el visor?

No hace falta ponerse las gafas cada vez. Opciones:

1. **Navegador del ordenador:** la escena 3D (modo normal, sin VR) se puede ver y depurar en Chrome o Edge.
2. **Emulador de WebXR:** Meta ofrece el **Immersive Web Emulator**, una extensión para Chrome/Edge que *simula unas gafas y sus mandos* en el ordenador. Permite mover la "cabeza" y los "mandos" virtuales y pulsar sus botones. También existe **IWER** (Immersive Web Emulation Runtime), un emulador que se integra en el propio proyecto y se activa solo si el navegador no tiene WebXR.
3. **Herramientas de depuración:** las DevTools del navegador (consola, errores) y, en las gafas, la depuración remota desde `chrome://inspect` con el cable USB.
4. **Ver lo que ve el visor:** con *Meta Quest Developer Hub* se puede transmitir la imagen de las gafas al ordenador.

Aun así, la **prueba final siempre debe hacerse en las gafas reales**, porque el rendimiento, la escala y la sensación no son iguales.

**Fuentes:**
- Meta, *WebXR workflow*: https://developers.meta.com/vr/documentation/web/webxr-workflow/ (consulta: 26/11/2026)
- Meta, *WebXR first steps* (IWER y `@iwer/devui`), enlace arriba (consulta: 26/11/2026)
