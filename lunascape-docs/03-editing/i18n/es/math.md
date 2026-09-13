# Escribir fórmulas

Las fórmulas se escriben con la notación de TeX y se representan en el dispositivo con KaTeX. No se usa la red.

## Notación

| Tipo | Delimitadores | Ejemplo |
|---|---|---|
| Fórmula en línea (dentro de una frase) | `$...$` o `\(...\)` | `La relación entre masa y energía se expresa como $E = mc^2$.` |
| Fórmula en bloque (en una línea propia) | `$$...$$` o `\[...\]` | Véase abajo |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- No hace falta dejar espacios antes ni después de los delimitadores. También se reconocen las fórmulas contiguas al texto japonés, como `値は$V=-H$である`.
- El signo `$` dentro de código en línea o de un bloque de código no se trata como fórmula: se muestra tal cual.
- Los textos con aspecto de importe, como `$5 and $10`, no se tratan como fórmulas.

## Editar

En la vista visual, las fórmulas se muestran ya representadas. Para modificar su contenido, pulse [Markdown] en la pantalla de edición y edite el código fuente. Al guardar desde la vista visual se conservan sin cambios el código TeX y la forma original de los delimitadores (`$` o `\(`).

> **Nota**
>
> - Por seguridad, KaTeX funciona con `trust: false` y tiene límites de tamaño (`maxSize: 50`) y de expansiones de macro (`maxExpand: 1000`). Las fórmulas que superen estos límites no se representan.
> - En documentos existentes, un `tikzpicture` escrito dentro de `$$...$$` o `\[...\]` se reconoce como diagrama de TikZ, no como fórmula.

## Temas relacionados

- [Escribir diagramas y gráficos](diagrams.md)
- [Los diagramas, las fórmulas o las imágenes no se muestran](../07-troubleshooting/rendering.md)
