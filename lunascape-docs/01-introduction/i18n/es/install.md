# Instalar la extensión

La extensión de VS Code «Lunascape Docs Pro» se distribuye como un archivo VSIX. Es gratuita; «Pro» indica que es la edición que entrega el trabajo a una IA y que se actualiza por sí misma.

## Requisitos

- VS Code 1.90 o posterior
- Las funciones que escriben archivos —crear documentos, organizar el INDEX, guardar los ajustes de comprobación, traducir— solo funcionan en un área de trabajo que hayas marcado como de confianza en VS Code.

## Instalar

1. Obtén el archivo VSIX. Este enlace siempre apunta a la versión más reciente.

   [Descargar lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Abre la vista de extensiones (`⇧⌘X` / `Ctrl+Shift+X`).
3. En el menú `…` de la parte superior derecha, elige [Instalar desde VSIX...] e indica el archivo que descargaste.

### Desde la línea de comandos

Una sola línea, si prefieres no salir de la terminal. Descarga e instala.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Nota**
> Si no se encuentra `code`, ejecuta [Shell Command: Instalar el comando 'code' en PATH] desde la paleta de comandos (`⇧⌘P` / `Ctrl+Shift+P`).

## Actualizar

Cuando se publica una versión más reciente, la extensión la obtiene y la instala por sí misma. VS Code te propone recargar la ventana, y es entonces cuando empiezas a usarla. Tus ajustes y documentos se mantienen tal cual.

La comprobación se hace una vez al día. Si quieres comprobarlo ahora mismo, ejecuta [Lunascape Docs: Comprobar actualizaciones] desde la paleta de comandos (`⇧⌘P` / `Ctrl+Shift+P`).

El comportamiento se cambia con el ajuste `lunascapeDocEditor.update.check`.

| Ajuste | Comportamiento |
|---|---|
| Instalar una versión más reciente cuando se publique | Predeterminado |
| Avisarme y decidir cada vez | Aparece una notificación y nada cambia hasta que pulsas [Actualizar] |
| No comprobar | No hace nada |

### Cuando no se puede actualizar

Si aparece «No se pudo obtener la actualización: No Servers», la versión instalada es la 0.22.18 o anterior. La función de actualización de esa versión falla siempre en el último paso tras la descarga, así que no puede pasar por sí misma a una versión más reciente. Vuelve a instalarla a mano una sola vez con los pasos de arriba; a partir de entonces se actualiza sola.

## Comprobar la versión

Abre «Lunascape Docs Pro» en la vista de extensiones para ver la versión instalada. La necesitarás al informar de un problema.

## Temas relacionados

- [Crear tus primeros documentos](first-documents.md)
- [Informar de un problema](../07-troubleshooting/report.md)
