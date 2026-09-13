# 文件未顯示

## 顯示「找不到可開啟的 Markdown 或 docs 資料夾」

- 工作區中沒有 `docs` 資料夾，或使用了 `docs` 以外的名稱。
  - 只要把 `lunascape-docs.json` 放進該資料夾，不論名稱為何都會被辨識為文件根目錄。
  - 或者，在設定 `lunascapeDocEditor.rootDirectoryNames` 中加入資料夾名稱。
- 若尚未有任何文件，請以「Lunascape Docs: 從範本建立文件」建立。
- 也可以先在編輯器中開啟 Markdown 檔案，再執行「Lunascape Docs: 以規格書檢視器開啟」。

## 文件未顯示在 INDEX 中

- 請確認副檔名為 `.md`、`.markdown` 或 `.mdx`。
- 下列資料夾不會顯示：以 `.` 開頭的資料夾、`node_modules`，以及在 `ignoredDirectories` 中指定的資料夾（預設為 `99-archive`）。
- 位於 `i18n/` 下的翻譯版本不會單獨顯示在 INDEX 中。請從語言選單切換。
- 若剛新增的檔案沒有顯示，請按 [重新載入]。
- 您可能正在檢視其他文件根目錄。請確認工具列最左端的文件根目錄名稱。

## 按下資料夾後沒有任何顯示

該資料夾的 `README.md` 是只有 front matter 而沒有內文的「設定專用描述子」。請在 INDEX 中展開資料夾，並選擇其中的文件。

## 開啟了非預期的文件根目錄

- 當設定 `lunascapeDocEditor.rootMode` 為 `fixed` 時，一律開啟 `lunascapeDocEditor.root`。
- 設為 `auto` 時，會選擇最接近所開啟 Markdown 檔案的文件根目錄。可用工具列最左端的下拉式選單切換。

## 文件根目錄的名稱與預期不同

名稱依下列順序決定：`lunascape-docs.json` 的 `title` → 根目錄 `README.md` 的 `navigation.title` → 其 H1 → `index.md` → 資料夾名稱。若要固定名稱，請設定 `title`。

## INDEX 消失了

- 在只有 1 份文件的文件根目錄中，INDEX 僅會在首次自動關閉。可用工具列的欄位顯示圖示開啟。也可在 [顯示設定] 的 [只有一份文件時自動隱藏] 中關閉此行為。
- 畫面較窄時，請從 [返回] 左側的 [開啟 INDEX]（三條線）開啟。

## 按下連結沒有開啟

- 「找不到連結目標」：連結目標的檔案不存在。可用文件工具的 [檢查] 確認內部連結。
- 「未開啟不安全或不支援的連結」：指向文件根目錄外部，或 `https://`、`mailto:` 以外配置的連結不會開啟。

## 顯示的語言與預期不同

- 請在語言選單中確認目前頁面的語言及其判定依據。
- 系統會記住您上次選擇的顯示語言。請在語言選單中重新選擇預設語言。
- 若已設定個人設定 `lunascapeDocEditor.locale`，則會優先顯示該語言的翻譯版本。

## 相關項目

- [切換文件根目錄](../02-reading/roots.md)
- [文件根目錄與檔案規範](../04-document-tools/structure.md)
