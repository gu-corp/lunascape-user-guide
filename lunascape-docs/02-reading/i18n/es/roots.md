# Cambiar de raíz de documentación

Una raíz de documentación es la carpeta superior de un conjunto de documentos. El INDEX, el filtrado, las comprobaciones y la traducción funcionan por raíz de documentación.

## Cómo se localiza una raíz de documentación

Lunascape Docs recorre las carpetas superiores a partir del archivo Markdown abierto y toma como raíz de documentación la carpeta más cercana que cumpla una de estas condiciones.

- Una carpeta que contiene `lunascape-docs.json` (el nombre de la carpeta es indiferente)
- Una carpeta llamada `docs` (puede añadir más nombres con la opción `lunascapeDocEditor.rootDirectoryNames`)

Al ejecutar «Lunascape Docs: Abrir el visor de especificaciones», se abre la raíz de documentación indicada en la opción `lunascapeDocEditor.root` (valor predeterminado: `docs`).

## Cambiar a otra raíz de documentación

Cuando el área de trabajo tiene varias raíces de documentación, el nombre de la raíz situado en el extremo izquierdo de la barra de herramientas se convierte en una lista desplegable.

1. Pulse el nombre de la raíz de documentación en el extremo izquierdo de la barra de herramientas.
2. Elija una raíz de documentación en la lista.
   Se muestra su página inicial y el INDEX cambia.

> **Sugerencia**
>
> Los nombres de la lista se determinan en este orden. No cambian al cambiar el idioma de la interfaz.
>
> 1. `title` en `lunascape-docs.json`
> 2. `navigation.title` del `README.md` de la raíz y, si no lo tiene, su H1
> 3. `navigation.title` del `index.md` de la raíz y, si no lo tiene, su H1
> 4. El nombre de la carpeta (en una carpeta `docs` estándar, el nombre de su carpeta principal)

## Abrir un Markdown que no pertenece a ninguna raíz de documentación

Al abrir un archivo Markdown que no está dentro de una raíz de documentación, se muestra su carpeta como raíz de documentación temporal. El INDEX presenta los archivos Markdown de esa carpeta y de las que contiene.

- Pulse [Ir a la carpeta superior] en la barra de herramientas para ampliar el alcance hasta la carpeta principal dentro del área de trabajo.
- En esta vista no están disponibles la configuración de idioma del proyecto ni la traducción por lotes. Coloque un archivo `lunascape-docs.json` en la carpeta para convertirla en raíz de documentación y poder usarlas.

## Abrir siempre una raíz de documentación fija

Si asigna el valor `fixed` a la opción `lunascapeDocEditor.rootMode`, se abrirá siempre la raíz de documentación indicada en `lunascapeDocEditor.root`, sea cual sea el archivo Markdown que abra.

## Temas relacionados

- [Raíces de documentación y convenciones de archivos](../04-document-tools/structure.md)
- [Configuración del proyecto](../04-document-tools/project-configuration.md)
- [Lista de opciones de VS Code](../08-reference/settings.md)
