# 安装扩展

VS Code 扩展“Lunascape Docs Pro”以 VSIX 文件的形式发布，免费提供。“Pro”表示这是具备将工作交给 AI 以及自我更新功能的版本。

## 运行环境

- VS Code 1.90 或更高版本
- 创建文档、从 INDEX 整理、保存检查设置、翻译等涉及写入的功能，只能在你已在 VS Code 中标记为“受信任”的工作区中使用。

## 安装

1. 获取 VSIX 文件。此链接始终指向最新版本。

   [下载 lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. 打开 VS Code 的扩展视图（`⇧⌘X` / `Ctrl+Shift+X`）。
3. 从右上角的 `…` 菜单中选择 [从 VSIX 安装...]，并指定你获取的文件。

### 用命令安装

也可以在终端中用一行命令完成。它会连续执行获取和安装。

macOS / Linux：

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows（PowerShell）：

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **注意**
> 如果找不到 `code`，请从命令面板（`⇧⌘P` / `Ctrl+Shift+P`）运行 [Shell 命令: 在 PATH 中安装 'code' 命令]。

## 更新

有新版本发布时，扩展会自行获取并安装。当 VS Code 提示重新加载窗口时，即在此时切换。你的设置和文档会原样保留。

每天检查一次。如果想立即确认，请从命令面板（`⇧⌘P` / `Ctrl+Shift+P`）运行 [Lunascape Docs: 检查更新]。

其行为可通过设置 `lunascapeDocEditor.update.check` 更改。

| 设置 | 行为 |
|---|---|
| 有新版本发布时即安装 | 默认 |
| 通知我，每次由我决定是否安装 | 出现通知，只有在按下 [更新] 时才会切换 |
| 不检查 | 不做任何操作 |

### 无法更新时

如果出现“更新を取得できませんでした: No Servers”，说明已安装的版本为 0.22.18 或更早。该版本的更新功能在获取之后的一步必然失败，因此无法自行更新到新版本。请按上面的步骤手动重装一次。之后即可自行更新。

## 确认版本

在扩展视图中打开“Lunascape Docs Pro”，即可看到已安装的版本。报告问题时需要用到它。

## 相关主题

- [首次创建文档](first-documents.md)
- [报告问题](../07-troubleshooting/report.md)
