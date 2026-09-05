# GitHub のリポジトリを開く

Web 版では、GitHub のリポジトリを指定して文書を開きます。公開リポジトリならログインは不要です。

## 画面から開く

1. <https://docs.lunascape.org/> を開きます。
2. ツールバーの GitHub ボタン（[GitHubのドキュメントを開く]）を押します。
3. [リポジトリを直接指定] にリポジトリを入力し、[開く] を押します。
   GitHub にログインしているときは、[読めるリポジトリから選ぶ] で一覧から選ぶこともできます。

## URL で開く

URL の `source` パラメーターで、開くリポジトリと文書ルートを指定できます。このアドレスを共有すると、相手も同じ文書を開けます。

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs
```

| 指定 | 書きかた |
|---|---|
| リポジトリのみ（既定ブランチのルート） | `github:owner/repo` |
| ブランチまたはタグを指定 | `github:owner/repo@main` |
| 文書ルートのフォルダを指定 | `github:owner/repo@main/docs` |
| GitHub の URL をそのまま | `https://github.com/owner/repo/tree/main/docs` |

特定のページを直接開くには、URL の末尾に `#/` と文書ルートからの相対パスを付けます。

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

ページを移動すると URL の `#/` 以降が更新されるため、ブラウザのアドレスバーからいつでもリンクをコピーできます。ブラウザの [戻る] [進む] も使えます。

> **ご注意**
>
> - ログインしていない状態では、GitHub API の利用制限（1 時間あたり 60 回）があります。文書が多いリポジトリや繰り返しの閲覧では、[GitHub でログイン] してください。
> - `/` を含むブランチ名（`feature/xxx` など）は指定できません。
> - 文書は閲覧者の GitHub 権限で読み込まれます。読み取り権限のない人には表示されません。

## ローカルフォルダの文書を開く

ツールバーの [ローカルフォルダの文書を開く] を押し、端末内のフォルダを選びます。ファイルはブラウザの中で処理され、外部へ送られることはありません。フォルダの選択に対応したブラウザ（Chrome、Edge など）で使えます。

## 関連項目

- [非公開リポジトリを閲覧する](private-repository.md)
- [Web 版で開けない・ログインできない](../07-troubleshooting/web.md)
