# Consultar un repositorio privado

Los documentos de repositorios privados se pueden consultar tras iniciar sesión con GitHub, limitados a aquellos sobre los que tiene permiso de lectura. Lunascape Docs nunca tiene cuentas ni permisos propios.

## Iniciar sesión y abrir

1. Abra <https://docs.lunascape.org/>.
   Cuando indica un documento privado o aún no ha iniciado sesión, aparece la pantalla de inicio de sesión.
2. Pulse [Iniciar sesión con GitHub].
   La pantalla de autorización de GitHub se abre en una ventana emergente.
3. Cuando haya iniciado sesión, pulse [Abrir documentos] en la barra de herramientas y elija el repositorio que desea abrir en [Elegir entre los repositorios que puede leer].

> **Sugerencia**
>
> - El nombre de la cuenta con la que ha iniciado sesión se muestra en la barra de herramientas. Desde ahí también puede [Cerrar sesión] o [Iniciar sesión con otra cuenta].
> - En la lista aparecen los repositorios de las cuentas (organizaciones o personas) en las que está instalada la GitHub App «Lunascape Docs», limitados a aquellos sobre los que tiene permiso de lectura.

## Configuración que realiza el propietario del repositorio

Si el repositorio deseado no aparece en la lista, el propietario del repositorio o el administrador de la organización debe instalar la GitHub App «Lunascape Docs».

- Los permisos solicitados son Contents (lectura y escritura) y Pull requests (lectura y escritura). La lectura es para la consulta; la escritura es para la solicitud de publicación (Pull Request) desde la Web. Lunascape Docs nunca guarda el contenido de los documentos.
- La instalación se realiza por cuenta (organización o persona). Se configura si el alcance es «All repositories» (que incluye automáticamente los repositorios que se creen en adelante) o solo los repositorios seleccionados.

| Situación | Procedimiento |
|---|---|
| Instalar por primera vez en una organización o cuenta personal | Realícelo desde la [página de instalación](https://github.com/apps/lunascape-docs/installations/new) |
| Añadir repositorios en una organización que ya lo tiene instalado | Configúrelo en Settings de la organización → GitHub Apps → Lunascape Docs → Configure → Repository access |

Aunque se instale para toda la organización, cada miembro solo puede consultar los repositorios sobre los que tiene permiso de lectura. Y solo puede enviar solicitudes de publicación a los repositorios sobre los que tiene permiso de escritura.

> **Sugerencia**
> - Al instalarlo por primera vez, los permisos solicitados se muestran en una lista en la pantalla de instalación, y al pulsar «Install» quedan aprobados. No hay ninguna operación adicional.
> - Las organizaciones que ya tenían la app instalada antes de que se añadiera un permiso reciben un correo de confirmación dirigido a sus administradores, y aparece un botón de aprobación en la parte superior de Settings de la organización → GitHub Apps → Lunascape Docs → Configure. Hasta que lo aprueben, en esa organización solo se puede consultar, y al enviar una solicitud de publicación se muestra «Se requiere conceder permiso de escritura».
> - Puede comprobar con qué permisos está instalada actualmente en esa misma pantalla Configure. En el caso de una cuenta personal, es Settings → Applications → Installed GitHub Apps.
> - Si por error ha quitado un repositorio del alcance o ha desinstalado la app, puede restaurarlo volviéndolo a instalar desde la [página de instalación](https://github.com/apps/lunascape-docs/installations/new). El mensaje de rechazo de la solicitud de publicación incluye un enlace a la pantalla donde corregirlo.
> - Si en el lado del repositorio no desea aceptar solicitudes de publicación, escriba `"publish": { "enabled": false }` en `lunascape-docs.json`. La consulta sigue funcionando con normalidad.

## Temas relacionados

- [Abrir un repositorio de GitHub](open-repository.md)
- [No se puede abrir o iniciar sesión en la versión Web](../07-troubleshooting/web.md)
