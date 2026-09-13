# 切换文档根目录

文档根目录是一组文档的最上层文件夹。INDEX、筛选、检查和翻译均以文档根目录为单位工作。

## 文档根目录的查找方式

Lunascape Docs 从打开的 Markdown 文件向上逐层查找父文件夹，并将最先符合以下任一条件的文件夹作为文档根目录。

- 含有 `lunascape-docs.json` 的文件夹（文件夹名称不限）
- 名为 `docs` 的文件夹（可通过设置 `lunascapeDocEditor.rootDirectoryNames` 添加名称）

执行"Lunascape Docs: 打开规格书查看器"时，将打开设置 `lunascapeDocEditor.root`（默认为 `docs`）指定的文档根目录。

## 切换到其他文档根目录

当工作区中有多个文档根目录时，工具栏最左端的文档根目录名称会变为下拉菜单。

1. 按工具栏最左端的文档根目录名称。
2. 从列表中选择文档根目录。
   所选文档根目录的起始页将显示出来，INDEX 随之切换。

> **提示**
>
> 列表中显示的名称按以下顺序确定。切换界面语言也不会改变。
>
> 1. `lunascape-docs.json` 的 `title`
> 2. 根目录 `README.md` 的 `navigation.title`，没有时使用其 H1
> 3. 根目录 `index.md` 的 `navigation.title`，没有时使用其 H1
> 4. 文件夹名称（对于标准的 `docs` 文件夹，使用其父文件夹名称）

## 打开不属于文档根目录的 Markdown

打开不包含在文档根目录中的 Markdown 文件时，将该文件所在的文件夹作为临时文档根目录显示。INDEX 中会列出同一文件夹及其下方的 Markdown 文件。

- 按工具栏的 [上级文件夹]，可将显示范围扩大到工作区内的父文件夹。
- 在此显示方式下，无法使用项目的语言设置和批量翻译。在该文件夹中放入 `lunascape-docs.json` 使其成为文档根目录后即可使用。

## 始终打开固定的文档根目录

将设置 `lunascapeDocEditor.rootMode` 设为 `fixed` 后，无论打开哪个 Markdown，都始终打开 `lunascapeDocEditor.root` 指定的文档根目录。

## 相关主题

- [文档根目录与文件约定](../04-document-tools/structure.md)
- [项目设置](../04-document-tools/project-configuration.md)
- [VS Code 设置一览](../08-reference/settings.md)
