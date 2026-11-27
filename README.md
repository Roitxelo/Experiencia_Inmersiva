# Experiencia inmersiva

Proyecto de clase para crear una pequeña experiencia de realidad virtual accesible desde el navegador de unas **Meta Quest 3**, con **WebXR + React** (React Three Fiber y `@react-three/xr`).

El objetivo mínimo del reto es mostrar una escena 3D con al menos tres objetos, entrar en modo inmersivo, seleccionar o activar un objeto y mostrar una respuesta visual.

## La experiencia

Despiertas diminuto en el taller de un inventor. Con un arco hecho de un clip y una goma elástica, y una munición que va cambiando (agujas y clavos), usas los objetos del taller a tu favor para detener a un robot aspirador, enlazar dos canicas que te teletransportan y activar la máquina que te devuelve tu tamaño. Duración objetivo: 10–12 minutos.

## Estado

- **Diseño del flujo: cerrado** (27/11/2026) y **en corrección**: versión 2 tras el informe de Gemini en [`docs/5_correcciones/`](docs/5_correcciones/README.md), pendiente de revisión de Codex y cierre de Roi.
- Siguiente fase: prueba técnica en el visor (fase 0), mapa con medidas, lista de modelos 3D y guion técnico.

## Índice

| Qué | Dónde |
|---|---|
| Enunciado del reto | [`docs/1_enunciado/`](docs/1_enunciado/) |
| Investigación guiada (Reto 5) | [`docs/2_investigacion/reto5_investigacion_guiada.md`](docs/2_investigacion/reto5_investigacion_guiada.md) |
| **Flujo definitivo del juego** | [`docs/3_diseno/flujo_definitivo.md`](docs/3_diseno/flujo_definitivo.md) |
| **Guía de objetos** | [`docs/3_diseno/guia_objetos.md`](docs/3_diseno/guia_objetos.md) |
| **Correcciones del informe de Gemini (flujo v2)** | [`docs/5_correcciones/`](docs/5_correcciones/README.md) |
| Histórico de borradores y propuestas | [`docs/4_historico/`](docs/4_historico/README.md) |
| Registro paso a paso | [`MEMORIA.md`](MEMORIA.md) |

Código y recursos: se incorporarán en la fase de desarrollo.

## Forma de trabajo

Roi dirige y decide; Claude y Codex proponen y desarrollan. Cada hito tendrá una propuesta comprensible, una decisión compartida, una implementación pequeña y una comprobación. El resultado se registra en `MEMORIA.md` y se guarda en Git. Las funciones de realidad virtual se validarán en las Meta Quest 3.
