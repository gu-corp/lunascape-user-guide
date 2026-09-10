# 拡張機能をインストールする

VS Code 拡張機能「Lunascape Docs」は VSIX ファイルとして配布しています。

## 動作環境

- VS Code 1.90 以降
- 文書の作成、INDEX からの整理、チェック設定の保存、翻訳など、書き込みを伴う機能は、VS Code で「信頼済み」にしたワークスペースでだけ使えます。

## インストールする

1. VSIX ファイルを取得します。このリンクは常に最新版を指します。

   [lunascape-doc.vsix をダウンロード](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-doc.vsix)

2. VS Code の拡張機能ビュー（`⇧⌘X` / `Ctrl+Shift+X`）を開きます。
3. 右上の `…` メニューから [VSIX からのインストール...] を選び、取得したファイルを指定します。

## 更新する

新しい版が公開されると、拡張機能がそれを知らせます。[更新] を押すと取得して導入し、ウィンドウを再読み込みすると切り替わります。設定と文書はそのまま残ります。

確認は 1 日に 1 回です。こちらから勝手に入れ替えることはありません。知らせが不要であれば、設定 `lunascapeDocEditor.update.check` を「確認しない」にします。

## バージョンを確認する

拡張機能ビューで「Lunascape Docs」を開くと、インストールされているバージョンが表示されます。不具合を報告するときに必要です。

## 関連項目

- [文書をはじめて作成する](first-documents.md)
- [不具合を報告する](../07-troubleshooting/report.md)
