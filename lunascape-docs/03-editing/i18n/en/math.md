# Writing math

Math is written in TeX notation and rendered on your device with KaTeX. No network is used.

## Notation

| Kind | Delimiters | Example |
|---|---|---|
| Inline math (within a sentence) | `$...$` or `\(...\)` | `Mass and energy are related by $E = mc^2$.` |
| Display math (on its own line) | `$$...$$` or `\[...\]` | See below |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- No whitespace is needed around the delimiters. Math directly adjacent to Japanese text, such as `値は$V=-H$である`, is recognized.
- A `$` inside inline code or a code block is kept as literal text.
- Currency-like text such as `$5 and $10` is not treated as math.

## Edit

In the visual view, math is shown rendered. To change it, press [Markdown] in the editor and edit the source. Saving from the visual view keeps the TeX source and the original delimiter form (`$` or `\(`) unchanged.

> **Note**
>
> - For safety KaTeX runs with `trust: false` and limits size (`maxSize: 50`) and macro expansion (`maxExpand: 1000`). Math beyond these limits is not rendered.
> - A `tikzpicture` written inside `$$...$$` or `\[...\]` in an existing document is recognized as a TikZ figure, not as math.

## Related topics

- [Writing diagrams and charts](diagrams.md)
- [Diagrams, math or images do not render](../07-troubleshooting/rendering.md)
