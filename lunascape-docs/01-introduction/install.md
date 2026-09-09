# 拡張機能をインストールする

VS Code 拡張機能「Lunascape Docs」は Visual Studio Marketplace で公開しています。

## 動作環境

- VS Code 1.90 以降
- 文書の作成、INDEX からの整理、チェック設定の保存、翻訳など、書き込みを伴う機能は、VS Code で「信頼済み」にしたワークスペースでだけ使えます。

## インストールする

1. VS Code の拡張機能ビュー（`⇧⌘X` / `Ctrl+Shift+X`）を開き、「Lunascape Docs」を検索します。
   [Marketplace のページ](https://marketplace.visualstudio.com/items?itemName=lunascape.lunascape-doc)から開いても構いません。
2. [インストール] をクリックします。

## 更新する

Marketplace からインストールした場合、新しい版は自動更新されます。VS Code の設定で自動更新をオフにしているときは、拡張機能ビューに表示される [更新] から手動で更新します。

## バージョンを確認する

拡張機能ビューで「Lunascape Docs」を開くと、インストールされているバージョンが表示されます。不具合を報告するときに必要です。

## VSIX から直接インストールする場合

Marketplace 版の配信より前のリリースを試す、社内ネットワークから Marketplace に到達できない、といった事情があるときは、GitHub のリリースページから `.vsix` ファイルを取得してインストールできます。

1. [リリースページ](https://github.com/gu-corp/lunascape-docs/releases) を開き、目的の版の `.vsix` ファイルをダウンロードします。
   GitHub にログインしていれば、リンクからそのままダウンロードできます。
2. 次のいずれかの方法でインストールします。
   - **ドラッグ＆ドロップ**: VS Code の拡張機能ビュー（`⇧⌘X` / `Ctrl+Shift+X`）に `.vsix` ファイルをドロップします。
   - **メニュー**: 拡張機能ビュー右上の [⋯] から [VSIX からのインストール…] を選び、ファイルを指定します。
   - **コマンドライン**: `code --install-extension <ダウンロードしたファイル>` を実行します。
3. インストール後に変化がないときは、コマンドパレット（`⇧⌘P` / `Ctrl+Shift+P`）で「Developer: Reload Window」を実行します。

この方法でインストールした版は自動更新されません。Marketplace から入れ直すと、以後は自動更新に切り替わります。

> **ヒント**
>
> [GitHub CLI](https://cli.github.com/) を使うと、取得からインストールまでをまとめて実行できます。
>
> ```sh
> gh release download -R gu-corp/lunascape-docs -p '*.vsix' -D /tmp \
>   && code --install-extension /tmp/lunascape-doc-*.vsix
> ```

## 関連項目

- [文書をはじめて作成する](first-documents.md)
- [不具合を報告する](../07-troubleshooting/report.md)
