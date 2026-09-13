# Ajustar el tamaño de las imágenes

Las imágenes pegadas en un documento se ajustan automáticamente al ancho del texto y a la altura de la pantalla. Para una imagen que quieras mostrar con un tamaño concreto, puedes especificar su ancho.

## Cómo funciona el ajuste automático

- Una imagen de Markdown normal (`![descripción](./images/screen.png)`) se reduce para que quepa en el ancho del texto. Nunca se amplía más allá de su tamaño original.
- Una captura de pantalla alargada se limita al 72 % de la altura de la pantalla o a 720px, lo que sea menor.

## Especificar el ancho en la pantalla de edición

1. Pulsa [Editar] y selecciona la imagen en la vista visual.
2. Elige un ancho en [Tamaño de la imagen] de la barra de herramientas.
3. Pulsa [Guardar].

| Opción | Ancho |
|---|---|
| [Automático] | Sin especificar (ajuste automático) |
| [Pequeño (360px)] | 360px |
| [Mediano (560px)] | 560px |
| [Grande (760px)] | 760px |
| [Ancho del texto (920px)] | 920px |
| [Personalizado…] | Cualquier número entero de 16 a 4096px |

## Especificar el ancho en Markdown

Asigna un `width` numérico a la etiqueta HTML `img`. Es una forma de escritura que se muestra igual en GitHub y en MDX.

```html
<img src="./images/screen.png" alt="Pantalla de ajustes" width="360" />
```

> **Nota**
>
> - En `width` se indica solo un número. No se añade `px` ni `%`. Aunque especifiques un valor mayor que el ancho del texto, se mostrará ajustado al ancho del texto.
> - Las imágenes se indican con una ruta relativa desde el documento. Las imágenes que están fuera de la raíz de documentación no se muestran.

## Temas relacionados

- [Editar un documento](README.md)
- [Los diagramas, las fórmulas o las imágenes no se muestran](../07-troubleshooting/rendering.md)
