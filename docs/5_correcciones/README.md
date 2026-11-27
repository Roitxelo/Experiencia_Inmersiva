# 5 · Correcciones del informe de Gemini

Carpeta de trabajo para corregir los errores del [informe de coherencia de Gemini](00_informe_gemini.md) y llegar a una versión final del flujo **antes de dibujar el mapa**.

**No sustituye todavía a `docs/3_diseno/`.** Cuando Roi cierre la versión 2, el flujo y la guía corregidos pasarán a `docs/3_diseno/`, y los anteriores a `docs/4_historico/`.

## Estado

| Fecha | Quién | Qué |
|---|---|---|
| 27/11/2026 | Gemini | Informe con 24 hallazgos |
| 27/11/2026 | Claude | Valoración (real, parcial o malentendido), soluciones y versión 2 |
| 27/11/2026 | Roi | Decide la cuerda de goma elástica (E03) |
| — | Codex | Revisión de la versión 2 ([encargo](07_prompt_para_codex.md)) |
| — | Roi | Cierre de la versión 2 |

**Resumen:** 31 puntos (29 de Gemini, separados, y 2 nuevos). 26 resueltos en la v2 y 5 pendientes de Roi o de la prueba en el visor (E07 y E08 se validan en la fase 0; E23, E25 y E28 son tareas de Roi).

## Archivos (por orden de lectura)

| # | Archivo | Para qué |
|---|---|---|
| 00 | [informe_gemini.md](00_informe_gemini.md) | Informe original de Gemini (sin cambios) |
| 01 | [lista_errores.md](01_lista_errores.md) | **Lista maestra:** cada error con valoración, gravedad, estado y solución en una línea |
| 02 | [soluciones_por_pasos.md](02_soluciones_por_pasos.md) | Solución detallada de cada error |
| 03 | [cotas_y_mapa.md](03_cotas_y_mapa.md) | Escala, alturas, planta, reglas de conexión y puntos seguros: la base del mapa |
| 04 | [controles_confort_interfaz.md](04_controles_confort_interfaz.md) | Mandos de Quest 3, confort, caídas e interfaz React |
| 05 | [flujo_corregido.md](05_flujo_corregido.md) | **Flujo v2** sin los errores |
| 06 | [guia_objetos_corregida.md](06_guia_objetos_corregida.md) | **Guía de objetos v2** |
| 07 | [prompt_para_codex.md](07_prompt_para_codex.md) | Encargo para que Codex revise y lleve la v2 a la versión final |

## Cómo se trabaja aquí

1. Cada cambio se apunta en [01_lista_errores.md](01_lista_errores.md): se cambia el estado y se añade una nota.
2. Si un cambio toca una decisión de Roi, se le pregunta antes.
3. El flujo (05) y la guía (06) se mantienen coherentes entre sí y con las cotas (03).
4. Cada paso se registra en `MEMORIA.md`.
