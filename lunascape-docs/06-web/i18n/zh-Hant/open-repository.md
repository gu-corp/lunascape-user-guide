# 開啟 GitHub 存放庫

在 Web 版中，指定 GitHub 存放庫來開啟文件。公開存放庫不需要登入。

## 從畫面開啟

1. 開啟 <https://docs.lunascape.org/>。
2. 按下工具列的 [開啟文件]（資料夾圖示）。
3. 在 [直接指定存放庫] 輸入存放庫，然後按下 [開啟]。
   登入 GitHub 後，也可以透過 [從可讀取的存放庫中選擇] 從清單中挑選。

> **提示**
>
> - 旁邊的 GitHub 圖示會在 github.com 開啟您正在閱讀的文件，並不是開啟文件的操作。

## 以 URL 開啟

網址的形式是把存放庫與文件的位置直接排列而成。路徑是存放庫中的位置，因此與 GitHub 的 URL 排列方式相同。

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| 指定內容 | 寫法 |
|---|---|
| 僅存放庫（預設分支） | `/github/owner/repo` |
| 存放庫中的文件 | `/github/owner/repo/docs/01-product/vision.md` |
| 指定分支或標籤 | 在結尾加上 `?ref=v1.2.0` |

切換頁面時網址也會跟著改變。按下工具列的 [分享此文件]，就能把目前閱讀頁面的連結交給別人。瀏覽器的 [返回] [前進] 也可以使用。

以往 `?source=` 的形式仍然可以照常開啟。開啟之後會改寫成新的形式。

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **注意**
>
> - 未登入時會受到 GitHub API 的使用限制（每小時 60 次）。文件數量多的存放庫或反覆閱讀時，請 [使用 GitHub 登入]。
> - 含有 `/` 的分支名稱（例如 `feature/xxx`），可以用上述網址形式的 `?ref=` 指定。`?source=` 的形式無法表示。
> - 文件是以閱讀者本人的 GitHub 權限載入。沒有讀取權限的人不會看到。

## 開啟本機資料夾中的文件

按下工具列的 [開啟文件]，再從清單下方的 [開啟本機資料夾中的文件] 選擇裝置中的資料夾。檔案會在瀏覽器內處理，不會傳送到外部。可在支援選擇資料夾的瀏覽器（Chrome、Edge 等）中使用。

## 相關項目

- [閱讀非公開存放庫](private-repository.md)
- [Web 版無法開啟或無法登入](../07-troubleshooting/web.md)
