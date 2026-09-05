# Diagrams, math or images do not render

## A TikZ figure shows as collapsed source

- The distributed extension does not bundle a TikZ rendering engine. This is the expected display.
- For development and evaluation, install `node-tikzjax` 1.0.5 at the root of a trusted workspace and set `lunascapeDocEditor.tikz.runtime` to `workspace`.
- The Web viewer does not render TikZ.

## Math is shown as plain text

- Check the delimiters: `$...$` or `\(...\)` inline, `$$...$$` or `\[...\]` for display math.
- A `$` inside inline code or a code block is never math.
- Currency-like text such as `$5 and $10` is not treated as math.
- Very large math or heavy macro expansion beyond the limits (`maxSize: 50`, `maxExpand: 1000`) is not rendered. Split it up.

## A diagram says it cannot be rendered

- The error message from Mermaid, Vega-Lite, WaveDrom and others points at the syntax problem. Check the source in the editor with [Markdown].
- Vega-Lite: embed data in `data.values` or `datasets`. External data URLs and image marks cannot be used.
- WaveDrom: write strict JSON. The JavaScript form (unquoted keys and so on) cannot be used.
- Penrose: use only `@preset set-theory` at the top and the allowed statements (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- "生成SVGに安全でない参照があります" (The generated SVG contains unsafe references) / "生成されたSVGが上限を超えています" (The generated SVG exceeds the limit): diagrams that reference external resources, or that are too large, are not shown. Reduce the content or remove the references.

## An image is not shown

- Image paths are relative to the document. Images outside the documentation root are not shown.
- The `width` of an `<img>` takes a number only (`width="360"`).

## Diagrams are missing on an exported website

The rendering libraries for TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob and Penrose are loaded on demand. Deploy the `vendor/` folder together with the exported site.

## Related topics

- [Writing math](../03-editing/math.md)
- [Writing diagrams and charts](../03-editing/diagrams.md)
- [Sizing images](../03-editing/images.md)
