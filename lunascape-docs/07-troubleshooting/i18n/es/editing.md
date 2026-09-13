# No se puede editar, guardar ni reordenar

## No aparece el botón [Editar]

- [Botón de edición] está desactivado en [Configuración de visualización]. Actívelo o use [⋯] → [Editar] en la parte superior derecha del documento, o bien [Editar] en el menú del elemento del INDEX.
- Ocurre lo mismo cuando `editor.showEditButton` de `lunascape-docs.json` es `false`.
- No se puede editar mientras se muestra la ayuda. Cierre la ayuda.

## No se puede cambiar a la vista visual

«Este documento contiene sintaxis MDX, por lo que no se puede cambiar a la pantalla de edición normal»: los documentos con sintaxis propia de MDX (componentes, `import`, etc.) se editan solo en la vista Markdown, para conservar esa sintaxis.

## No se pueden editar directamente las fórmulas ni los diagramas

La vista visual muestra el resultado representado. Pulse [Markdown] en la pantalla de edición y edite el código fuente.

## No se puede reordenar ni arrastrar

- No se puede reordenar mientras hay un filtro aplicado, mientras se edita un documento ni mientras se procesa otra operación del INDEX.
- Si no confía en el área de trabajo, las acciones de creación, organización y eliminación no están disponibles. Confíe en el área de trabajo en VS Code.
- «El INDEX se ha actualizado. Arrastre de nuevo»: acaba de aplicarse otro cambio. Repita la operación.
- La página de inicio (el `README.md` de la raíz) no se puede mover.

## Aparece «Hay cambios sin guardar»

El archivo en cuestión se está editando en el editor de VS Code. Guarde o descarte los cambios primero y vuelva a intentarlo.

## No se puede cambiar el nombre

No se pueden usar los siguientes nombres.

- Nombres que empiezan por `.`, `i18n` y los nombres reservados de Windows (`CON`, etc.)
- Nombres que terminan en punto o espacio, y nombres que contienen caracteres de control o caracteres no permitidos en nombres de archivo
- Nombres que ya existen en la misma carpeta (incluidos los que solo se diferencian por mayúsculas y minúsculas)
- Nombres de documento sin una extensión de Markdown

## Guardé los cambios, pero no aparecen en Git o no se confirman

Lunascape Docs solo escribe en el archivo; no prepara ni confirma nada en Git. Compruébelo en la vista de control de código fuente de VS Code y confirme los cambios si es necesario.

## Temas relacionados

- [Editar un documento](../03-editing/README.md)
- [Crear y organizar documentos y carpetas](../03-editing/organize.md)
- [Cambiar el orden de los documentos](../03-editing/reorder.md)
