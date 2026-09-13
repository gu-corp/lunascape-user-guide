# 在 Web 上发布自己的文档

你可以将自己仓库中的文档通过 GitHub Pages 或任意静态托管服务发布为网站。发布方式有两种。本步骤面向能够 clone Lunascape Docs 仓库并使用 `npm` 的开发者。

## 方式 1：放置查看器的两个文件

只部署查看器本体（`index.html` 和 `lsdoc.js`），文档从 GitHub 加载。文档本身不包含在站点内，因此对非公开仓库也是安全的（阅读者通过 GitHub 登录）。

1. 在 Lunascape Docs 仓库中执行以下命令。

   ```sh
   npm run build:viewer
   ```

   `dist/viewer/` 中会生成 `index.html` 和 `lsdoc.js`。
2. 将这两个文件放入要发布的仓库的 `docs/` 中。
3. 启用 GitHub Pages。

要显示的文档根目录按以下顺序确定。

1. `index.html` 中的设置 `source`
2. 同一文件夹下 `lunascape-docs.json` 中记载的 `repository`
3. 根据 `*.github.io` 的 URL 和分支结构推断

## 方式 2：导出包含文档的静态站点

将查看器与文档文件一并导出，直接托管。

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

输出内容包括查看器整套文件、`docs/` 下的文档、清单文件 `lunascape-docs-manifest.json` 和 `.nojekyll`。将输出目录放到 S3 或 GitHub Pages 上即可发布。使用 GitHub Actions 自动发布的示例，请参阅仓库中的 `examples/workflows/publish-docs-pages.yml`。

> **注意**
>
> - **请勿将非公开仓库的文档导出后放到 GitHub Pages 上。** 除 Enterprise Cloud 以外的 GitHub Pages 任何人都可以浏览。如需限定公开，请使用方式 1，让阅读者通过 GitHub 登录。
> - 以 `file://` 直接打开 `index.html` 无法正常工作。这是因为浏览器禁止加载相邻文件和执行 ES 模块。在本地确认时，请使用 VS Code 版或 HTTP 服务器。
> - TikZ、Vega-Lite、Markmap、WaveDrom、Svgbob、Penrose 的绘图库在显示时加载。在导出的站点中，请将 `vendor/` 文件夹一并放置。

## 相关主题

- [Web 版能做什么](README.md)
- [浏览非公开仓库](private-repository.md)
