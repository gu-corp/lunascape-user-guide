# 文書ルートを切り替える

文書ルートは、1 組の文書の最上位フォルダです。INDEX、絞り込み、チェック、翻訳は、すべて文書ルート単位で動作します。

## 文書ルートの見つけかた

Lunascape Docs は、開いた Markdown ファイルから親フォルダをたどり、次のいずれかに当たる最も近いフォルダを文書ルートにします。

- `lunascape-docs.json` があるフォルダ（フォルダ名は問いません）
- `docs` という名前のフォルダ（設定 `lunascapeDocEditor.rootDirectoryNames` で名前を追加できます）

「Lunascape Docs: 仕様書ビューアーを開く」を実行したときは、設定 `lunascapeDocEditor.root`（既定 `docs`）の文書ルートを開きます。

## 別の文書ルートに切り替える

ワークスペースに文書ルートが複数あるときは、ツールバー左端の文書ルート名がプルダウンになります。

1. ツールバー左端の文書ルート名を押します。
2. 一覧から文書ルートを選びます。
   選んだ文書ルートの開始ページが表示され、INDEX が切り替わります。

> **ヒント**
>
> 一覧に表示される名前は、次の順で決まります。表示言語を切り替えても変わりません。
>
> 1. `lunascape-docs.json` の `title`
> 2. ルートの `README.md` の `navigation.title`、なければその H1
> 3. ルートの `index.md` の `navigation.title`、なければその H1
> 4. フォルダ名（標準の `docs` フォルダでは、その親フォルダ名）

## 文書ルートに属さない Markdown を開く

文書ルートに含まれない Markdown ファイルを開くと、そのファイルのあるフォルダを一時的な文書ルートとして表示します。INDEX には、同じフォルダとその下にある Markdown ファイルが並びます。

- ツールバーの [上のフォルダへ] を押すと、ワークスペース内の親フォルダまで表示範囲を広げられます。
- この表示では、プロジェクトの言語設定と一括翻訳は使えません。そのフォルダに `lunascape-docs.json` を置いて文書ルートにすると使えるようになります。

## 常に決まった文書ルートを開く

設定 `lunascapeDocEditor.rootMode` を `fixed` にすると、どの Markdown を開いても、常に `lunascapeDocEditor.root` の文書ルートを開きます。

## 関連項目

- [文書ルートとファイル規約](../04-document-tools/structure.md)
- [プロジェクト設定](../04-document-tools/project-configuration.md)
- [VS Code 設定一覧](../08-reference/settings.md)
