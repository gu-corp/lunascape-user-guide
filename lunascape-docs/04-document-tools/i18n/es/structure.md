# Raíces de documentación y convenciones de archivos

Estas son las reglas que sigue Lunascape Docs para encontrar los documentos y construir el INDEX. El sistema de archivos es en sí mismo el origen de la verdad, por lo que no se necesita ningún registro ni configuración de compilación.

## Raíz de documentación

- La carpeta `docs` más cercana, o una carpeta que contenga `lunascape-docs.json`, se convierte en la raíz de documentación.
- Con un `lunascape-docs.json`, la carpeta no tiene por qué llamarse `docs`.
- Al abrir un archivo Markdown que no pertenece a ninguna raíz de documentación, se muestra su carpeta como raíz de documentación temporal.

## Archivos que se muestran en el INDEX

- Se muestran los archivos `.md`, `.markdown` y `.mdx`. Los archivos nuevos aparecen siempre, incluso sin front matter ni información de navegación.
- No se muestran las carpetas que empiezan por `.`, `node_modules` ni las carpetas indicadas en `ignoredDirectories` (por defecto `99-archive`).
- Todo lo que hay bajo `i18n/` se trata como traducciones y no se lista por separado en el INDEX.

## Portadas de carpeta

- Un `README.md` (o `index.md` cuando no hay README) con contenido en el cuerpo es la portada de su carpeta. Al pulsar el nombre de la carpeta en el INDEX se abre esa portada.
- Un `README.md` que solo contiene front matter, sin cuerpo, se trata como un «descriptor solo de configuración» y no se muestra como página. Úsalo cuando una carpeta solo necesite tener un título o un orden.
- Cuando existen tanto `README.md` como `index.md`, tiene prioridad `README.md`.

## Idioma predeterminado y traducciones

- Los documentos en el idioma predeterminado (documentos canónicos) se mantienen en su sitio.
- La traducción va en una carpeta `i18n/<idioma>/` junto al documento, con el mismo nombre de archivo. No se reconoce reconstruir la estructura de carpetas bajo `i18n/`.
- Esa es la única ubicación desde la que se resuelve una traducción. El mismo archivo colocado en cualquier otro sitio es un archivo huérfano que ningún documento reclama como su traducción.

```text
docs/
  lunascape-docs.json
  README.md                  ← portada de la raíz (página de inicio)
  i18n/en/README.md          ← su traducción al inglés
  01-product/
    README.md                ← portada de la carpeta
    requirements.md
    i18n/en/README.md        ← las traducciones al inglés de los dos anteriores
    i18n/en/requirements.md
  99-archive/                ← excluida del INDEX por defecto
```

## Acerca de `_meta.json`

El `_meta.json` de Nextra no se usa para la navegación. Los archivos existentes no se modifican ni se eliminan. En el futuro, solo una función explícita de importación y exportación se encargará de ellos.

## Temas relacionados

- [Configurar la información de navegación](navigation-metadata.md)
- [Configuración del proyecto](project-configuration.md)
- [Cambiar de raíz de documentación](../02-reading/roots.md)
