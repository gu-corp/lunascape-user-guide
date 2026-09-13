# 命令一览

在命令面板（`⇧⌘P` / `Ctrl+Shift+P`）中输入“Lunascape Docs”，即可运行以下命令。

| 命令 | 作用 |
|---|---|
| Lunascape Docs: 打开规格书查看器 | 在查看器中打开最近的文档根目录。阅读、编辑、检查和翻译都在此界面中进行 |
| Lunascape Docs: 在规格书查看器中打开 | 在查看器中显示编辑器里打开的 Markdown 文件 |
| Lunascape Docs: 从模板创建文档 | 为没有文档文件夹的项目创建最初的一套文档 |
| Lunascape Docs: 验证文档根目录 | 用 docs-lint 检查整个文档根目录，并在文档工具和“问题”面板中显示结果 |
| Lunascape Docs: 打开帮助 | 打开本帮助指南 |

## 从资源管理器操作

在资源管理器中右键单击 `.md`、`.markdown` 或 `.mdx` 文件，可以选择 [Lunascape Docs: 在规格书查看器中打开]。

> **提示**
>
> 若要在正常打开 Markdown 文件时也用 Lunascape Docs 显示，请在工作区设置中添加编辑器关联。
>
> ```json
> {
>   "workbench.editorAssociations": {
>     "*.md": "lunascapeDocEditor.markdownPortal"
>   }
> }
> ```

## 演练

通过 VS Code 的 [帮助] 菜单 →“欢迎使用”中的演练“开始使用 Lunascape Docs”，可以按顺序尝试最初的操作。

## 相关主题

- [基本操作](../02-reading/README.md)
- [键盘操作一览](../08-reference/keyboard.md)
