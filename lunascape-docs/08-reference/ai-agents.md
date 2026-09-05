# AIからの利用

拡張機能は、読み取り専用の Language Model Tool `lunascape_getDocsSpecification` を VS Code に登録します。対応する VS Code のエージェントは、Lunascape Docs の機能、設定、文書規約について質問されたとき、このツールでこのヘルプの内容（一般仕様）を取得できます。

## 使いかた

VS Code のチャットで `#lunascapeDocs` を付けて質問するか、Lunascape Docs の設定や文書構成について質問します。

```text
#lunascapeDocs lunascape-docs.json で英語の翻訳を有効にするには？
```

## ツールの引数

| 引数 | 内容 |
|---|---|
| `topic` | 取得する章です。`all`、`usage`（基本操作）、`structure`（文書ルートとファイル規約）、`editing`（文書を編集する）、`configuration`（プロジェクト設定）、`security`（セキュリティと保存境界）、`ai`（AIからの利用） |
| `locale` | ヘルプの言語です（`ja` または `en`）。省略すると VS Code の表示言語、なければ日本語のヘルプを返します |

> **ご注意**
>
> - ツールは文書の本文を外部へ送信しません。
> - ツールはワークスペース名やローカルパスを返しません。
> - ツールはファイルを変更しません。
> - `AGENTS.md` がなくても、VS Code の対応エージェントから利用できます。拡張機能のツール API を使わない別の AI クライアントには、自動では共有されません。

## 関連項目

- [ヘルプを表示する](../02-reading/help.md)
- [セキュリティと保存境界](security.md)
