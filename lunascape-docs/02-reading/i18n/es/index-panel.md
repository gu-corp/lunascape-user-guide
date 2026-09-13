# Usar el INDEX

El INDEX, a la izquierda de la pantalla, es el árbol de carpetas y documentos de la raíz de documentación.

## Filtrar

1. Escriba una palabra en [Filtrar documentos], encima del INDEX.
2. Solo se muestran los elementos cuyo nombre coincide. Borre lo escrito para volver al estado anterior.

> **Nota**
>
> Mientras hay un filtro activo, no se puede reordenar arrastrando y soltando.

## Abrir y cerrar carpetas

- Pulse la flecha situada a la izquierda del nombre de la carpeta, o el nombre de una carpeta sin portada, para abrirla o cerrarla.
- Si la carpeta tiene portada (un `README.md` o un `index.md` con contenido), al pulsar su nombre se abre la portada. Para solo abrirla o cerrarla, use [Abrir carpeta] / [Cerrar carpeta] en el menú del elemento.
- El estado de apertura de las carpetas se guarda para cada usuario y no se escribe en los archivos gestionados por Git.

## El README y la portada de la carpeta

`README.md` es el archivo que describe el contenido de esa carpeta.

- En una carpeta con README, al pulsar el nombre de la carpeta se muestra ese README.
- En una carpeta sin README se muestra el primer documento que contiene.
- El título (H1) del README pasa a ser el nombre de esa carpeta en el INDEX.

El README no es obligatorio. Para añadirlo después, elija [Crear un README] en el menú del elemento de la carpeta (solo aparece en las carpetas que no tienen README).

## Mostrar u ocultar el INDEX

- El icono izquierdo del control de columnas de la barra de herramientas muestra u oculta el INDEX. El icono derecho muestra u oculta «En esta página».
- Cuando la pantalla es estrecha, el INDEX empieza cerrado. Pulse [Abrir INDEX] (las tres líneas) que aparece a la izquierda de [Atrás] y el INDEX se abre superpuesto al documento. Se cierra con el [×] del INDEX, al hacer clic en el fondo, con `Esc` o al cambiar de documento. Esta apertura temporal no modifica la configuración de las pantallas anchas.
- En una raíz de documentación con un solo documento visible, el INDEX se cierra automáticamente la primera vez. Puede volver a abrirlo con el icono de columnas. Este comportamiento se desactiva en [Configuración de visualización], con [Ocultar si solo hay un documento].

## Usar el menú del elemento

Sitúe el puntero sobre un elemento del INDEX para que aparezca [⋯], o haga clic con el botón derecho en el elemento, para abrir su menú. Los elementos se ordenan así.

| Grupo | Elementos |
|---|---|
| Acciones frecuentes | [Abrir carpeta] / [Cerrar carpeta], [Abrir INDEX] (abre la portada de la carpeta), [Editar], [Cambiar el título], [Abrir en VS Code], [Copiar la ruta] |
| Crear y organizar | [Crear un README] (solo en carpetas sin README), [Nuevo documento], [Nueva carpeta], [Duplicar], [Cambiar el nombre del archivo] / [Cambiar el nombre de la carpeta], [Mover una posición hacia arriba], [Mover una posición hacia abajo] |
| Eliminar | [Mover a la papelera] |

- Para crear directamente en la raíz de documentación, pulse [⋯] en el extremo derecho del encabezado del INDEX, o haga clic con el botón derecho en una zona vacía del INDEX, y elija [Nuevo documento] o [Nueva carpeta]. En ese mismo menú están [Cambiar el nombre del documento] y, si la raíz de documentación no tiene README, [Crear un README]. El mismo menú se abre al hacer clic con el botón derecho en el nombre del documento que aparece en la barra de herramientas.
- Dentro del menú, `↑` `↓` se desplazan entre los elementos y `Home` `End` van al primero y al último. Al cerrarlo con `Esc`, el foco vuelve a donde estaba antes de abrirlo.

> **Nota**
>
> Los elementos de creación, organización y eliminación solo aparecen cuando el área de trabajo es de confianza en VS Code. Tampoco están disponibles mientras se edita un documento ni mientras se procesa otra operación del INDEX.

## Cambiar el aspecto

Desde [Configuración de visualización] puede cambiar la visualización de los nombres de archivo, los iconos de documentos y carpetas, el número de elementos de cada carpeta, las líneas guía de jerarquía y la densidad de visualización. Para más detalles, consulte [Cambiar la configuración de visualización](display-settings.md).

## Temas relacionados

- [Crear y organizar documentos y carpetas](../03-editing/organize.md)
- [Cambiar el orden de los documentos](../03-editing/reorder.md)
