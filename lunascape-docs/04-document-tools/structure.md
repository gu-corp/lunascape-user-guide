# 文書ルートとファイル規約

Lunascape Docs が文書を見つけ、INDEX を組み立てるときの規則です。ファイルシステムがそのまま正本になるため、台帳やビルドの設定は必要ありません。

## 文書ルート

- 最も近い `docs` フォルダ、または `lunascape-docs.json` を置いたフォルダが文書ルートになります。
- `lunascape-docs.json` を置けば、フォルダ名は `docs` でなくてもかまいません。
- 文書ルートに属さない Markdown を開くと、そのフォルダを一時的な文書ルートとして表示します。

## INDEX に表示されるファイル

- `.md`、`.markdown`、`.mdx` のファイルを表示します。front matter やナビゲーション情報がなくても、新しいファイルは必ず表示されます。
- `.` で始まるフォルダ、`node_modules`、および `ignoredDirectories`（既定は `99-archive`）に指定したフォルダは表示されません。
- `i18n/` の下は翻訳版として扱い、INDEX には個別に表示しません。

## フォルダの表紙

- 本文のある `README.md`（なければ `index.md`）は、そのフォルダの表紙になります。INDEX でフォルダ名を押すと表紙が開きます。
- front matter だけで本文のない `README.md` は「設定専用の記述子」として扱い、ページとしては表示しません。フォルダのタイトルや順序だけを持たせたいときに使います。
- `README.md` と `index.md` の両方があるときは、`README.md` を優先します。

## 既定言語と翻訳版

- 既定言語の文書（正本）は、そのままの場所に置きます。
- 翻訳版は、正本と同じフォルダーの `i18n/<言語>/` に、同じファイル名で置きます。フォルダー構造を `i18n/` の下に作り直す形では認識されません。
- 解決先はこの 1 か所だけです。別の場所に置いた同名の翻訳は、どの文書の翻訳としても扱われない孤立ファイルになります。

```text
docs/
  lunascape-docs.json
  README.md                  ← 文書ルートの表紙（開始ページ）
  i18n/en/README.md          ← その英語版
  01-product/
    README.md                ← フォルダの表紙
    requirements.md
    i18n/en/README.md        ← 上の 2 文書の英語版
    i18n/en/requirements.md
  99-archive/                ← 既定で INDEX から除外
```

## `_meta.json` について

Nextra の `_meta.json` は、ナビゲーションには使いません。既存のファイルは変更も削除もしません。将来、明示的な取り込み・書き出し機能でだけ扱う予定です。

## 関連項目

- [ナビゲーション情報を設定する](navigation-metadata.md)
- [プロジェクト設定](project-configuration.md)
- [文書ルートを切り替える](../02-reading/roots.md)
