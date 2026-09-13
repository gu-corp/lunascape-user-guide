# 文件根目錄與檔案慣例

這是 Lunascape Docs 尋找文件並組建 INDEX 時所遵循的規則。檔案系統本身就是正本，因此不需要台帳或建置設定。

## 文件根目錄

- 最接近的 `docs` 資料夾，或放有 `lunascape-docs.json` 的資料夾，會成為文件根目錄。
- 只要放上 `lunascape-docs.json`，資料夾就不必命名為 `docs`。
- 開啟不屬於任何文件根目錄的 Markdown 時，會將該資料夾當作臨時的文件根目錄顯示。

## 顯示於 INDEX 的檔案

- 會顯示 `.md`、`.markdown`、`.mdx` 檔案。即使沒有 front matter 或導覽資訊，新檔案也一定會顯示。
- 以 `.` 開頭的資料夾、`node_modules`，以及在 `ignoredDirectories`（預設為 `99-archive`）中指定的資料夾，都不會顯示。
- `i18n/` 之下的內容會當作翻譯版處理，不會在 INDEX 中單獨顯示。

## 資料夾的封面頁

- 具有正文的 `README.md`（若無則為 `index.md`）會成為該資料夾的封面頁。在 INDEX 中按下資料夾名稱即可開啟封面頁。
- 只有 front matter 而沒有正文的 `README.md`，會被視為「僅供設定的描述子」，不會作為頁面顯示。當你只想為資料夾指定標題或排序時使用。
- 當 `README.md` 與 `index.md` 同時存在時，以 `README.md` 為優先。

## 預設語言與翻譯版

- 預設語言的文件（正本）留在原本的位置。
- 翻譯版放在與正本相同資料夾下的 `i18n/<語言>/`，並使用相同的檔案名稱。在 `i18n/` 之下重新建立整個資料夾結構的做法不會被辨識。
- 解析來源只有這一處。放在其他位置的同名翻譯，會成為不被任何文件視為翻譯的孤立檔案。

```text
docs/
  lunascape-docs.json
  README.md                  ← 文件根目錄的封面頁（起始頁）
  i18n/en/README.md          ← 其英文版
  01-product/
    README.md                ← 資料夾的封面頁
    requirements.md
    i18n/en/README.md        ← 上述兩份文件的英文版
    i18n/en/requirements.md
  99-archive/                ← 預設從 INDEX 排除
```

## 關於 `_meta.json`

Nextra 的 `_meta.json` 不會用於導覽。現有的檔案既不會修改也不會刪除。未來只會由明確的匯入／匯出功能來處理它們。

## 關聯項目

- [設定導覽資訊](navigation-metadata.md)
- [專案設定](project-configuration.md)
- [切換文件根目錄](../02-reading/roots.md)
