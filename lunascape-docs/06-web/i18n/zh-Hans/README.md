# Web 版的功能

Lunascape Docs 的 Web 浏览器版发布在 <https://docs.lunascape.org/>。无需安装，即可像浏览网站一样阅读 GitHub 上的文档。

## 可用功能

| 功能 | 内容 |
|---|---|
| 浏览公开仓库 | 无需登录即可打开 GitHub 公开仓库中的文档 |
| 浏览私有仓库 | 使用 GitHub 登录后，可以打开自己拥有读取权限的仓库 |
| 浏览本地文件夹 | 通过 [打开文档] 中的 [打开本地文件夹中的文档]，打开设备中的文件夹（仅限支持的浏览器） |
| 阅读功能 | INDEX、链接、历史记录、筛选、本页目录、语言切换、主题切换。与 VS Code 版相同 |
| 图与公式 | Mermaid、Vega-Lite、Markmap、WaveDrom、Svgbob、Penrose、KaTeX 公式 |
| 草稿 | 编辑文档，并将修改作为草稿保留在设备中。不会写入仓库 |
| 页面直达链接 | 可在 URL 中指定仓库和页面，直接打开特定页面 |

## 与 VS Code 版的区别

- Web 版没有文档检查、从模板创建、生成翻译方案以及从 INDEX 整理这些功能。
- 不绘制 TikZ 图。
- 编辑内容不会写入仓库，而是成为设备中的草稿。将草稿作为 Pull Request 发送的"发布请求"虽已实现，但在公开查看器中未启用。若要反映到仓库中，请使用 VS Code 版或在本地克隆中编辑。

## 相关项目

- [打开 GitHub 仓库](open-repository.md)
- [浏览私有仓库](private-repository.md)
- [保存草稿](drafts.md)
