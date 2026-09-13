# Cambiar el orden de los documentos

El orden que se muestra en el INDEX se puede cambiar arrastrando y soltando o con el teclado. El orden modificado se guarda en el front matter del documento como `navigation.order`.

## Reordenar arrastrando y soltando

1. Arrastre un documento o una carpeta en el INDEX.
2. Suéltelo antes o después de un elemento del mismo nivel, o sobre una carpeta.
   Dentro del mismo nivel cambia el orden. Si lo suelta sobre otra carpeta, el elemento se mueve a esa carpeta.

## Reordenar con el teclado o el menú

- Coloque el foco en un elemento del INDEX y pulse `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Elija [Mover una posición hacia arriba] / [Mover una posición hacia abajo] en el menú del elemento.

## Qué se guarda

- Al reordenar dentro del mismo nivel se actualiza `navigation.order` en el front matter del documento original. En el caso de una carpeta, se escribe en el `README.md` de esa carpeta. Si la carpeta no tiene `README.md`, se crea un `README.md` que contiene solo el front matter.
- Al mover un elemento a otra carpeta, el documento original y sus traducciones se mueven juntos. Antes del traslado se muestra una confirmación sobre el efecto en los enlaces relativos.
- No se realiza ninguna preparación ni confirmación de cambios en Git.

> **Nota**
>
> - No se puede reordenar mientras hay un filtro aplicado, mientras se edita un documento ni en un área de trabajo que no es de confianza.
> - Cuando aparece «El INDEX se ha actualizado», es porque acaba de aplicarse otro cambio. Repita la operación.
> - La página de inicio no se puede mover a otra carpeta.

> **Sugerencia**
>
> Si asigna a `navigation.order` valores de 100 en 100, como 100, 200 y 300, después será más fácil insertar documentos entre ellos. Para más información, consulte [Configurar la información de navegación](../04-document-tools/navigation-metadata.md).

## Temas relacionados

- [Crear y organizar documentos y carpetas](organize.md)
- [Configurar la información de navegación](../04-document-tools/navigation-metadata.md)
