# プロジェクト設定

文書ルート直下の `lunascape-docs.json` は、チームで共有する文書ルートの設定です。Git で管理します。

## 設定ファイルを作成・編集する

- ツールバーの [文書ツール] → [チェック] タブ → [ルールの提供元と文書設定] → [文書設定を編集] を押すと、VS Code で開きます。ファイルがないときは、このときに初期ファイルが作成されます。
- ファイル名 `lunascape-docs.json` には同梱の JSON Schema が自動的に関連付けられ、入力補完と各項目の説明が表示されます。`$schema` の記述は不要です。

## 設定例

```json
{
  "id": "product-docs",
  "title": "製品ドキュメント",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## 項目の説明

| 項目 | 内容 | 既定 |
|---|---|---|
| `id` | 利用者ごとの表示設定を保存するキーです。フォルダを移動しても設定を引き継ぎたいときに、固定の ID を付けます | フォルダのパス |
| `title` | ツールバー左端と文書ルートの一覧に表示する名前です。表示言語を切り替えても変わりません | ルートの README/index の見出し、なければフォルダ名 |
| `indexTitle` | INDEX の見出しです | `INDEX` |
| `startPage` | 最初に開く文書（文書ルートからの相対パス）です | `README.md` |
| `appearance` | 配色です。`light`（常に明るい）または `auto`（VS Code のテーマに追従） | `light` |
| `defaultLocale` | 既定言語（正本の言語）です。BCP 47 の言語タグ（`ja`、`en`、`zh-Hant` など）で指定します。翻訳元になります | 未設定（本文から推定して表示） |
| `fallbackLocale` | 閲覧環境の言語が対応言語のどれとも一致しない読者に、最初に見せる言語です。`locales` に含まれる言語を指定します | 未設定（`defaultLocale` を使用） |
| `locales` | 対応言語の一覧です。`defaultLocale` を含めます。言語メニューと翻訳先の候補になります | `defaultLocale` のみ |
| `ignoredDirectories` | INDEX、検索、チェックから除外するフォルダ名です。指定すると既定を置き換えます | `["99-archive"]` |
| `tree` | INDEX の表示の既定値です。利用者は表示設定で上書きできます | 上記の例のとおり |
| `editor.defaultMode` | 利用者がまだ切り替えていないときの編集表示です。`visual` または `source` | `visual` |
| `editor.showEditButton` | 本文右下の [編集] を表示するかどうかです | `true` |
| `documentStandards.pack` | 文書チェックとテンプレートに使う Standard Pack です。`builtin:<名前>`、または文書ルートからの相対パス | なし |
| `documentStandards.profile` | Pack が定義するプロファイル名です | なし |
| `translation.enabled` | 翻訳案の作成と一括翻訳を有効にします | `true` |
| `translation.contextFiles` | 翻訳時に用語と文体の参考として渡す、正本の Markdown（文書ルートからの相対パス）です | `[]` |
| `translation.maxContextCharacters` | 参考文書の合計文字数の上限です（最大 1048576） | `49152` |

## 設定の優先順位

表示に関する項目は、次の順に優先されます。

1. 利用者の表示設定（[表示設定] パネル）
2. VS Code の設定（`lunascapeDocEditor.*`）
3. `lunascape-docs.json`
4. 製品の既定値

言語（`defaultLocale`、`fallbackLocale`、`locales`）だけは例外で、`lunascape-docs.json` が正本です。VS Code の個人設定でプロジェクトの言語を上書きすることはできません。

> **ご注意**
>
> `docs-lint.config.json` にも `standard` として Standard Pack を指定できます。両方にある場合は `docs-lint.config.json` が優先されます。

## 関連項目

- [チェックルールを変更する](rules.md)
- [表示設定を変更する](../02-reading/display-settings.md)
- [VS Code 設定一覧](../08-reference/settings.md)
