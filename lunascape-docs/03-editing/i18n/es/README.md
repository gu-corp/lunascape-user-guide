# Editar un documento

Los documentos se pueden editar directamente dentro del visor. La pantalla de edición tiene una vista visual, donde se edita lo que se ve, y una vista de código fuente Markdown; un solo botón alterna entre ambas.

## Empezar a editar

Presione cualquiera de las siguientes opciones. Todas abren la misma pantalla de edición.

- [Editar], en la parte inferior derecha del documento
- [⋯] (Más acciones), en la parte superior derecha del documento → [Editar]
- El menú del elemento en INDEX → [Editar]

## Editar

1. Edite el texto directamente.
   En la barra de herramientas de la parte superior de la pantalla de edición puede usar el formato de párrafo (texto normal, títulos 1 a 4, cita, código), [Negrita], [Cursiva], [Lista con viñetas], [Lista numerada], [Enlace], [Insertar una tabla], [Tamaño de la imagen], [Deshacer] y [Rehacer].
2. Para editar el código fuente Markdown directamente, presione [Markdown].
   Presiónelo otra vez para volver a la vista visual. Se recuerda la última vista utilizada y se restaura la próxima vez que presione [Editar].
3. Presione [Guardar].
   El contenido se escribe en el archivo Markdown y el visor vuelve al modo de lectura. Para descartar los cambios, presione [Cancelar].

> **Nota**
>
> - Al guardar solo se escribe el archivo. El área de preparación y la confirmación de Git nunca se hacen de forma automática.
> - Las fórmulas y los diagramas como Mermaid, TikZ o Vega-Lite se muestran ya representados en la vista visual. Para cambiar su contenido, cambie a [Markdown].
> - Los documentos que contienen sintaxis propia de MDX (componentes, `import`, etc.) se editan solo en la vista Markdown, para conservar esa sintaxis.
> - El front matter (la configuración delimitada por `---` al principio del archivo) se conserva aunque edite en la vista visual.

> **Sugerencia**
>
> - Al presionar [Abrir en VS Code], el archivo se abre en el editor de texto habitual. Si guarda allí, la vista del visor se actualiza automáticamente.
> - Si no desea que se muestre el botón [Editar], desactive [Botón de edición] en [Configuración de visualización]. Para ocultarlo en todo el proyecto, establezca `editor.showEditButton` en `false` en `lunascape-docs.json`.
> - La vista que se abre primero (visual o Markdown) se puede cambiar con la configuración `lunascapeDocEditor.editor.defaultMode` o con `editor.defaultMode` en `lunascape-docs.json`.

## Temas relacionados

- [Crear y organizar documentos y carpetas](organize.md)
- [Ajustar el tamaño de las imágenes](images.md)
- [Escribir fórmulas](math.md)
- [Escribir diagramas y gráficos](diagrams.md)
