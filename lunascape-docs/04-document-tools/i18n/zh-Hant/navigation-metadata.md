# 設定導覽資訊

INDEX 中顯示的名稱與順序，寫在各文件的 YAML front matter 裡。即使不寫，文件仍會顯示，並採用標題（H1）與檔名順序。

## 文件的名稱與順序

在文件開頭寫入如下內容。

```yaml
---
navigation:
  title: 開始使用
  order: 200
---
```

| 項目 | 內容 |
|---|---|
| `navigation.title` | 在 INDEX 中顯示的名稱。省略時使用 H1，若也沒有則使用檔名 |
| `navigation.order` | 決定排序的整數，由小到大排列。省略時採用穩定的預設順序（依檔名） |

> **提示**
>
> - 將 `order` 以 100、200、300 這樣每 100 為間隔設定，之後便能在中間插入 150。
> - 即使有未指定、不正確或重複的 `order`，文件也不會被隱藏。
> - 在 INDEX 中重新排序時，`navigation.order` 會自動寫入，無需手動撰寫。

## 資料夾的名稱與順序

資料夾的名稱與順序，由該資料夾的 `README.md`（若沒有則為 `index.md`）的 front matter 保存。封面頁不需要有正文內容。

```yaml
---
navigation:
  title: 產品企劃
  order: 100
---
```

沒有封面頁的資料夾，會以資料夾名稱與預設順序顯示。當在 INDEX 中變更標題或重新排序而有需要時，會建立僅含 front matter 的 `README.md`。僅是閱覽並不會建立檔案。

## 翻譯版的處理方式

- 順序，以及資料夾的角色（是封面頁還是僅供設定），僅由預設語言的文件決定。
- 翻譯版只能覆寫 `navigation.title`。當正本有正文內容時，翻譯版的 H1 也會作為名稱使用。
- 即使只有翻譯版，也不會增加頁面。

## 子項目的排列與折疊

在資料夾的封面頁中，已定義用來指定其直屬子項目的排列方式與初始折疊狀態的 `navigation.children.sort` 與 `navigation.children.defaultCollapsed`。在 VS Code 中的讀取與編輯將於日後支援。

## 相關項目

- [變更文件的排序](../03-editing/reorder.md)
- [文件根目錄與檔案規約](structure.md)
