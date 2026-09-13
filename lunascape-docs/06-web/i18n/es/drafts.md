# Guardar borradores

Cuando editas un documento en el visor Web, los cambios no se escriben en el repositorio. Se guardan dentro del navegador como un «borrador».

## Crear un borrador

1. Abre un documento y pulsa [Editar] en la parte inferior derecha.
2. Edita y pulsa [Guardar].
   Aparece «Guardado como borrador» y el cambio queda almacenado en el navegador.

- Los documentos con un borrador llevan una insignia en el INDEX. Sobre el texto aparece «Este documento es un borrador en este dispositivo (sin publicar)».
- [Borradores], en la barra de herramientas, muestra la cantidad y, al pulsarlo, abre la lista de borradores.

## Descartar un borrador

- Para descartar el borrador de un documento, pulsa [Descartar el borrador] sobre el texto.
- Para descartarlos todos, hazlo desde la lista de borradores.

## Reflejar los cambios en el repositorio

La «solicitud de publicación», que envía los borradores como Pull Request, está implementada, pero no está habilitada en el visor público. Para reflejar los cambios en el repositorio, edita con la versión de VS Code o en un clon local.

> **Nota**
>
> - Los borradores se guardan en el navegador (IndexedDB). No se transfieren a otro navegador ni a otro dispositivo, y si borras los datos del sitio, los borradores también se eliminan.
> - Si el documento del repositorio se actualiza después de crear el borrador, aparece «El origen se ha actualizado». Revisa el contenido y decide si descartas el borrador o lo sigues usando.
> - Si abres una carpeta local desde [Abrir documentos] y la editas, los cambios se guardan directamente en el archivo si el navegador lo admite. En los navegadores que no lo admiten, se conservan solo durante esa sesión.

## Temas relacionados

- [Qué puedes hacer en la versión Web](README.md)
- [Editar un documento](../03-editing/README.md)
