# Cambiar las reglas de comprobación

Puede cambiar el nivel de aviso (error, advertencia, información) de cada comprobación o desactivarla. Los cambios se guardan en el archivo `docs-lint.config.json` de la raíz de documentación y se comparten con el equipo.

## Cambiar un nivel de aviso

1. Pulse [Herramientas de documentos] en la barra de herramientas y abra la pestaña [Comprobación].
2. Pulse [Revisar y cambiar las reglas].
   La lista de comprobaciones se despliega dentro de la misma tarjeta. Cada elemento muestra su finalidad y el origen de su configuración actual (Project, Profile, Pack o Default).
3. Elija el nivel de aviso del elemento que quiera cambiar.
4. Pulse [Guardar y comprobar de nuevo].
   La configuración se guarda y toda la raíz de documentación se vuelve a comprobar con los nuevos ajustes.

| Opción | Significado |
|---|---|
| [Configuración estándar (…)] | Elimina la anulación y vuelve a la configuración estándar, determinada por el perfil, el Standard Pack y el valor predeterminado, en ese orden |
| [No usar] | No realiza esta comprobación |
| [Información] / [Advertencia] / [Error] | Informa con este nivel de aviso |

> **Nota**
>
> - Para guardar se necesita un área de trabajo de confianza.
> - Solo se guarda el nivel de aviso de cada elemento. Las opciones de cada elemento se conservan tal como están. El Standard Pack y el perfil no se modifican desde esta pantalla.
> - Si `docs-lint.config.json` se modificó externamente justo antes de guardar, la operación se cancela. Cargue el estado más reciente e inténtelo de nuevo.
> - Si `docs-lint.config.json` no existe, se crea al guardar.

## Editar directamente los archivos de configuración

- Al pulsar [Abrir la configuración avanzada] se abre `docs-lint.config.json` en VS Code.
- Abra [Origen de las reglas y configuración de los documentos] y pulse [Editar la configuración de los documentos] para abrir `lunascape-docs.json` en VS Code. El Standard Pack y el perfil se eligen ahí.

En ambos archivos están disponibles el autocompletado y las descripciones que aportan los esquemas JSON Schema incluidos con la extensión.

## Standard Pack y perfiles

Un Standard Pack es un estándar de documentación que reúne los tipos de documento necesarios, la estructura de capítulos, la terminología y las plantillas. Se elige con `documentStandards` en `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

El Pack incluido `builtin:gu-corp-software` ofrece los perfiles `base`, `web-application`, `api-service`, `regulated-financial-product` y `smart-contract`.

## Temas relacionados

- [Comprobar documentos](check.md)
- [Configuración del proyecto](project-configuration.md)
