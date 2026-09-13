# 图、公式或图像不显示

## TikZ 图显示为折叠的源代码

- 发布版扩展中未附带 TikZ 的渲染引擎。这是正常的显示结果。
- 用于开发和评估时，可在受信任的工作区根目录下安装 `node-tikzjax` 1.0.5，并将设置 `lunascapeDocEditor.tikz.runtime` 设为 `workspace`，即可渲染。
- Web 浏览器版不渲染 TikZ。

## 公式显示为普通文字

- 请确认分隔符。行内公式为 `$...$` 或 `\(...\)`，独立公式为 `$$...$$` 或 `\[...\]`。
- 行内代码和代码块中的 `$` 不会成为公式。
- 类似 `$5 and $10` 这样的金额写法不会被当作公式。
- 非常大的公式，或宏展开过多的公式，超过上限（`maxSize: 50`、`maxExpand: 1000`）时不会渲染。请拆分后再写。

## 图提示"无法渲染"

- Mermaid、Vega-Lite、WaveDrom 等给出的错误信息会指出语法问题所在。请在编辑界面的 [Markdown] 中确认源代码。
- Vega-Lite：数据请嵌入 `data.values` 或 `datasets` 中。无法使用外部 URL 的数据和图像标记。
- WaveDrom：请以严格的 JSON 书写。无法使用 JavaScript 形式（如不加引号的键名等）。
- Penrose：只能使用开头的 `@preset set-theory` 以及允许的语句（`Set`、`Subset`、`Disjoint`、`Intersecting`、`AutoLabel All`）。
- "生成的 SVG 中含有不安全的引用""生成的 SVG 超过了上限"：包含外部资源引用的图，或过大的图不会显示。请减少内容，或去掉这些引用。

## 图像不显示

- 图像路径请使用相对于文档的相对路径指定。位于文档根目录之外的图像不会显示。
- `<img>` 的 `width` 只能指定数值（`width="360"`）。

## 导出的网站上图不显示

TikZ、Vega-Lite、Markmap、WaveDrom、Svgbob、Penrose 的渲染库是在显示时加载的。请将 `vendor/` 文件夹一并放到导出的网站中。

## 相关主题

- [书写公式](../03-editing/math.md)
- [绘制图与图表](../03-editing/diagrams.md)
- [调整图像尺寸](../03-editing/images.md)
