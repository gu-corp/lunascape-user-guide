# チェックルールを変更する

各チェック項目の通知レベル（エラー、警告、情報）を変更したり、使わないようにしたりできます。変更は文書ルートの `docs-lint.config.json` に保存され、チームで共有されます。

## 通知レベルを変更する

1. ツールバーの [文書ツール] を押し、[チェック] タブを開きます。
2. [ルールを確認・変更] を押します。
   チェック項目の一覧が同じカードの中に展開されます。各項目には目的と、現在の設定の提供元（Project、Profile、Pack、Default）が表示されます。
3. 変更したい項目の通知レベルを選びます。
4. [保存して再チェック] を押します。
   設定が保存され、文書ルート全体が新しい設定でチェックし直されます。

| 選択肢 | 意味 |
|---|---|
| [標準設定（…）] | 上書きを削除し、プロファイル、Standard Pack、既定値の順で決まる標準の設定に戻します |
| [使わない] | この項目をチェックしません |
| [情報] / [警告] / [エラー] | この通知レベルで報告します |

> **ご注意**
>
> - 保存には信頼済みのワークスペースが必要です。
> - 保存されるのは各項目の通知レベルだけです。項目ごとのオプションはそのまま保持されます。Standard Pack とプロファイル自体は、この画面では変更しません。
> - 保存の直前に `docs-lint.config.json` が外部で変更されていた場合、保存は中止されます。最新の状態を読み込んでからやり直してください。
> - `docs-lint.config.json` がない場合は、保存したときに作成されます。

## 設定ファイルを直接編集する

- [詳細設定を開く] を押すと、`docs-lint.config.json` を VS Code で開きます。
- [ルールの提供元と文書設定] を開き、[文書設定を編集] を押すと、`lunascape-docs.json` を VS Code で開きます。Standard Pack とプロファイルはここで選びます。

どちらのファイルも、拡張機能に同梱した JSON Schema による入力補完と説明が有効です。

## Standard Pack とプロファイル

Standard Pack は、必要な文書の種類、章立て、用語、テンプレートをまとめた文書標準です。`lunascape-docs.json` の `documentStandards` で選びます。

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

同梱の Pack `builtin:gu-corp-software` には、`base`、`web-application`、`api-service`、`regulated-financial-product`、`smart-contract` のプロファイルがあります。

## 関連項目

- [文書をチェックする](check.md)
- [プロジェクト設定](project-configuration.md)
