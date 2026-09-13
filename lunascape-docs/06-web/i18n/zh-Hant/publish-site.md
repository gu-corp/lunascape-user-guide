# 在網站上發布自己的文件

您可以將自己存放庫中的文件，透過 GitHub Pages 或任何靜態主機服務發布為網站。發布方式有兩種。以下步驟適用於能夠 clone Lunascape Docs 存放庫並使用 `npm` 的開發者。

## 方法 1：放置檢視器的兩個檔案

只部署檢視器本體（`index.html` 與 `lsdoc.js`），文件則從 GitHub 載入。文件本身不包含在網站中，因此非公開存放庫也很安全（閱讀者以 GitHub 登入）。

1. 在 Lunascape Docs 存放庫中執行下列指令。

   ```sh
   npm run build:viewer
   ```

   `dist/viewer/` 中會產生 `index.html` 與 `lsdoc.js`。
2. 將這兩個檔案放入要發布的存放庫的 `docs/` 中。
3. 啟用 GitHub Pages。

要顯示的文件根目錄依下列順序決定。

1. `index.html` 中的設定 `source`
2. 同一資料夾的 `lunascape-docs.json` 中記載的 `repository`
3. 由 `*.github.io` 的網址與分支結構推測

## 方法 2：匯出包含文件的靜態網站

將檢視器與文件檔案一併匯出，直接放到主機服務上。

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

輸出內容包含檢視器全套檔案、`docs/` 之下的文件、清單檔 `lunascape-docs-manifest.json` 以及 `.nojekyll`。將輸出結果放到 S3 或 GitHub Pages 即可發布。以 GitHub Actions 自動發布的範例，請參閱存放庫中的 `examples/workflows/publish-docs-pages.yml`。

> **注意**
>
> - **請勿將非公開存放庫的文件匯出後放到 GitHub Pages。** Enterprise Cloud 以外的 GitHub Pages 任何人都能閱讀。若需要限定公開，請使用方法 1，並讓閱讀者以 GitHub 登入。
> - 以 `file://` 直接開啟 `index.html` 無法運作，因為瀏覽器會禁止載入相鄰檔案與執行 ES 模組。要在本機確認時，請使用 VS Code 版或 HTTP 伺服器。
> - TikZ、Vega-Lite、Markmap、WaveDrom、Svgbob、Penrose 的繪圖程式庫會在顯示時載入。在匯出的網站中，請一併放置 `vendor/` 資料夾。

## 相關主題

- [網頁版的功能](README.md)
- [閱讀非公開存放庫](private-repository.md)
