# 文档根目录与文件约定

Lunascape Docs 查找文档并组建 INDEX 时所遵循的规则。文件系统本身就是正本，因此不需要台账或构建配置。

## 文档根目录

- 最近的 `docs` 文件夹，或放置了 `lunascape-docs.json` 的文件夹，会成为文档根目录。
- 只要放置 `lunascape-docs.json`，文件夹就不必命名为 `docs`。
- 打开不属于任何文档根目录的 Markdown 时，会把该文件夹作为临时的文档根目录来显示。

## 会显示在 INDEX 中的文件

- 显示 `.md`、`.markdown`、`.mdx` 文件。即使没有 front matter 或导航信息，新文件也一定会显示。
- 以 `.` 开头的文件夹、`node_modules`，以及在 `ignoredDirectories`（默认为 `99-archive`）中指定的文件夹不会显示。
- `i18n/` 之下的内容视为翻译版本，不会在 INDEX 中单独显示。

## 文件夹封面

- 有正文的 `README.md`（若无则为 `index.md`）会成为该文件夹的封面。在 INDEX 中点击文件夹名即可打开封面。
- 只有 front matter、没有正文的 `README.md` 会被视为“仅配置的描述符”，不会作为页面显示。当只想为文件夹设置标题或排序时使用它。
- 当 `README.md` 与 `index.md` 同时存在时，优先使用 `README.md`。

## 默认语言与翻译版本

- 默认语言的文档（正本文档）保留在原处。
- 翻译版本放在与正本相同文件夹下的 `i18n/<语言>/` 中，使用相同的文件名。在 `i18n/` 之下重建文件夹结构的做法不会被识别。
- 解析来源只有这一处。放在其他位置的同名翻译会成为孤立文件，不会被当作任何文档的翻译。

```text
docs/
  lunascape-docs.json
  README.md                  ← 文档根目录的封面（起始页）
  i18n/en/README.md          ← 其英语版本
  01-product/
    README.md                ← 文件夹的封面
    requirements.md
    i18n/en/README.md        ← 上面两个文档的英语版本
    i18n/en/requirements.md
  99-archive/                ← 默认从 INDEX 中排除
```

## 关于 `_meta.json`

Nextra 的 `_meta.json` 不用于导航。既不修改也不删除现有文件。将来只会通过明确的导入/导出功能来处理它们。

## 相关主题

- [设置导航信息](navigation-metadata.md)
- [项目配置](project-configuration.md)
- [切换文档根目录](../02-reading/roots.md)
