# 從 AI 使用

擴充功能會向 VS Code 註冊唯讀的 Language Model Tool `lunascape_getDocsSpecification`。當相容的 VS Code 代理程式被問及 Lunascape Docs 的功能、設定或文件慣例時，可透過這個工具取得本說明的內容（一般規格）。

## 使用方式

在 VS Code 的聊天中加上 `#lunascapeDocs` 提問，或直接詢問 Lunascape Docs 的設定或文件結構。

```text
#lunascapeDocs 要在 lunascape-docs.json 中啟用英文翻譯該怎麼做？
```

## 工具的引數

| 引數 | 內容 |
|---|---|
| `topic` | 要取得的章節。`all`、`usage`（基本操作）、`structure`（文件根目錄與檔案慣例）、`editing`（編輯文件）、`configuration`（專案設定）、`security`（安全性與儲存邊界）、`ai`（從 AI 使用） |
| `locale` | 說明的語言（`ja`、`en` 等，隨附說明的語言標籤）。省略時會使用 VS Code 的顯示語言，若無則回傳日文的說明 |

> **請注意**
>
> - 工具不會將文件的內文傳送到外部。
> - 工具不會回傳工作區名稱或本機路徑。
> - 工具不會變更檔案。
> - 即使沒有 `AGENTS.md`，也能從相容的 VS Code 代理程式使用。對於不使用擴充功能工具 API 的其他 AI 用戶端，則不會自動共用。

## 相關項目

- [顯示說明](../02-reading/help.md)
- [安全性與儲存邊界](security.md)
