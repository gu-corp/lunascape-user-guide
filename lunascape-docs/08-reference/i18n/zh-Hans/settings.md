# VS Code 设置一览

在 VS Code 的设置（`⌘,` / `Ctrl+,`）中搜索"Lunascape Docs"，即可更改以下项目。这些都是每位用户的个人设置，不会保存到项目的文档中。

## 文档根目录

| 设置 | 值 | 默认 | 作用 |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` 会自动选择离所打开的 Markdown 最近的文档根目录；若不属于任何根目录，则临时打开其父文件夹。`fixed` 始终打开 `root` 指定的文档根目录 |
| `lunascapeDocEditor.rootDirectoryNames` | 字符串数组 | `["docs"]` | 在 `auto` 模式下作为文档根目录自动发现的文件夹名。含有 `lunascape-docs.json` 的文件夹无论名称如何都会被发现。当仓库根目录下的 `lunascape-docs.json` 中有 `defaultFolder` 或 `roots` 时，以其为准 |
| `lunascapeDocEditor.root` | 路径 | `docs` | `fixed` 模式下，或通过命令打开时所用的、相对于工作区的文档根目录 |
| `lunascapeDocEditor.startPage` | 路径 | `README.md` | 相对于文档根目录的起始页 |
| `lunascapeDocEditor.title` | 字符串 | `Lunascape Docs` | 覆盖文档标签页的标题。不影响文档根目录的选择名称 |
| `lunascapeDocEditor.ignoredDirectories` | 字符串数组 | `["99-archive"]` | 从 INDEX 中排除的文件夹名 |

## 显示

| 设置 | 值 | 默认 | 作用 |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` 为白色背景，`auto` 跟随 VS Code 的配色 |
| `lunascapeDocEditor.locale` | 语言标签 | 无 | 可用时优先显示的个人文档语言。不会更改项目的正本语言 |
| `lunascapeDocEditor.documentMetadata.compact` | 布尔值 | `true` | 将 H1 之后的文档管理表折叠为"文档信息"一行 |
| `lunascapeDocEditor.tree.showFileNames` | 布尔值 | `false` | 在 INDEX 中显示文件名而非文档名 |
| `lunascapeDocEditor.tree.showDocumentIcons` | 布尔值 | `false` | 在 INDEX 中显示文档图标 |
| `lunascapeDocEditor.tree.showFolderIcons` | 布尔值 | `false` | 在 INDEX 中显示文件夹图标 |
| `lunascapeDocEditor.tree.showItemCounts` | 布尔值 | `false` | 在 INDEX 中显示各文件夹下一级的项目数 |
| `lunascapeDocEditor.tree.showGuides` | 布尔值 | `true` | 在 INDEX 中显示层级的引导线 |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | INDEX 的行间距 |
| `lunascapeDocEditor.tree.autoHideSingleItem` | 布尔值 | `true` | 只有一个文档时，仅首次关闭 INDEX |

## 编辑

| 设置 | 值 | 默认 | 作用 |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | 尚未切换时使用的编辑视图。上次使用的视图优先 |
| `lunascapeDocEditor.editor.showEditButton` | 布尔值 | `true` | 在正文右下角显示 [编辑] |

## 图

| 设置 | 值 | 默认 | 作用 |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | TikZ 的绘制运行时。`bundled` 为随附的已审核运行时（当前发行版未随附），`workspace` 为受信任的工作区根目录下的 `node-tikzjax` 1.0.5（仅供开发与评估），`disabled` 则不绘制 |

## 已弃用的设置

| 设置 | 改用 |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `lunascape-docs.json` 的 `defaultLocale` |
| `lunascapeDocEditor.locales` | `lunascape-docs.json` 的 `locales` |

个人设置无法覆盖项目的语言。

## 相关主题

- [更改显示设置](../02-reading/display-settings.md)
- [项目配置](../04-document-tools/project-configuration.md)
