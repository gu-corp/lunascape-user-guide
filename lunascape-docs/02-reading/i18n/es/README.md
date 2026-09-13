# Operaciones básicas

Operaciones básicas para abrir los documentos y llegar a la página que quiere leer.

## Abrir los documentos

1. Abra el repositorio en VS Code.
2. En la paleta de comandos (`⇧⌘P` / `Ctrl+Shift+P`), ejecute «Lunascape Docs: Abrir el visor de especificaciones».
   Se localiza la raíz de documentación más cercana (de forma predeterminada, la carpeta `docs`) y se muestra su página inicial.

> **Sugerencia**
>
> - Haga clic con el botón derecho en un archivo Markdown del Explorador y elija [Lunascape Docs: Abrir en el visor de especificaciones] para empezar por ese archivo.
> - Si abre un archivo Markdown que no pertenece a ninguna raíz de documentación, su carpeta se muestra como raíz de documentación temporal.

## Desplazarse entre páginas

| Operación | Método |
|---|---|
| Abrir desde el índice | Pulse el nombre de un documento en el INDEX de la izquierda |
| Seguir un enlace | Pulse un enlace del texto. Se abre en la misma vista |
| Recorrer el historial | [Atrás] y [Adelante] en la barra de herramientas, o `Alt`+`←` / `Alt`+`→` |
| Volver a la página inicial | [Inicio de la especificación] en la barra de herramientas |
| Subir un nivel | [INDEX superior] en la barra de herramientas, o un elemento de la ruta de navegación |
| Desplazarse dentro de la página | Pulse un título en «En esta página», a la derecha |

## Buscar un documento

Escriba una palabra en [Filtrar documentos], encima del INDEX, para mostrar solo los documentos cuyo nombre coincida. Borre el texto para volver a la vista anterior.

## Actualizar el contenido

Cuando guarda un archivo Markdown en el editor de VS Code, la vista se actualiza automáticamente. Si ha modificado los archivos con una herramienta externa, pulse [Recargar] en la barra de herramientas.

> **Nota**
>
> - Los enlaces externos del texto (`https://`, etc.) se abren en el navegador predeterminado. Los enlaces a archivos situados fuera de la raíz de documentación no se abren.
> - Los documentos que consulta se procesan en su equipo. No se envía ningún documento al exterior para su lectura.

## Temas relacionados

- [Usar el INDEX](index-panel.md)
- [Cambiar de raíz de documentación](roots.md)
- [Editar un documento](../03-editing/README.md)
