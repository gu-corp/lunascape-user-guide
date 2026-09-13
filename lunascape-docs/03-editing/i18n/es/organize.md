# Crear y organizar documentos y carpetas

Desde el menú de elementos del INDEX puede crear, duplicar, cambiar de nombre y eliminar documentos y carpetas. Los datos se escriben en un pequeño cuadro de diálogo dentro del visor, sin interrumpir la lectura.

> **Nota**
>
> Estas acciones solo están disponibles cuando el área de trabajo es de confianza en VS Code. No se pueden ejecutar mientras se edita un documento, mientras hay otra operación en curso ni cuando el elemento tiene cambios sin guardar.

## Crear un documento o una carpeta

1. Abra el menú de elementos ([⋯] o clic derecho) de la carpeta de destino.
   Para crear el elemento directamente en la raíz de documentación, use [⋯] en el extremo derecho del encabezado del INDEX o haga clic derecho en una zona vacía del INDEX.
2. Elija [Nuevo documento] o [Nueva carpeta].
3. Escriba un nombre y pulse [Crear].
   El nombre de un documento necesita una extensión de Markdown (`.md`, `.markdown`, `.mdx`, etc.).

Los documentos nuevos se crean como documentos del idioma predeterminado (documento original).

## Duplicar un documento

1. Abra el menú de elementos del documento y elija [Duplicar].
2. Escriba un nombre nuevo y pulse [Crear].

Solo se duplica el documento original; sus traducciones no.

## Cambiar el título

Cambia el encabezado del documento (H1). El nombre del archivo no varía.

1. Abra el menú de elementos de un documento o una carpeta y elija [Cambiar el título].
2. Escriba el título nuevo en una sola línea y pulse [Cambiar].

En el caso de una carpeta, se cambia el encabezado de su `README.md`. Cuando se muestra una traducción, cambia el título del documento de ese idioma.

## Cambiar el nombre del documento

Cambia el nombre del documento que aparece en la barra de herramientas (el nombre de la raíz de documentación).

1. Haga clic derecho en el nombre del documento en la barra de herramientas. También puede abrir el mismo menú desde [⋯] en el extremo derecho del encabezado del INDEX.
2. Elija [Cambiar el nombre del documento] y escriba un nombre nuevo.

Mientras no haya nada configurado, se muestra el nombre de la carpeta tal cual.

El nombre que establezca se escribe en **el lugar que proporciona actualmente el nombre del documento**, de modo que un encabezado visible nunca quede ignorado.

| Estado actual | Dónde se escribe |
|---|---|
| `lunascape-docs.json` contiene un nombre | Se actualiza `lunascape-docs.json` |
| No hay nombre, pero la raíz de documentación tiene un README | Se reescribe el encabezado (H1) del README |
| Ninguno de los dos | Se crea `lunascape-docs.json` y el nombre se guarda ahí |

El mensaje que aparece tras el cambio indica en cuál de ellos se escribió.

> **Sugerencia**
>
> El nombre del documento se determina en este orden: el nombre en `lunascape-docs.json`, luego el encabezado del README de la raíz de documentación y, por último, el nombre de la carpeta.

## Cambiar el nombre de un archivo o una carpeta

1. Abra el menú de elementos y elija [Cambiar el nombre del archivo] o [Cambiar el nombre de la carpeta].
2. Escriba el nombre nuevo y pulse [Cambiar].

Las traducciones correspondientes (la misma ruta bajo `i18n/<idioma>/`) se renombran junto con el elemento.

## Eliminar

1. Abra el menú de elementos y elija [Mover a la papelera].
2. Revise el mensaje de confirmación y apruebe el movimiento.

El elemento se mueve a la papelera del sistema operativo, así que puede restaurarlo si lo necesita. Las traducciones no se eliminan y permanecen en su lugar.

## Nombres que no se pueden usar

- Nombres que empiezan por `.` (no aparecerían en el INDEX)
- `i18n` (reservado para los archivos de traducción)
- Nombres reservados por Windows (`CON`, `PRN`, etc.)
- Nombres que terminan en punto o en espacio
- Nombres con caracteres de control o con caracteres no permitidos en nombres de archivo
- Nombres que ya existen en la misma carpeta (incluidos los que solo se diferencian en mayúsculas y minúsculas)

> **Nota**
>
> La página de inicio (normalmente el `README.md` de la raíz) no se puede renombrar ni mover. Cambie antes `startPage` en `lunascape-docs.json`.

## Temas relacionados

- [Cambiar el orden de los documentos](reorder.md)
- [Usar el INDEX](../02-reading/index-panel.md)
