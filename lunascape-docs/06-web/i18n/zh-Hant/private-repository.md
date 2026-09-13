# 閱覽非公開儲存庫

非公開儲存庫的文件，只要使用 GitHub 登入，就能閱覽自己具有讀取權限的儲存庫。Lunascape Docs 本身不會持有任何帳戶或權限。

## 登入並開啟

1. 開啟 <https://docs.lunascape.org/>。
   若指定了非公開的文件，或尚未登入，就會顯示登入畫面。
2. 按下 [使用 GitHub 登入]。
   GitHub 的驗證畫面會以彈出視窗開啟。
3. 登入完成後，按下工具列的 [開啟文件]，並在 [從可讀取的存放庫中選擇] 中選擇要開啟的儲存庫。

> **提示**
>
> - 登入中的帳戶名稱會顯示在工具列上。[登出] 與 [使用其他帳戶登入] 也可以從這裡進行。
> - 清單中顯示的，是已安裝 GitHub App「Lunascape Docs」的帳戶（組織或個人）的儲存庫中，自己具有讀取權限的那些。

## 儲存庫擁有者需進行的設定

如果清單中沒有顯示目標儲存庫，就必須由儲存庫的擁有者或組織的管理員安裝 GitHub App「Lunascape Docs」。

- 要求的權限為 Contents（讀寫）與 Pull requests（讀寫）。讀取用於閱覽，寫入用於從 Web 發送發佈請求（Pull Request）。Lunascape Docs 不會保存文件的內容。
- 安裝的單位是帳戶（組織或個人）。可設定將對象設為「All repositories」（自動包含日後建立的儲存庫），或僅限所選的儲存庫。

| 場景 | 步驟 |
|---|---|
| 於新的組織或個人帳戶導入 | 從[安裝頁面](https://github.com/apps/lunascape-docs/installations/new)進行 |
| 在已導入的組織中新增目標儲存庫 | 於組織的 Settings → GitHub Apps → Lunascape Docs → Configure → Repository access 中設定 |

即使在整個組織安裝，各成員能閱覽的也只有自己具有讀取權限的儲存庫。能發送發佈請求的，也只有自己具有寫入權限的儲存庫。

> **提示**
> - 新安裝時，要求的權限會在安裝畫面上以清單顯示，按下「Install」的當下即視為已核准。無須額外操作。
> - 在權限增加之前就已安裝的組織，管理員會收到一封確認信，並在組織的 Settings → GitHub Apps → Lunascape Docs → Configure 上方顯示核准按鈕。在核准之前，該組織只能閱覽，發送發佈請求時會顯示「需要授予寫入權限」。
> - 目前是以哪些權限加入的，可在同一個 Configure 畫面確認。個人帳戶則為 Settings → Applications → Installed GitHub Apps。
> - 若不慎移除目標儲存庫或解除安裝，只要從[安裝頁面](https://github.com/apps/lunascape-docs/installations/new)重新加入即可復原。發佈請求的拒絕訊息中，會附上前往修正畫面的連結。
> - 若儲存庫端不想接受發佈請求，請在 `lunascape-docs.json` 中寫入 `"publish": { "enabled": false }`。閱覽功能仍可照常使用。

## 關聯項目

- [開啟 GitHub 的儲存庫](open-repository.md)
- [無法在 Web 版開啟或登入](../07-troubleshooting/web.md)
