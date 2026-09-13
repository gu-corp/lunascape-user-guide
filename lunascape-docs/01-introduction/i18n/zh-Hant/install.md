# 安裝擴充功能

VS Code 擴充功能「Lunascape Docs Pro」以 VSIX 檔案形式發佈，完全免費。「Pro」代表這是具備將工作交給 AI 及自我更新功能的版本。

## 執行環境

- VS Code 1.90 以上
- 建立文件、從 INDEX 整理、儲存檢查設定、翻譯等需要寫入的功能，只能在 VS Code 中標記為「受信任」的工作區使用。

## 安裝

1. 取得 VSIX 檔案。此連結永遠指向最新版本。

   [下載 lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. 開啟 VS Code 的擴充功能檢視（`⇧⌘X` / `Ctrl+Shift+X`）。
3. 從右上角的 `…` 選單中選擇 [從 VSIX 安裝...]，並指定取得的檔案。

### 使用指令安裝

也可以在終端機中用一行指令完成。它會連續執行取得與安裝。

macOS / Linux：

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows（PowerShell）：

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **注意**
> 找不到 `code` 時，請從命令選擇區（`⇧⌘P` / `Ctrl+Shift+P`）執行 [Shell 命令：在 PATH 中安裝 'code' 命令]。

## 更新

當有新版本發佈時，擴充功能會自行取得並安裝。VS Code 提示重新載入視窗後，即會於此時切換。設定與文件將原樣保留。

檢查每天進行一次。若想立即確認，請從命令選擇區（`⇧⌘P` / `Ctrl+Shift+P`）執行 [Lunascape Docs：檢查更新]。

行為可透過設定 `lunascapeDocEditor.update.check` 變更。

| 設定 | 行為 |
|---|---|
| 有新版本發佈時即安裝 | 預設 |
| 通知我，是否安裝由我每次決定 | 出現通知，只有在按下 [更新] 時才會切換 |
| 不檢查 | 不做任何事 |

### 無法更新時

若出現「無法取得更新：No Servers」，表示安裝的版本為 0.22.18 或更早。該版本的更新功能在取得之後的下一步必定失敗，因此無法自行更新為新版本。請依上述步驟手動重新安裝一次。之後便會自行更新。

## 確認版本

在擴充功能檢視中開啟「Lunascape Docs Pro」，即會顯示已安裝的版本。回報問題時會需要用到。

## 關聯項目

- [第一次建立文件](first-documents.md)
- [回報問題](../07-troubleshooting/report.md)
