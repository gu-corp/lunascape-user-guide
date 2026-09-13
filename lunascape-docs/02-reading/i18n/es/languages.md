# Leer en otro idioma

Cuando un documento tiene traducciones, puede cambiar de idioma desde el menú de idiomas (globo terráqueo) de la barra de herramientas.

## Cambiar el idioma

1. Pulse el menú de idiomas de la barra de herramientas.
   Se muestra el idioma de la página actual y el motivo por el que se determinó (la ruta de la traducción, la detección automática o el idioma predeterminado del proyecto).
2. Elija el idioma en el que quiere leer.
   Se abre la traducción del mismo documento. El idioma elegido se recuerda y, en el siguiente documento que abra, se mostrará en ese idioma si existe una traducción.

La lista de idiomas indica si este documento tiene traducción en cada uno de ellos.

| Indicación | Significado |
|---|---|
| Traducido | Existe una traducción y se puede abrir |
| Sin traducir | El proyecto admite ese idioma, pero este documento todavía no tiene traducción |
| Desactualizado | Existe una traducción, pero el documento original cambió después de traducirla |

> **Nota**
>
> - Elegir un idioma solo abre una traducción que ya existe. Nunca genera una traducción ni crea un archivo. Para crear una traducción, use [Crear y gestionar traducciones…] en el mismo menú.
> - Cuando se detecta que el idioma de la página actual difiere del idioma predeterminado del proyecto, se muestra una advertencia. La configuración nunca se modifica.

## El idioma con el que se abre un documento

Al abrir un documento, el primer idioma de visualización se determina en este orden.

1. El idioma que usted mismo eligió antes en esta raíz de documentación. La elección se guarda (si elige el idioma predeterminado, también se guarda como elección).
2. El idioma de la interfaz de VS Code (en la versión para navegador web, la configuración de idioma del navegador). Se selecciona automáticamente el idioma admitido que coincida. Un idioma con región (como `en-US`) también coincide con su idioma base (`en`).
3. El idioma de reserva del proyecto (`fallbackLocale` en `lunascape-docs.json`).
4. El idioma predeterminado del proyecto.

> **Sugerencia**
>
> - Cuando la selección es automática, el idioma actual del menú de idiomas aparece marcado como «selección automática». Sitúe el puntero sobre la etiqueta para ver el motivo.
> - `fallbackLocale` es el idioma que se muestra a los lectores cuyo entorno no coincide con ninguno de los idiomas admitidos. En un proyecto cuyo original está en japonés y que tiene versión en inglés, si configura `"en"`, a un lector con el entorno en español se le abrirá la versión en inglés. Si no se configura, se usa el idioma predeterminado.

## Dónde se guardan las traducciones

Los documentos en el idioma predeterminado se quedan donde están y las traducciones se colocan en **`i18n/<idioma>/`, dentro de la misma carpeta**, con el mismo nombre de archivo.

```text
docs/
  README.md                  ← default language (for example Japanese)
  i18n/en/README.md          ← its English translation
  guide/
    setup.md
    i18n/en/setup.md         ← its English translation
```

> **Nota**
>
> - No se reconoce la estructura de carpetas reconstruida bajo `i18n/` (`i18n/en/guide/setup.md`). La carpeta `i18n/` debe estar siempre en la misma carpeta que el documento.
> - Ese es el único lugar del que se resuelve una traducción. Colocar además la traducción del mismo documento en el `i18n/` de una carpeta superior no genera ningún conflicto de prioridad: esa copia queda como un archivo huérfano que no aparece ni en el menú de idiomas ni en el registro (y nunca se elimina automáticamente). No guarde la misma traducción en dos lugares.

## Si lee en la versión para navegador web

En la versión para navegador web también puede cambiar de idioma de la misma manera si existe una traducción. Si quiere leer en un idioma que no tiene traducción, puede usar la función de traducción de páginas del navegador. El código, las fórmulas y los diagramas quedan excluidos de la traducción.

## Temas relacionados

- [Entregar trabajo a una IA](../05-ai/README.md)
- [Trabajos que se pueden entregar](../05-ai/tasks.md)
- [Cambiar la configuración de visualización](../02-reading/display-settings.md)
