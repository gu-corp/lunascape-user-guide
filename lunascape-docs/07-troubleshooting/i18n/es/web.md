# No se puede abrir la versión Web ni iniciar sesión

## Inicié sesión, pero el repositorio no aparece en la lista

La GitHub App «Lunascape Docs» no está instalada en esa cuenta, o el repositorio no está incluido. Pida al propietario del repositorio o al administrador de la organización que la instale siguiendo los pasos de [Ver un repositorio privado](../06-web/private-repository.md).

## No se puede pasar de la pantalla de inicio de sesión

- No tiene permiso de lectura sobre el repositorio. Pida al propietario del repositorio que se lo conceda.
- «Este sitio no tiene configurado el inicio de sesión con GitHub»: el visor que usted mismo instaló no tiene configurado un servicio de inicio de sesión. Un administrador debe configurarlo.

## No se abre la ventana emergente de inicio de sesión

El navegador está bloqueando las ventanas emergentes. Permita las ventanas emergentes de este sitio e inténtelo de nuevo.

## Aparece «La sesión ha caducado»

La sesión ha caducado. Vuelva a pulsar [Iniciar sesión con GitHub].

## Al abrir un repositorio público aparece un error 404

- Compruebe la forma `owner/repo@ref/dir`.
- No se pueden indicar nombres de rama que contengan `/`.

## Al cabo de un rato deja de cargarse

Si no ha iniciado sesión, se aplica el límite de uso de la API de GitHub (60 solicitudes por hora). Si aparece «Se ha alcanzado el límite de solicitudes», espere un momento o pulse [Iniciar sesión con GitHub].

## Aparece «Este sitio no puede mostrar este repositorio»

Para abrirlo desde un visor que usted mismo instaló, hay que añadir la URL de ese sitio a `viewer.origins` en el `lunascape-docs.json` del repositorio.

## Al abrir `index.html` no se muestra nada

No funciona si se abre directamente con `file://`. Ábralo a través de un servidor HTTP o utilice la versión para VS Code.

## En el sitio exportado aparece «No se encuentra lunascape-docs-manifest.json»

Publique tal cual el conjunto completo de archivos generado por `npm run export:web`, incluido el manifiesto.

## No se pueden guardar los borradores

- «No se puede abrir IndexedDB» / «Está en uso en otra pestaña»: se debe al modo privado del navegador o a otra pestaña que tiene abierto el mismo sitio. Ábralo en una ventana normal y cierre las demás pestañas.
- Los borradores se guardan por dispositivo y navegador. No se transfieren a otro dispositivo.

## Temas relacionados

- [Abrir un repositorio de GitHub](../06-web/open-repository.md)
- [Guardar borradores](../06-web/drafts.md)
