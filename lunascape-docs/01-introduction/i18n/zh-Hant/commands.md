# 命令一覽

在命令選擇區（`⇧⌘P` / `Ctrl+Shift+P`）輸入「Lunascape Docs」，即可執行下列命令。

| 命令 | 作用 |
|---|---|
| Lunascape Docs：開啟規格書檢視器 | 以檢視器開啟最接近的文件根目錄。閱讀、編輯、檢查與翻譯都在這個畫面進行 |
| Lunascape Docs：以規格書檢視器開啟 | 將編輯器中開啟的 Markdown 檔案顯示在檢視器中 |
| Lunascape Docs：從範本建立文件 | 為沒有文件資料夾的專案建立第一組文件 |
| Lunascape Docs：驗證文件根目錄 | 以 docs-lint 檢查整個文件根目錄，並將結果顯示在文件工具與「問題」面板中 |
| Lunascape Docs：開啟說明 | 開啟本說明手冊 |

## 從檔案總管操作

在檔案總管中以滑鼠右鍵按一下 `.md`、`.markdown` 或 `.mdx` 檔案，即可選擇 [Lunascape Docs：以規格書檢視器開啟]。

> **提示**
>
> 若要讓 Markdown 檔案在一般開啟時也以 Lunascape Docs 顯示，請在工作區設定中加入編輯器關聯。
>
> ```json
> {
>   "workbench.editorAssociations": {
>     "*.md": "lunascapeDocEditor.markdownPortal"
>   }
> }
> ```

## 逐步解說

在 VS Code 的 [說明] 功能表 →「歡迎使用」中，可從逐步解說「開始使用 Lunascape Docs」依序試用最初的操作。

## 相關項目

- [基本操作](../02-reading/README.md)
- [鍵盤操作一覽](../08-reference/keyboard.md)
