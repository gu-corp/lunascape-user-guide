# 主要規格

## 執行環境

| 環境 | 需求 |
|---|---|
| VS Code 擴充功能 | VS Code 1.90 以上。需要寫入的功能必須在受信任的工作區中執行 |
| Web 瀏覽器版 | 較新版本的 Chrome、Edge、Safari、Firefox。瀏覽本機資料夾時，需使用支援資料夾選取（File System Access API）的瀏覽器 |
| Chromium 擴充功能 | Manifest V3。不要求主機權限 |

## 支援的文件

| 項目 | 內容 |
|---|---|
| 檔案 | `.md`、`.markdown`、`.mdx` |
| Markdown | GitHub Flavored Markdown（表格、工作清單、程式碼區塊、刪除線）、本機圖片、YAML front matter |
| MDX | 僅顯示允許的元件。不執行任意指令碼 |
| HTML | 以 DOMPurify 3.4.14 淨化後顯示 |

## 圖表與數學式

| 種類 | 語言名稱 | 備註 |
|---|---|---|
| 數學式 | `$...$`、`$$...$$`、`\(...\)`、`\[...\]` | KaTeX。`trust: false`、`maxSize: 50`、`maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | 僅限內嵌資料。不可使用外部 URL 與圖片標記 |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | 僅限嚴格的 JSON |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | 發行版本以摺疊方式顯示原始碼。上限為輸入 64 KiB、15 秒、SVG 2 MiB |
| Penrose（實驗性） | `penrose` | 僅限 `set-theory` 預設集 |

## 上限值

| 項目 | 數值 |
|---|---|
| 範本的展開結果 | 4 MiB |
| 翻譯的參考內容 | 預設 49,152 個字元，最多 1,048,576 個字元 |
| 批次翻譯單次的對象 | 1,000 份文件 |
| 圖片的自訂寬度 | 16〜4096px |

## 檔案

| 檔案 | 用途 | Git 管理 |
|---|---|---|
| `lunascape-docs.json` | 文件根目錄的設定 | 有 |
| `docs-lint.config.json` | 檢查規則的設定 | 有 |
| `.lunascape-docs/translation-freshness.json` | 翻譯新鮮度的紀錄（僅路徑、語言、雜湊值與日期時間） | 有 |
| VS Code 的設定與工作區狀態 | 個人的顯示設定、提供者的選擇、INDEX 的展開狀態 | 無 |

## 隨附的 Standard Pack

`builtin:gu-corp-software` — 設定檔：`base`、`web-application`、`api-service`、`regulated-financial-product`、`smart-contract`

## 相關項目

- [VS Code 設定一覽](settings.md)
- [安全性與儲存界線](security.md)
