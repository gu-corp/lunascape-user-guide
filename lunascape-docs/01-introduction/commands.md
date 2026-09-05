# コマンド一覧

コマンドパレット（`⇧⌘P` / `Ctrl+Shift+P`）で「Lunascape Docs」と入力すると、次のコマンドを実行できます。

| コマンド | 働き |
|---|---|
| Lunascape Docs: 仕様書ビューアーを開く | 最も近い文書ルートをビューアーで開きます。閲覧、編集、チェック、翻訳はこの画面で行います |
| Lunascape Docs: 仕様書ビューアーで開く | エディターで開いている Markdown ファイルをビューアーで表示します |
| Lunascape Docs: テンプレートからドキュメントを作成 | 文書フォルダがないプロジェクトに、最初の文書一式を作成します |
| Lunascape Docs: 文書ルートを検証 | 文書ルート全体を docs-lint でチェックし、結果を文書ツールと「問題」パネルに表示します |
| Lunascape Docs: 翻訳に使うツールを選択… | 翻訳案の生成に使うツール（VS Code の言語モデル、または Claude CLI）を選び直します |
| Lunascape Docs: ヘルプを開く | このヘルプガイドを開きます |

## エクスプローラーからの操作

エクスプローラーで `.md`、`.markdown`、`.mdx` ファイルを右クリックすると、[Lunascape Docs: 仕様書ビューアーで開く] を選べます。

> **ヒント**
>
> Markdown ファイルを普通に開いたときも Lunascape Docs で表示するには、ワークスペースの設定にエディターの関連付けを追加します。
>
> ```json
> {
>   "workbench.editorAssociations": {
>     "*.md": "lunascapeDocEditor.markdownPortal"
>   }
> }
> ```

## ウォークスルー

VS Code の [ヘルプ] メニュー →「ようこそ」にあるウォークスルー「Lunascape Docsを始める」から、文書の作成、ビューアーを開く、ヘルプ、AI からの参照を順に試せます。

## 関連項目

- [基本操作](../02-reading/README.md)
- [キーボード操作一覧](../08-reference/keyboard.md)
