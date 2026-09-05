# 拡張機能をインストールする

VS Code 拡張機能「Lunascape Docs」は社内向けに配布しています。Marketplace にはないため、リリースページから `.vsix` ファイルを取得してインストールします。

## 動作環境

- VS Code 1.90 以降
- 文書の作成、INDEX からの整理、チェック設定の保存、翻訳など、書き込みを伴う機能は、VS Code で「信頼済み」にしたワークスペースでだけ使えます。

## インストールする

1. [リリースページ](https://github.com/gu-corp/lunascape-docs/releases) を開き、最新版の `.vsix` ファイルをダウンロードします。
   GitHub にログインしていれば、リンクからそのままダウンロードできます。
2. 次のいずれかの方法でインストールします。
   - **ドラッグ＆ドロップ**: VS Code の拡張機能ビュー（`⇧⌘X` / `Ctrl+Shift+X`）に `.vsix` ファイルをドロップします。
   - **メニュー**: 拡張機能ビュー右上の [⋯] から [VSIX からのインストール…] を選び、ファイルを指定します。
   - **コマンドライン**: `code --install-extension <ダウンロードしたファイル>` を実行します。
3. インストール後に変化がないときは、コマンドパレット（`⇧⌘P` / `Ctrl+Shift+P`）で「Developer: Reload Window」を実行します。

> **ヒント**
>
> [GitHub CLI](https://cli.github.com/) を使うと、取得からインストールまでをまとめて実行できます。
>
> ```sh
> gh release download -R gu-corp/lunascape-docs -p '*.vsix' -D /tmp \
>   && code --install-extension /tmp/lunascape-doc-editor-*.vsix
> ```

## 更新する

本拡張機能は自動更新されません。新しい版が公開されたら、同じ手順でインストールし直します。上書きインストールになるため、事前のアンインストールは不要です。

## バージョンを確認する

拡張機能ビューで「Lunascape Docs」を開くと、インストールされているバージョンが表示されます。不具合を報告するときに必要です。

## 関連項目

- [文書をはじめて作成する](first-documents.md)
- [不具合を報告する](../07-troubleshooting/report.md)
