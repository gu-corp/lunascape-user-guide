# El cuadro y sus registros

El cuadro situado en la parte superior de la pestaña [AI] muestra el estado de traducción de cada idioma admitido. Aunque no use la IA, puede ver qué falta.

| Etiqueta | Significado |
|---|---|
| Sin traducir | Número de documentos que aún no tienen traducción |
| Desactualizado | Número de documentos cuya traducción existe, pero cuyo documento original es más reciente que el registro |
| Traducido | Número de traducciones que siguen a su documento original |

El cuadro se calcula recorriendo la raíz de documentación. No interviene ninguna IA ni ningún modelo de lenguaje.

## Actualizar los registros de traducción

Para determinar el estado «desactualizado» es necesario haber registrado el documento original y la traducción tal como estaban en el momento de traducir. La IA de tipo sesión escribe los archivos directamente, por lo que el registro no se crea automáticamente.

1. Cuando termine la traducción y haya revisado el contenido, pulse [Actualizar los registros de traducción].
2. Las traducciones que no tienen registro quedan registradas como correspondientes al documento original actual.

Las sesiones de Claude Code y el guardado con proveedores de tipo API realizan el registro automáticamente (a la sesión se le indica que use la herramienta MCP `record_translation_freshness`). Este botón es necesario cuando la traducción se ha hecho con Codex o con el chat de VS Code.

A partir de ese momento, cuando modifique un documento original, su traducción aparecerá como «desactualizada».

> **Nota**
>
> - Las traducciones que ya tienen un registro no se sobrescriben, para no borrar el estado «desactualizado».
> - Los registros se guardan en `.lunascape-docs/translation-freshness.json`. Solo se guardan la ruta relativa, el idioma, el hash del contenido y la fecha y hora; el texto del documento no se incluye.

## Temas relacionados

- [Trabajo que se puede delegar](tasks.md)
- [Leer en otro idioma](../02-reading/languages.md)
