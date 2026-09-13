# Configuración del proyecto

El archivo `lunascape-docs.json` situado directamente bajo la raíz de documentación contiene la configuración de esa raíz compartida por el equipo. Se gestiona con Git.

## Crear o editar el archivo de configuración

- En la barra de herramientas, pulse [Herramientas de documentos] → pestaña [Comprobación] → [Origen de las reglas y configuración de los documentos] → [Editar la configuración de los documentos] para abrirlo en VS Code. Si el archivo no existe, en ese momento se crea un archivo inicial.
- Al nombre de archivo `lunascape-docs.json` se le asocia automáticamente el JSON Schema incluido, que ofrece autocompletado y una descripción de cada campo. No es necesario indicar `$schema`.

## Ejemplo de configuración

```json
{
  "id": "product-docs",
  "title": "Documentación del producto",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Descripción de los campos

| Campo | Contenido | Predeterminado |
|---|---|---|
| `id` | La clave con la que se guardan los ajustes de visualización de cada usuario. Asígnele un ID fijo cuando quiera conservar los ajustes aunque mueva la carpeta | La ruta de la carpeta |
| `title` | El nombre que se muestra en el extremo izquierdo de la barra de herramientas y en la lista de raíces de documentación. No cambia al cambiar el idioma de visualización | El encabezado del README/index de la raíz; si no lo hay, el nombre de la carpeta |
| `indexTitle` | El encabezado del INDEX | `INDEX` |
| `startPage` | El documento que se abre primero (ruta relativa a la raíz de documentación) | `README.md` |
| `appearance` | El esquema de colores: `light` (siempre claro) o `auto` (sigue el tema de VS Code) | `light` |
| `defaultLocale` | El idioma predeterminado (el idioma del documento canónico). Se indica con una etiqueta de idioma BCP 47 (`ja`, `en`, `zh-Hant`, etc.). Es el origen de las traducciones | Sin definir (se deduce del texto para mostrarlo) |
| `fallbackLocale` | El idioma que se muestra primero a los lectores cuyo entorno no coincide con ninguno de los idiomas admitidos. Indique un idioma incluido en `locales` | Sin definir (se usa `defaultLocale`) |
| `locales` | La lista de idiomas admitidos. Incluya `defaultLocale`. Aparecen en el menú de idiomas y son los destinos de traducción | Solo `defaultLocale` |
| `ignoredDirectories` | Los nombres de carpeta que se excluyen del INDEX, la búsqueda y las comprobaciones. Al indicarlo, se reemplaza el valor predeterminado | `["99-archive"]` |
| `tree` | Los valores predeterminados de la visualización del INDEX. Los usuarios pueden sobrescribirlos en la configuración de visualización | Como en el ejemplo anterior |
| `editor.defaultMode` | La vista de edición mientras el usuario aún no la ha cambiado: `visual` o `source` | `visual` |
| `editor.showEditButton` | Si se muestra [Editar] en la esquina inferior derecha del documento | `true` |
| `documentStandards.pack` | El Standard Pack que se usa para la comprobación de documentos y las plantillas: `builtin:<nombre>` o una ruta relativa a la raíz de documentación | Ninguno |
| `documentStandards.profile` | El nombre de perfil que define el Pack | Ninguno |
| `translation.enabled` | Habilita la creación de propuestas de traducción y la traducción por lotes | `true` |
| `translation.contextFiles` | Los archivos Markdown del canónico (ruta relativa a la raíz de documentación) que se pasan durante la traducción como referencia de terminología y estilo | `[]` |
| `translation.maxContextCharacters` | El límite del total de caracteres de los documentos de referencia (máximo 1048576) | `49152` |
| `description` | Una descripción de una línea del conjunto de documentos. Se muestra en la tarjeta de la página de inicio del repositorio. Igual que `title`, puede escribirse como cadena o como objeto por idioma | Ninguno |

## Indicar dónde están los documentos del repositorio

En el `lunascape-docs.json` situado directamente bajo el repositorio se puede escribir, en lugar de la configuración de esa carpeta, un **mapa del repositorio**. Si escribe cualquiera de los tres campos siguientes, se convierte en un mapa y esa carpeta deja de ser una raíz de documentación.

| Campo | Contenido | Predeterminado |
|---|---|---|
| `defaultFolder` | En qué carpeta están los documentos (ruta relativa a esta carpeta). El destino que indique no necesita archivo de configuración | Ninguno (se usa `docs`) |
| `roots` | Cuando hay varios conjuntos de documentos, su lista (rutas relativas a esta carpeta, en orden de presentación). En este caso, esta carpeta pasa a ser la página de inicio | Ninguno |
| `excludes` | Las carpetas que se excluyen del descubrimiento de raíces de documentación (rutas relativas a esta carpeta). Se suman a las exclusiones predeterminadas, como `node_modules` | `[]` |
| `home.cards` | Si en la página de inicio se muestran las tarjetas de los conjuntos de documentos bajo el README. Póngalo en `false` cuando escriba usted mismo los enlaces en el README | `true` |

La raíz de documentación se determina en el siguiente orden. De arriba abajo, se usa la primera que se encuentre.

1. La carpeta indicada mediante un ajuste o un comando
2. El destino al que apunta `defaultFolder` o `roots` en el `lunascape-docs.json` situado directamente bajo el repositorio
3. La carpeta que contiene un `lunascape-docs.json` (si hay dos o más bajo un padre común, ese padre pasa a ser la página de inicio)
4. La carpeta `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. El propio directorio directamente bajo el repositorio

> **Sugerencia**
>
> Si no escribe nada, actúa la opción 4, de modo que un repositorio normal con un único `docs/` funciona igual que hasta ahora. Escriba `defaultFolder` solo cuando quiera que la carpeta se llame `manual`.

### Ejemplo de mapa

```json
{
  "title": "Ayuda de Lunascape",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Prioridad de la configuración

Los campos relativos a la visualización tienen prioridad en el siguiente orden.

1. La configuración de visualización del usuario (el panel [Configuración de visualización])
2. La configuración de VS Code (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Los valores predeterminados del producto

Solo los idiomas (`defaultLocale`, `fallbackLocale`, `locales`) son una excepción: `lunascape-docs.json` es la fuente de referencia. La configuración personal de VS Code no puede sobrescribir los idiomas del proyecto.

> **Nota**
>
> También se puede indicar un Standard Pack como `standard` en `docs-lint.config.json`. Cuando está en ambos, prevalece `docs-lint.config.json`.

## Temas relacionados

- [Cambiar las reglas de comprobación](rules.md)
- [Cambiar la configuración de visualización](../02-reading/display-settings.md)
- [Lista de ajustes de VS Code](../08-reference/settings.md)
