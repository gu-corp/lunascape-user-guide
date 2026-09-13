# Web 版可以做什麼

Web 瀏覽器版的 Lunascape Docs 公開於 <https://docs.lunascape.org/>。不需安裝任何程式，就能像瀏覽網站一樣閱讀 GitHub 上的文件。

## 可以做什麼

| 功能 | 內容 |
|---|---|
| 瀏覽公開存放庫 | 不必登入，即可開啟 GitHub 公開存放庫中的文件 |
| 瀏覽非公開存放庫 | 以 GitHub 登入後，可開啟自己具有讀取權限的存放庫 |
| 瀏覽本機資料夾 | 在 [開啟文件] 中選擇 [開啟本機資料夾中的文件]，開啟裝置內的資料夾（僅限支援的瀏覽器） |
| 閱讀功能 | INDEX、連結、瀏覽記錄、篩選、本頁內容、切換語言、切換主題。與 VS Code 版相同 |
| 圖表與數學式 | Mermaid、Vega-Lite、Markmap、WaveDrom、Svgbob、Penrose、KaTeX 數學式 |
| 草稿 | 編輯文件，並將變更保存為裝置內的草稿。不會寫入存放庫 |
| 頁面直接連結 | 以 URL 指定存放庫與頁面，即可直接開啟特定頁面 |

## 與 VS Code 版的差異

- 文件檢查、從範本建立、產生翻譯草案、從 INDEX 整理等功能，Web 版沒有提供。
- 不會繪製 TikZ 圖。
- 編輯內容不會寫入存放庫，而是成為裝置內的草稿。將草稿以 Pull Request 送出的「發布請求」雖已實作，但在公開檢視器上並未啟用。若要反映到存放庫，請使用 VS Code 版或在本機複本中編輯。

## 相關項目

- [開啟 GitHub 的存放庫](open-repository.md)
- [瀏覽非公開存放庫](private-repository.md)
- [儲存草稿](drafts.md)
