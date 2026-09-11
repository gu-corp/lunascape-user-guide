# VS Code 設定一覧

VS Code の設定（`⌘,` / `Ctrl+,`）で「Lunascape Docs」を検索すると、次の項目を変更できます。いずれも利用者ごとの設定で、プロジェクトの文書には保存されません。

## 文書ルート

| 設定 | 値 | 既定 | 働き |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` は開いた Markdown に最も近い文書ルートを自動で選び、属さなければ親フォルダを一時的に開きます。`fixed` は常に `root` の文書ルートを開きます |
| `lunascapeDocEditor.rootDirectoryNames` | 文字列の配列 | `["docs"]` | `auto` で文書ルートとして自動発見するフォルダ名です。`lunascape-docs.json` があるフォルダは名前に関係なく発見します。リポジトリ直下の `lunascape-docs.json` に `defaultFolder` または `roots` があるときは、そちらが優先されます |
| `lunascapeDocEditor.root` | パス | `docs` | `fixed` モード、またはコマンドから開くときの、ワークスペースからの相対文書ルートです |
| `lunascapeDocEditor.startPage` | パス | `README.md` | 文書ルートからの相対開始ページです |
| `lunascapeDocEditor.title` | 文字列 | `Lunascape Docs` | 文書タブのタイトルを上書きします。文書ルートの選択名には影響しません |
| `lunascapeDocEditor.ignoredDirectories` | 文字列の配列 | `["99-archive"]` | INDEX から除外するフォルダ名です |

## 表示

| 設定 | 値 | 既定 | 働き |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` は白背景、`auto` は VS Code の配色に追従します |
| `lunascapeDocEditor.locale` | 言語タグ | なし | 利用できる場合に優先して表示する、個人の文書言語です。プロジェクトの正本言語は変更しません |
| `lunascapeDocEditor.documentMetadata.compact` | 真偽値 | `true` | H1 直後の文書管理表を「文書情報」の行に折りたたみます |
| `lunascapeDocEditor.tree.showFileNames` | 真偽値 | `false` | INDEX に文書名の代わりにファイル名を表示します |
| `lunascapeDocEditor.tree.showDocumentIcons` | 真偽値 | `false` | INDEX に文書アイコンを表示します |
| `lunascapeDocEditor.tree.showFolderIcons` | 真偽値 | `false` | INDEX にフォルダアイコンを表示します |
| `lunascapeDocEditor.tree.showItemCounts` | 真偽値 | `false` | INDEX にフォルダ直下の項目数を表示します |
| `lunascapeDocEditor.tree.showGuides` | 真偽値 | `true` | INDEX に階層のガイド線を表示します |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | INDEX の行間です |
| `lunascapeDocEditor.tree.autoHideSingleItem` | 真偽値 | `true` | 文書が 1 件だけのとき、INDEX を初回だけ閉じます |

## 編集

| 設定 | 値 | 既定 | 働き |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | まだ切り替えていないときの編集表示です。最後に使った表示のほうが優先されます |
| `lunascapeDocEditor.editor.showEditButton` | 真偽値 | `true` | 本文右下の [編集] を表示します |

## 図

| 設定 | 値 | 既定 | 働き |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | TikZ の描画ランタイムです。`bundled` は同梱の承認済みランタイム（現在の配布版には同梱されていません）、`workspace` は信頼済みワークスペース直下の `node-tikzjax` 1.0.5（開発・評価専用）、`disabled` は描画しません |

## 非推奨の設定

| 設定 | 代わりに使うもの |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `lunascape-docs.json` の `defaultLocale` |
| `lunascapeDocEditor.locales` | `lunascape-docs.json` の `locales` |

個人の設定でプロジェクトの言語を上書きすることはできません。

## 関連項目

- [表示設定を変更する](../02-reading/display-settings.md)
- [プロジェクト設定](../04-document-tools/project-configuration.md)
