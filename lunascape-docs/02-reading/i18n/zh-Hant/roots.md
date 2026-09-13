# 切換文件根目錄

文件根目錄是一組文件的最上層資料夾。INDEX、篩選、檢查與翻譯都以文件根目錄為單位運作。

## 文件根目錄的尋找方式

Lunascape Docs 會從開啟的 Markdown 檔案往上層資料夾尋找，並將最接近且符合下列任一條件的資料夾當作文件根目錄。

- 含有 `lunascape-docs.json` 的資料夾（不限資料夾名稱）
- 名稱為 `docs` 的資料夾（可透過設定 `lunascapeDocEditor.rootDirectoryNames` 新增名稱）

執行「Lunascape Docs：開啟規格書檢視器」時，會開啟設定 `lunascapeDocEditor.root`（預設為 `docs`）所指定的文件根目錄。

## 切換到其他文件根目錄

當工作區中有多個文件根目錄時，工具列最左側的文件根目錄名稱會變成下拉式選單。

1. 按下工具列最左側的文件根目錄名稱。
2. 從清單中選擇文件根目錄。
   畫面會顯示所選文件根目錄的起始頁，INDEX 也會一併切換。

> **提示**
>
> 清單中顯示的名稱依下列順序決定，切換顯示語言也不會改變。
>
> 1. `lunascape-docs.json` 的 `title`
> 2. 根目錄 `README.md` 的 `navigation.title`，若無則為其 H1
> 3. 根目錄 `index.md` 的 `navigation.title`，若無則為其 H1
> 4. 資料夾名稱（標準的 `docs` 資料夾則為其上層資料夾名稱）

## 開啟不屬於文件根目錄的 Markdown

開啟不包含在文件根目錄內的 Markdown 檔案時，會將該檔案所在的資料夾當作暫時的文件根目錄來顯示。INDEX 中會列出同一資料夾及其下層的 Markdown 檔案。

- 按下工具列的 [上層資料夾]，可將顯示範圍擴大到工作區內的上層資料夾。
- 在此顯示方式下，無法使用專案的語言設定與批次翻譯。在該資料夾放入 `lunascape-docs.json` 使其成為文件根目錄後即可使用。

## 固定開啟特定的文件根目錄

將設定 `lunascapeDocEditor.rootMode` 設為 `fixed` 後，無論開啟哪一個 Markdown 檔案，都會固定開啟 `lunascapeDocEditor.root` 所指定的文件根目錄。

## 相關項目

- [文件根目錄與檔案慣例](../04-document-tools/structure.md)
- [專案設定](../04-document-tools/project-configuration.md)
- [VS Code 設定一覽](../08-reference/settings.md)
