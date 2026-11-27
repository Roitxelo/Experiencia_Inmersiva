# Encargo para Codex · revisión de la versión 2 del flujo

Copia este texto en Codex desde la raíz del repositorio.

---

Hola, Codex. Trabajamos en `docs/5_correcciones/`. Gemini auditó el flujo definitivo y Claude ha valorado cada hallazgo y redactado una versión 2. Tu tarea es revisarla y dejarla lista para que Roi la cierre. Escribe todo en castellano.

**Lee, en este orden:**
1. `docs/5_correcciones/README.md`
2. `docs/5_correcciones/00_informe_gemini.md`
3. `docs/5_correcciones/01_lista_errores.md`
4. `docs/5_correcciones/02_soluciones_por_pasos.md`
5. `docs/5_correcciones/03_cotas_y_mapa.md` y `04_controles_confort_interfaz.md`
6. `docs/5_correcciones/05_flujo_corregido.md` y `06_guia_objetos_corregida.md`
7. `MEMORIA.md`, entradas 12–22 (decisiones de Roi)

**Decisiones de Roi que no puedes cambiar sin preguntarle:** clip como arco que se abre tirando de las puntas; cuerda de goma elástica (entrada 22); aguja con hilo solo en la zona 1; canica 2 bajada cortando su hilo; regla-puente con calzo de goma de borrar; tres cajones de subida; robot de dos modos con botella y charco; canica con chicle en la cabeza del clavo; teletransporte solo al final y un único salto; final con plomada y bandeja embudo; munición ilimitada; 3 hilos en la bolsa; orden de recortes. Recuerda la entrada 16: no añadas teletransporte temprano ni cambies elementos sin aprobación.

**Qué revisar:**
1. **Coherencia física y espacial:** comprueba las cotas del documento 03 (alturas, cartón de 50 cm a unos 35°, cajones de 8 cm, hueco de la regla y pasillo del robot). Confirma que las reglas de conexión impiden atajos y que ninguna caída deja al jugador atrapado.
2. **Coherencia entre 05 y 06:** misma munición, mismos desbloqueos, mismas fichas y mismos fallos.
3. **Viabilidad en React Three Fiber + `@react-three/xr` en Quest 3:** mapa de mandos, saltos con viñeta, portal, péndulo y aguja con hilo sin física de cuerda. Señala lo que sea caro de programar y propón cómo abaratarlo.
4. **Valoraciones de la lista 01:** si crees que algún punto marcado como *Malentendido* o *Parcial* es en realidad un error real (o al revés), dilo y justifícalo.
5. Busca errores nuevos que no vieran ni Gemini ni Claude.

**Cómo entregar:**
- No toques `docs/3_diseno/`.
- Añade tus comentarios en `docs/5_correcciones/08_revision_codex.md`, con una tabla: ID (E01… o N01… para los nuevos), qué ves, propuesta y si necesita decisión de Roi.
- Si una corrección es evidente y no toca decisiones de Roi, aplícala directamente en 03–06 y márcalo en la columna "Estado" de `01_lista_errores.md`.
- Añade una entrada nueva en `MEMORIA.md` siguiendo el formato de las anteriores.
- Commits pequeños, en castellano y a nombre de Roi (`Roitxelo`). No hagas push sin que Roi lo pida.

Termina con una lista breve de las preguntas que Roi tiene que responder para cerrar la versión 2.
