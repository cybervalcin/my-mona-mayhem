<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematización centrada en el diseño

---

En esta parte, usarás los ciclos de planificación e implementación de Copilot para diseñar una transformación completa del tema. Este es un proceso de desarrollo centrado en el diseño: empieza con una visión, perfecciona los elementos visuales y deja que Copilot se encargue del trabajo pesado de CSS.

## Tarea 1: Planifica el tema retro

<!-- track:vscode:start -->
Cambia a **Plan** en GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Usa `/plan` en GitHub Copilot CLI o pulsa **Shift+Tab** hasta activar el modo plan.
<!-- track:cli:end -->

Introduce este prompt:

> Quiero convertir esta página en una experiencia completa de arcade retro. Planifica una renovación visual integral que incluya: efectos de líneas de barrido CRT en el fondo, un brillo de neón en el título que pulse como un letrero, una insignia VS animada con cambios de color en el degradado, una capa de brillo y destellos en las tarjetas de resultados de usuarios, animaciones de entrada flotante para los campos, texto de carga que cambie entre verde y morado, y efectos de resplandor al pasar el cursor sobre los cuadrados de contribuciones. Mantén el fondo oscuro (`#0a0a1a`) con acentos verdes (`#5fed83`) y morados (`#8a2be2`). Usa un tema oscuro con la tipografía retro Press Start 2P de Google Fonts.

Copilot generará un plan detallado de implementación que abarque todos los efectos visuales. **No lo aceptes de inmediato**: revísalo e itera:

- Sugiere ajustes en la duración de las animaciones (por ejemplo, *"Haz que el pulso de neón sea más lento, de unos 3 segundos"*).
- Pregunta por efectos concretos (por ejemplo, *"¿Cómo funcionará la capa de destellos en las tarjetas?"*).
- Pide cambios en el enfoque si algo no te convence.

## Tarea 2: Implementa el tema

Cuando estés satisfecho con el plan, pide a Copilot que lo implemente.

> Implementa el plan del tema de arcade retro que acabamos de diseñar.

Copilot añadirá varias animaciones CSS, pseudoelementos y transiciones a la hoja de estilos. Entre otras cosas, podría añadir:

- `@keyframes` para el efecto de líneas de barrido, el pulso de neón, el brillo y las animaciones de entrada flotante.
- Pseudoelementos (`::before`, `::after`) para efectos de superposición.
- Propiedades personalizadas de CSS para los colores del tema.
- Transiciones y estados `hover` para los elementos interactivos.

<!-- track:cli:start -->
Cuando terminen los cambios, usa `/diff` para revisar los estilos antes de aprobarlos.
<!-- track:cli:end -->

## Tarea 3: Perfecciona el estilo

> **⚠️ ¿No ves los cambios?** Si el tema o las animaciones nuevas no aparecen, detén el servidor de desarrollo (`Ctrl+C`), reinícialo con `npm run dev` y fuerza la recarga del navegador (`Ctrl+Shift+R`).

Mantén abierta la vista previa del navegador e itera sobre el diseño. Prueba prompts como:

> El efecto de líneas de barrido es demasiado intenso; reduce la opacidad a 0.03.

> Añade un parpadeo eléctrico sutil al texto del título.

> La insignia VS debería pulsar con más intensidad.

Este es un proceso de **desarrollo centrado en el diseño**: estás perfeccionando el resultado visual en tiempo real. Cada prompt mejora la experiencia hasta que te convenza. No te conformes con algo «suficientemente bueno»: sigue puliéndolo hasta que la página parezca sacada de una máquina recreativa.

## Tarea 4: Actualiza las instrucciones

Tus instrucciones deben reflejar las decisiones de diseño importantes para que los prompts posteriores mantengan la coherencia.

<!-- track:vscode:start -->
Pide a Copilot Chat:

> Añade una sección de guía de diseño a copilot-instructions.md que describa el tema de arcade retro: colores, tipografías y estilo de animación.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Pide a Copilot CLI:

> Actualiza las instrucciones del repositorio con una breve guía de diseño para el tema de arcade retro: colores, tipografías, estilo de animación y la regla de que la nueva interfaz debe mantener la estética de neón.
<!-- track:cli:end -->

Haz commit de las instrucciones y los cambios de diseño cuando la página tenga el aspecto que buscas.

## ✅ Parte 4 completada

**Lo que has aprendido:**

- Usar flujos de planificación para esbozar un **sistema de diseño antes de implementarlo**.
- **Iterar sobre el resultado visual** con comentarios rápidos.
- **Actualizar las instrucciones tras tomar decisiones importantes** para mantener la identidad visual.
