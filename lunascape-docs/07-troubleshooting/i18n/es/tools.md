# La comprobación, la creación o la traducción no funcionan

## Comprobación

### Aparece «No se puede usar docs-lint»

- El entorno de ejecución de docs-lint no está incluido en la extensión o hay un problema en la configuración. Vuelva a instalar la extensión.
- «Para cargar de forma segura el pack local y la configuración, confíe en esta área de trabajo en VS Code»: para usar un Standard Pack local se necesita un área de trabajo de confianza.

### El resultado se queda en «Se requiere volver a comprobar»

Al modificar un documento o la configuración, el resultado anterior deja de ser válido. Vuelva a pulsar [Comprobar la raíz de documentación]. Los cambios sin guardar no se tienen en cuenta.

### Al pulsar una advertencia no se abre nada

Los elementos de «Toda la raíz de documentación» no están vinculados a un documento concreto, por lo que no tienen una posición. Revise el documento correspondiente según el contenido de la advertencia.

### No se pueden guardar las reglas

- Se necesita un área de trabajo de confianza.
- «La configuración de Lint se modificó desde otra operación»: `docs-lint.config.json` se modificó desde fuera. Cargue el estado más reciente y vuelva a intentarlo.
- No se pueden editar los enlaces simbólicos ni los archivos de configuración situados fuera de la raíz de documentación.

## Creación a partir de una plantilla

- «La vista previa de la plantilla ha caducado» / «El contenido introducido ha cambiado»: vuelva a pulsar [Vista previa] y después cree el documento.
- «El documento de destino ya existe»: los archivos existentes no se sobrescriben. Indique otro destino.
- El destino requiere una ruta relativa a la raíz de documentación y la extensión `.md` o `.mdx`. No se puede crear nada dentro de `i18n`.
- «Para crear documentos, confíe en el área de trabajo»: confíe en el área de trabajo en VS Code.

<!-- ai-only:start -->
## Traducción

### No se pueden pulsar los botones de traducción

- «La traducción con IA no está habilitada en esta raíz de documentación»: establezca `translation.enabled` en `true` en `lunascape-docs.json`.
- «El idioma predeterminado del proyecto no está definido»: guarde el idioma predeterminado en [Cambiar la configuración de visualización](../02-reading/display-settings.md).
- «Añada el idioma de destino a los idiomas admitidos»: añada el idioma de destino a `locales`.
- «No se encuentra el documento original que traducir»: tiene abierta una página traducida. Cambie a la página en el idioma predeterminado.
- La traducción por lotes no está disponible en una vista temporal de carpeta. Coloque un archivo `lunascape-docs.json` en esa carpeta para convertirla en una raíz de documentación.

### La propuesta de traducción se rechaza o se pide rehacerla

- «El documento original ha cambiado. Vuelva a generar la propuesta de traducción»: el documento original o el destino cambiaron después de generar la propuesta. Traduzca de nuevo.
- No se acepta la respuesta del modelo de lenguaje si le faltan identificadores o código que deben protegerse. Puede consultar el contenido de la respuesta en el panel de salida «Lunascape Docs 翻訳».
- «La traducción por lotes admite hasta 1000 documentos por vez»: divida el alcance por carpetas o mediante una selección explícita.
<!-- ai-only:end -->

## Temas relacionados

- [Comprobar documentos](../04-document-tools/check.md)
- [Crear un documento a partir de una plantilla](../04-document-tools/templates.md)
- [Entregar trabajo a una IA](../05-ai/README.md)
