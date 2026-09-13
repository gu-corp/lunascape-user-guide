# Los diagramas, las fórmulas o las imágenes no se muestran

## Una figura TikZ aparece como código fuente plegado

- La extensión que se distribuye no incluye el motor de dibujo de TikZ. Esta visualización es la normal.
- Para desarrollo y evaluación, instale `node-tikzjax` 1.0.5 directamente en la raíz de un área de trabajo de confianza y establezca la opción `lunascapeDocEditor.tikz.runtime` en `workspace`; así se dibujarán las figuras.
- El visor web no dibuja TikZ.

## Las fórmulas se muestran como texto normal

- Compruebe los delimitadores: `$...$` o `\(...\)` para las fórmulas en línea, y `$$...$$` o `\[...\]` para las fórmulas independientes.
- Un `$` dentro de código en línea o de un bloque de código nunca es una fórmula.
- El texto que parece un importe, como `$5 and $10`, no se trata como fórmula.
- Las fórmulas muy grandes o con mucha expansión de macros no se dibujan si superan los límites (`maxSize: 50`, `maxExpand: 1000`). Divídalas.

## Un diagrama indica «No se puede dibujar»

- El mensaje de error de Mermaid, Vega-Lite, WaveDrom y otros indica el problema de sintaxis. Compruebe el código fuente con [Markdown] en la pantalla de edición.
- Vega-Lite: incruste los datos en `data.values` o en `datasets`. No se pueden usar datos de una URL externa ni marcas de imagen.
- WaveDrom: escriba JSON estricto. No se puede usar el formato de JavaScript (claves sin comillas, etc.).
- Penrose: use solo `@preset set-theory` al principio y las sentencias permitidas (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- «El SVG generado contiene referencias no seguras», «El SVG generado supera el límite»: no se muestran los diagramas que hacen referencia a recursos externos ni los que son demasiado grandes. Reduzca el contenido o quite las referencias.

## Una imagen no se muestra

- La ruta de la imagen se indica como ruta relativa desde el documento. Las imágenes situadas fuera de la raíz de documentación no se muestran.
- El atributo `width` de `<img>` admite solo un número (`width="360"`).

## Los diagramas no se muestran en el sitio web exportado

Las bibliotecas de dibujo de TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob y Penrose se cargan en el momento de mostrar el contenido. Coloque también la carpeta `vendor/` junto con el sitio exportado.

## Temas relacionados

- [Escribir fórmulas](../03-editing/math.md)
- [Escribir diagramas y gráficos](../03-editing/diagrams.md)
- [Ajustar el tamaño de las imágenes](../03-editing/images.md)
