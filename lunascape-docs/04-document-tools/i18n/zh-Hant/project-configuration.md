# 專案設定

文件根目錄下的 `lunascape-docs.json` 是團隊共用的文件根目錄設定，以 Git 管理。

## 建立與編輯設定檔

- 按下工具列的 [文件工具] → [檢查] 分頁 → [規則的提供來源與文件設定] → [編輯文件設定]，即可在 VS Code 中開啟。若檔案不存在，此時會建立初始檔案。
- 檔名 `lunascape-docs.json` 會自動關聯內附的 JSON Schema，顯示輸入補完與各項目的說明。無需撰寫 `$schema`。

## 設定範例

```json
{
  "id": "product-docs",
  "title": "產品文件",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## 項目說明

| 項目 | 內容 | 預設 |
|---|---|---|
| `id` | 用來儲存各使用者顯示設定的鍵。當你想在移動資料夾後仍沿用設定時，指定一個固定的 ID | 資料夾的路徑 |
| `title` | 顯示於工具列最左端與文件根目錄一覽的名稱。切換顯示語言時不會改變 | 根目錄 README/index 的標題，若無則為資料夾名稱 |
| `indexTitle` | INDEX 的標題 | `INDEX` |
| `startPage` | 最先開啟的文件（相對於文件根目錄的路徑） | `README.md` |
| `appearance` | 配色。`light`（永遠明亮）或 `auto`（跟隨 VS Code 主題） | `light` |
| `defaultLocale` | 預設語言（正本的語言）。以 BCP 47 語言標籤（`ja`、`en`、`zh-Hant` 等）指定，作為翻譯來源 | 未設定（依內文推定後顯示） |
| `fallbackLocale` | 對於閱覽環境語言與任何支援語言皆不相符的讀者，最先呈現的語言。指定 `locales` 中包含的語言 | 未設定（使用 `defaultLocale`） |
| `locales` | 支援語言的清單，須包含 `defaultLocale`。會成為語言選單與翻譯目標的候選 | 僅 `defaultLocale` |
| `ignoredDirectories` | 從 INDEX、搜尋與檢查中排除的資料夾名稱。指定後會取代預設值 | `["99-archive"]` |
| `tree` | INDEX 顯示的預設值。使用者可在顯示設定中覆寫 | 如上方範例 |
| `editor.defaultMode` | 使用者尚未切換時的編輯顯示。`visual` 或 `source` | `visual` |
| `editor.showEditButton` | 是否顯示內文右下角的 [編輯] | `true` |
| `documentStandards.pack` | 文件檢查與範本所使用的 Standard Pack。`builtin:<名稱>`，或相對於文件根目錄的路徑 | 無 |
| `documentStandards.profile` | Pack 定義的設定檔名稱 | 無 |
| `translation.enabled` | 啟用翻譯稿的建立與批次翻譯 | `true` |
| `translation.contextFiles` | 翻譯時作為用語與文體參考傳遞的正本 Markdown（相對於文件根目錄的路徑） | `[]` |
| `translation.maxContextCharacters` | 參考文件的合計字數上限（最大 1048576） | `49152` |
| `description` | 文件集合的一行說明。顯示於儲存庫首頁的卡片。與 `title` 相同，可寫成字串或依語言分列的物件 | 無 |

## 告知文件在儲存庫的何處

放在儲存庫直下的 `lunascape-docs.json`，可以不寫該資料夾的設定，而寫**儲存庫的地圖**。只要寫入下列三個項目之一，它就會成為地圖，該資料夾本身就不會成為文件根目錄。

| 項目 | 內容 | 預設 |
|---|---|---|
| `defaultFolder` | 文件位於哪個資料夾（相對於直下的路徑）。所指向的位置不需要設定檔 | 無（使用 `docs`） |
| `roots` | 當擁有多個文件集合時的一覽（相對於直下的路徑，依顯示順序）。此時直下即為首頁 | 無 |
| `excludes` | 從文件根目錄探索中排除的資料夾（相對於直下的路徑）。會加在 `node_modules` 等預設排除之上 | `[]` |
| `home.cards` | 是否在首頁 README 下方顯示文件集合的卡片。當你自行在 README 撰寫連結時設為 `false` | `true` |

文件根目錄依下列順序決定，由上而下取最先找到者。

1. 以設定或指令指定資料夾時，該資料夾
2. 直下 `lunascape-docs.json` 的 `defaultFolder` 或 `roots` 所指向的位置
3. 有 `lunascape-docs.json` 的資料夾（若同一共通母資料夾下有兩個以上，則該母資料夾為首頁）
4. `docs` 資料夾（`lunascapeDocEditor.rootDirectoryNames`）
5. 儲存庫直下本身

> **提示**
>
> 若什麼都不寫，第 4 項便會生效，因此只有一個 `docs/` 的普通儲存庫維持一如既往。只有想把資料夾名稱設為 `manual` 時，才需要撰寫 `defaultFolder`。

### 地圖範例

```json
{
  "title": "Lunascape 說明",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## 設定的優先順序

與顯示相關的項目，依下列順序優先。

1. 使用者的顯示設定（[顯示設定] 面板）
2. VS Code 的設定（`lunascapeDocEditor.*`）
3. `lunascape-docs.json`
4. 產品的預設值

唯獨語言（`defaultLocale`、`fallbackLocale`、`locales`）為例外，以 `lunascape-docs.json` 為正本。無法以 VS Code 的個人設定覆寫專案的語言。

> **注意**
>
> 也可以在 `docs-lint.config.json` 中以 `standard` 指定 Standard Pack。兩者皆有時，以 `docs-lint.config.json` 為優先。

## 關聯項目

- [變更檢查規則](rules.md)
- [變更顯示設定](../02-reading/display-settings.md)
- [VS Code 設定一覽](../08-reference/settings.md)
