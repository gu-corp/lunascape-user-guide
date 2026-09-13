# 圖表、數學式或圖片無法顯示

## TikZ 圖表顯示為折疊的原始碼

- 發行版的擴充功能未內含 TikZ 的繪製引擎。這是正常的顯示結果。
- 若用於開發與評估，請在受信任的工作區根目錄下安裝 `node-tikzjax` 1.0.5，並將設定 `lunascapeDocEditor.tikz.runtime` 設為 `workspace`，即可繪製。
- Web 瀏覽器版不會繪製 TikZ。

## 數學式顯示為原始文字

- 請確認分隔符號。行內為 `$...$` 或 `\(...\)`，獨立數學式為 `$$...$$` 或 `\[...\]`。
- 行內程式碼或程式碼區塊中的 `$` 不會成為數學式。
- 類似 `$5 and $10` 的金額寫法不會視為數學式。
- 非常龐大的數學式，或巨集展開次數過多的數學式，超過上限（`maxSize: 50`、`maxExpand: 1000`）時不會繪製。請分割內容。

## 圖表顯示「無法繪製」

- Mermaid、Vega-Lite、WaveDrom 等的錯誤訊息會指出語法問題所在。請在編輯畫面的 [Markdown] 確認原始碼。
- Vega-Lite：資料請內嵌於 `data.values` 或 `datasets`。無法使用外部 URL 的資料與圖片標記。
- WaveDrom：請以嚴格的 JSON 撰寫。無法使用 JavaScript 形式（例如未加引號的索引鍵）。
- Penrose：只能使用開頭的 `@preset set-theory`，以及允許的陳述（`Set`、`Subset`、`Disjoint`、`Intersecting`、`AutoLabel All`）。
- 「產生的 SVG 含有不安全的參照」「產生的 SVG 超過上限」：含有外部資源參照的圖表，或過大的圖表不會顯示。請減少內容，或移除參照。

## 圖片無法顯示

- 圖片路徑請以文件的相對路徑指定。文件根目錄之外的圖片不會顯示。
- `<img>` 的 `width` 只能指定數值（`width="360"`）。

## 匯出的網站上圖表無法顯示

TikZ、Vega-Lite、Markmap、WaveDrom、Svgbob、Penrose 的繪製程式庫會在顯示時載入。請將 `vendor/` 資料夾一併配置到匯出的網站中。

## 相關項目

- [撰寫數學式](../03-editing/math.md)
- [撰寫圖表與圖形](../03-editing/diagrams.md)
- [調整圖片大小](../03-editing/images.md)
