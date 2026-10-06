# Editar un documento

Los documentos se pueden editar directamente dentro del visor. La pantalla de edición tiene una «vista visual», donde editas lo que ves, y una «vista de código Markdown»; un solo botón alterna entre ambas.

## Empezar a editar

Pulsa cualquiera de las siguientes opciones. Todas abren la misma pantalla de edición.

- [Editar], abajo a la derecha del documento
- [⋯] (Más acciones), arriba a la derecha del documento → [Editar]
- El menú del elemento en el INDEX → [Editar]

## Editar

1. Edita el texto directamente.
   En la barra de herramientas de la parte superior de la pantalla de edición puedes usar el formato de párrafo (cuerpo, títulos 1 a 4, cita, código), [Negrita], [Cursiva], [Lista con viñetas], [Lista numerada], [Enlace], [Insertar una tabla], [Tamaño de la imagen], [Deshacer] y [Rehacer].
2. Si quieres editar directamente el código Markdown, pulsa [Markdown].
   Vuelve a pulsarlo para regresar a la vista visual. Se recuerda la última vista que usaste y se restaura la próxima vez que pulses [Editar].
3. Pulsa [Guardar] (también puedes guardar con Ctrl+S / ⌘S).
   Se escribe en el archivo Markdown y se regresa a la vista de lectura. Para dejar de editar y volver al contenido guardado por última vez, pulsa [Descartar cambios].

## Empezar siempre en la pantalla de edición (modo de edición)

Pulsa [Modo de edición] en la barra de herramientas para activarlo: a partir de entonces, cada documento se abre en la pantalla de edición. Se usa cuando escribes de forma continua, como en un bloc de notas.

- Mientras está activado, pulsar [Guardar] no cierra la pantalla de edición. [Descartar cambios] regresa al contenido guardado por última vez y mantiene abierta la pantalla de edición.
- Vuelve a pulsarlo para desactivarlo y regresar a la vista de lectura. El estado activado o desactivado se recuerda para cada usuario.
- No se muestra en raíces de documentación en las que no se puede escribir (por ejemplo, una fuente de GitHub de solo lectura).

## Ediciones sin guardar

Las ediciones que no has guardado se conservan automáticamente en este dispositivo. No se pierden aunque pases a otro documento o cierres la pestaña o la ventana.

- [Sin guardar] en la pantalla de edición indica que hay diferencias con el contenido guardado por última vez.
- La próxima vez que abras el mismo documento, se reanuda desde las ediciones conservadas y así se te indica. Si el documento original se ha actualizado desde entonces, también se te avisa. Con [Descartar cambios] puedes volver al contenido más reciente.
- Las ediciones conservadas desaparecen con [Guardar] o [Descartar cambios]. Como no se han guardado, no aparecen en Git ni entre los borradores.

> **Nota**
>
> - Guardar solo escribe en el archivo. La preparación (staging) y la confirmación (commit) en Git nunca se hacen de forma automática.
> - Las fórmulas y los diagramas como Mermaid, TikZ y Vega-Lite se muestran renderizados en la vista visual. Para cambiar su contenido, cambia a [Markdown].
> - Los documentos que contienen sintaxis propia de MDX (componentes, `import`, etc.) se editan solo en la vista Markdown, para preservar esa sintaxis.
> - El front matter (la configuración delimitada por `---` al principio) se conserva aunque lo edites en la vista visual.

> **Sugerencia**
>
> - [Abrir en VS Code] abre el archivo en el editor de texto habitual. Al guardar allí, la vista del visor también se actualiza automáticamente.
> - Si no quieres que se muestre el botón [Editar], desactiva [Botón de edición] en [Configuración de visualización]. Para ocultarlo en todo el proyecto, establece `editor.showEditButton` en `false` en `lunascape-docs.json`.
> - La vista inicial predeterminada (visual o Markdown) se puede cambiar con la opción `lunascapeDocEditor.editor.defaultMode` o con `editor.defaultMode` en `lunascape-docs.json`.

## Temas relacionados

- [Crear y organizar documentos y carpetas](organize.md)
- [Ajustar el tamaño de las imágenes](images.md)
- [Escribir fórmulas](math.md)
- [Escribir diagramas y gráficos](diagrams.md)
