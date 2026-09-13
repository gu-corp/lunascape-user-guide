# Configuración de VS Code

En la configuración de VS Code (`⌘,` / `Ctrl+,`), busque «Lunascape Docs» para cambiar los siguientes elementos. Todos son ajustes personales de cada usuario y nunca se guardan en los documentos del proyecto.

## Raíz de documentación

| Ajuste | Valores | Predeterminado | Función |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` elige automáticamente la raíz de documentación más cercana al archivo Markdown abierto y, si no pertenece a ninguna, abre temporalmente la carpeta superior. `fixed` abre siempre la raíz de documentación indicada en `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Matriz de cadenas | `["docs"]` | Nombres de carpeta que se descubren automáticamente como raíces de documentación en el modo `auto`. Una carpeta con `lunascape-docs.json` se descubre sin importar su nombre. Si el archivo `lunascape-docs.json` situado en la raíz del repositorio incluye `defaultFolder` o `roots`, estos tienen prioridad |
| `lunascapeDocEditor.root` | Ruta | `docs` | Raíz de documentación relativa al área de trabajo, para el modo `fixed` o al abrir desde un comando |
| `lunascapeDocEditor.startPage` | Ruta | `README.md` | Página inicial relativa a la raíz de documentación |
| `lunascapeDocEditor.title` | Cadena | `Lunascape Docs` | Reemplaza el título de la pestaña del documento. No afecta al nombre del selector de raíz de documentación |
| `lunascapeDocEditor.ignoredDirectories` | Matriz de cadenas | `["99-archive"]` | Nombres de carpeta que se excluyen del INDEX |

## Visualización

| Ajuste | Valores | Predeterminado | Función |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` usa fondo blanco; `auto` sigue el tema de colores de VS Code |
| `lunascapeDocEditor.locale` | Etiqueta de idioma | Ninguno | Su idioma del documento personal, que se muestra con prioridad cuando está disponible. No cambia el idioma original del proyecto |
| `lunascapeDocEditor.documentMetadata.compact` | Booleano | `true` | Contrae la tabla de gestión del documento situada tras el H1 en una fila «Información del documento» |
| `lunascapeDocEditor.tree.showFileNames` | Booleano | `false` | Muestra los nombres de archivo en lugar de los nombres de documento en el INDEX |
| `lunascapeDocEditor.tree.showDocumentIcons` | Booleano | `false` | Muestra los iconos de documento en el INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | Booleano | `false` | Muestra los iconos de carpeta en el INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | Booleano | `false` | Muestra en el INDEX el número de elementos contenidos directamente en cada carpeta |
| `lunascapeDocEditor.tree.showGuides` | Booleano | `true` | Muestra en el INDEX las líneas guía de la jerarquía |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Espaciado entre filas del INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Booleano | `true` | Cierra el INDEX la primera vez cuando solo hay un documento |

## Edición

| Ajuste | Valores | Predeterminado | Función |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Vista de edición que se usa mientras no se haya cambiado. La última vista utilizada tiene prioridad |
| `lunascapeDocEditor.editor.showEditButton` | Booleano | `true` | Muestra [Editar] en la parte inferior derecha del documento |

## Diagramas

| Ajuste | Valores | Predeterminado | Función |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Entorno de ejecución para dibujar TikZ. `bundled` usa el entorno aprobado incluido con el producto (no se incluye en la versión distribuida actual), `workspace` usa `node-tikzjax` 1.0.5 situado en la raíz de un área de trabajo de confianza (solo para desarrollo y evaluación) y `disabled` no dibuja nada |

## Ajustes obsoletos

| Ajuste | Qué usar en su lugar |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` de `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` de `lunascape-docs.json` |

Los ajustes personales no pueden reemplazar los idiomas del proyecto.

## Temas relacionados

- [Cambiar la configuración de visualización](../02-reading/display-settings.md)
- [Configuración del proyecto](../04-document-tools/project-configuration.md)
