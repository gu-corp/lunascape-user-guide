# VS Code 設定一覽

在 VS Code 的設定（`⌘,` / `Ctrl+,`）中搜尋「Lunascape Docs」，即可變更下列項目。這些都是各使用者自己的設定，不會儲存到專案的文件中。

## 文件根目錄

| 設定 | 值 | 預設 | 作用 |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` 會自動選擇離所開啟 Markdown 最近的文件根目錄，若不屬於任何根目錄，則暫時開啟其上層資料夾。`fixed` 則一律開啟 `root` 所指的文件根目錄 |
| `lunascapeDocEditor.rootDirectoryNames` | 字串陣列 | `["docs"]` | 在 `auto` 模式下自動探索為文件根目錄的資料夾名稱。含有 `lunascape-docs.json` 的資料夾不論名稱為何都會被探索到。當存放庫根目錄的 `lunascape-docs.json` 中有 `defaultFolder` 或 `roots` 時，以其為優先 |
| `lunascapeDocEditor.root` | 路徑 | `docs` | 在 `fixed` 模式或從命令開啟時，相對於工作區的文件根目錄 |
| `lunascapeDocEditor.startPage` | 路徑 | `README.md` | 相對於文件根目錄的起始頁 |
| `lunascapeDocEditor.title` | 字串 | `Lunascape Docs` | 覆寫文件索引標籤的標題。不會影響文件根目錄的選擇名稱 |
| `lunascapeDocEditor.ignoredDirectories` | 字串陣列 | `["99-archive"]` | 要從 INDEX 排除的資料夾名稱 |

## 顯示

| 設定 | 值 | 預設 | 作用 |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` 為白色背景，`auto` 則跟隨 VS Code 的配色 |
| `lunascapeDocEditor.locale` | 語言標籤 | 無 | 可用時優先顯示的個人文件語言。不會變更專案的正本語言 |
| `lunascapeDocEditor.documentMetadata.compact` | 布林值 | `true` | 將 H1 之後的文件管理表摺疊成「文件資訊」一列 |
| `lunascapeDocEditor.tree.showFileNames` | 布林值 | `false` | 在 INDEX 中以檔案名稱取代文件名稱顯示 |
| `lunascapeDocEditor.tree.showDocumentIcons` | 布林值 | `false` | 在 INDEX 中顯示文件圖示 |
| `lunascapeDocEditor.tree.showFolderIcons` | 布林值 | `false` | 在 INDEX 中顯示資料夾圖示 |
| `lunascapeDocEditor.tree.showItemCounts` | 布林值 | `false` | 在 INDEX 中顯示各資料夾底下的項目數 |
| `lunascapeDocEditor.tree.showGuides` | 布林值 | `true` | 在 INDEX 中顯示階層的輔助線 |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | INDEX 的行距 |
| `lunascapeDocEditor.tree.autoHideSingleItem` | 布林值 | `true` | 當文件只有 1 件時，僅第一次關閉 INDEX |

## 編輯

| 設定 | 值 | 預設 | 作用 |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | 尚未切換時所使用的編輯畫面。最後使用過的畫面優先 |
| `lunascapeDocEditor.editor.showEditButton` | 布林值 | `true` | 顯示內文右下角的 [編輯] |

## 圖表

| 設定 | 值 | 預設 | 作用 |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | TikZ 的繪製執行環境。`bundled` 為隨附的已核可執行環境（目前的發行版並未隨附），`workspace` 為受信任的工作區根目錄下的 `node-tikzjax` 1.0.5（僅供開發與評估使用），`disabled` 則不繪製 |

## 已不建議使用的設定

| 設定 | 改用 |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `lunascape-docs.json` 的 `defaultLocale` |
| `lunascapeDocEditor.locales` | `lunascape-docs.json` 的 `locales` |

無法以個人設定覆寫專案的語言。

## 相關項目

- [變更顯示設定](../02-reading/display-settings.md)
- [專案設定](../04-document-tools/project-configuration.md)
