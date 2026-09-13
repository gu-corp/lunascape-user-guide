# Los documentos no aparecen

## Se muestra «No se encontró ninguna carpeta Markdown o docs que abrir»

- El área de trabajo no tiene una carpeta `docs`, o usa un nombre distinto de `docs`.
  - Si coloca `lunascape-docs.json` en esa carpeta, se reconocerá como raíz de documentación sin importar su nombre.
  - O bien, agregue el nombre de la carpeta a la configuración `lunascapeDocEditor.rootDirectoryNames`.
- Si todavía no hay documentos, créelos con «Lunascape Docs: Crear documentación a partir de una plantilla».
- También puede abrir un archivo Markdown en el editor y ejecutar «Lunascape Docs: Abrir en el visor de especificaciones».

## Un documento no aparece en el INDEX

- Compruebe que la extensión sea `.md`, `.markdown` o `.mdx`.
- Estas carpetas no se muestran: las carpetas que empiezan por `.`, `node_modules` y las carpetas indicadas en `ignoredDirectories` (de forma predeterminada, `99-archive`).
- Las traducciones que están bajo `i18n/` no aparecen por separado en el INDEX. Cambie a ellas desde el menú de idiomas.
- Si un archivo que acaba de agregar no aparece, pulse [Recargar].
- Puede que esté viendo otra raíz de documentación. Compruebe el nombre de la raíz de documentación en el extremo izquierdo de la barra de herramientas.

## Al pulsar una carpeta no se muestra nada

El `README.md` de esa carpeta es un «descriptor solo de configuración»: tiene front matter pero no tiene cuerpo. Abra la carpeta en el INDEX y elija un documento de su interior.

## Se abre una raíz de documentación no deseada

- Si la configuración `lunascapeDocEditor.rootMode` está en `fixed`, siempre se abre `lunascapeDocEditor.root`.
- Con `auto` se elige la raíz de documentación más cercana al archivo Markdown abierto. Puede cambiarla con la lista desplegable del extremo izquierdo de la barra de herramientas.

## El nombre de la raíz de documentación no es el esperado

El nombre se determina en este orden: `title` de `lunascape-docs.json` → `navigation.title` del `README.md` de la raíz → su H1 → `index.md` → el nombre de la carpeta. Si quiere fijarlo, defina `title`.

## El INDEX desapareció

- En una raíz de documentación con un solo documento, el INDEX se cierra automáticamente solo la primera vez. Puede abrirlo con el icono de columnas de la barra de herramientas. Puede desactivarlo en [Configuración de visualización], con [Ocultar si solo hay un documento].
- Cuando la pantalla es estrecha, ábralo desde [Abrir INDEX] (las tres líneas), a la izquierda de [Atrás].

## Al pulsar un enlace no se abre nada

- «No se encontró el destino del enlace»: el archivo de destino no existe. Puede comprobar los enlaces internos con [Comprobación], en Herramientas de documentos.
- «No se abrió un enlace no seguro o no admitido»: no se abren los enlaces que apuntan fuera de la raíz de documentación ni los que usan un esquema distinto de `https://` o `mailto:`.

## Se muestra un idioma distinto del previsto

- En el menú de idiomas, compruebe el idioma de la página que se muestra y el motivo por el que se eligió.
- El idioma de la interfaz que eligió la última vez se recuerda. Vuelva a elegir el idioma predeterminado en el menú de idiomas.
- Si la configuración personal `lunascapeDocEditor.locale` está definida, se da prioridad a la traducción de ese idioma.

## Temas relacionados

- [Cambiar de raíz de documentación](../02-reading/roots.md)
- [Raíces de documentación y convenciones de archivos](../04-document-tools/structure.md)
