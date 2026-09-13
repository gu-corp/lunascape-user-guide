# Configuración de IA

Elija la IA y el modelo que recibirán su trabajo. Esta pantalla usa sus propias listas desplegables, no la selección rápida de VS Code.

1. Pulse [Herramientas de documentos] → pestaña [IA] → [Configuración de IA…].
2. Elija un [Proveedor].
   Los que este entorno no puede usar aparecen sin poder seleccionarse, junto con el motivo.
3. Elija un [Modelo]. Las opciones cambian según el proveedor.
4. Cierre la pantalla. La elección se guarda por usuario y se reutiliza la próxima vez.

## Proveedores

| Proveedor | Tipo | Detección |
|---|---|---|
| Claude Code | De sesión | Presencia del comando `claude` |
| Codex | De sesión | Presencia del comando `codex` |
| Modelos de lenguaje de VS Code | De API | Modelos registrados en la VS Code Language Model API |
| Anthropic API | De API | Registro de una clave de API |
| API compatible con OpenAI | De API | Registro de una clave de API y un punto de conexión |

Un proveedor **de sesión** lee y escribe los archivos por sí mismo y ejecuta también la comprobación de documentos. Sus resultados se escriben directamente en el árbol de trabajo y se revisan en las diferencias de Git.

Un proveedor **de API** devuelve el Markdown de un documento, y la extensión muestra las diferencias antes de guardar.

## Registrar una clave de API

La Anthropic API y las API compatibles con OpenAI se pueden usar una vez que se registra una clave de API.

1. Elija el destino del registro en [Proveedor]. Aparece el campo para la clave de API.
2. Escriba la [Clave de API]. Para una API compatible con OpenAI, escriba también el [Punto de conexión] (por ejemplo, `https://api.openai.com/v1`).
3. Pulse [Guardar]. Se muestra «Clave registrada».

> **Nota**
>
> - Las claves se guardan en el SecretStorage de VS Code y no se vuelven a mostrar. Tampoco se escriben en `settings.json` ni en ningún documento. Puede borrarlas con [Eliminar clave].
> - La lista de modelos se obtiene de cada servicio con la clave registrada. Mientras no se pueda obtener, se muestra una lista conocida.
> - Con un proveedor de API solo se pueden ejecutar «Traducir esta página» y «Corregir esta página». Para recorrer varios documentos o crear documentos, use un proveedor de sesión.

> **Sugerencia**
>
> Si no se encuentra ningún proveedor, instale Claude Code o Codex, o registre una clave de API. Vuelva a abrir [Configuración de IA…] y se detectará.

## Temas relacionados

- [Entregar trabajo a una IA](README.md)
- [Lista de configuraciones de VS Code](../08-reference/settings.md)
