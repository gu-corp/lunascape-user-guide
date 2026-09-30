# このリポジトリについて

Lunascape 製品群のユーザーマニュアルを 1 つのリポジトリで管理しています。製品ごとのディレクトリが、それぞれ独立した文書集合です（[Lunascape Docs](https://docs.lunascape.org/) で配信されます）。

| 製品 | 文書集合 | 読む |
|---|---|---|
| Lunascape Desktop | [desktop/](desktop/) | <https://docs.lunascape.org/github/gu-corp/lunascape-user-guide/desktop> |
| Lunascape Mobile | [mobile/](mobile/) | <https://docs.lunascape.org/github/gu-corp/lunascape-user-guide/mobile> |
| Lunascape Docs | [lunascape-docs/](lunascape-docs/) | <https://docs.lunascape.org/github/gu-corp/lunascape-user-guide/lunascape-docs> |

- 各文書集合は自分の `lunascape-docs.json`・言語構成・INDEX を持ちます。翻訳は各フォルダー横の `i18n/<locale>/` に置きます。`title` と `description` は言語別に書け、ホームのカードと切替に使われます。
- リポジトリ直下の `README.md` はホーム（製品を選ぶ画面）の本文です。見出しと一文だけにし、開発者向けの注記はこのファイルに書きます。
- 画像（スクリーンショット）は、文章だけでは場所や見た目が伝わらないところにだけ入れます。1 つのセクションに何枚も並べません。
  - 文書と同じフォルダーの `img/` に置き、`<img src="img/…" alt="…" width="560" />` のように相対パスで参照します。`width` は数値だけで、ウィンドウ全体は `760`、ダイアログや部分の切り抜きは `560` か `360` を目安にします。
  - ファイル名は内容がわかる名前（`site-info-popup.png` など）にします。翻訳版は `i18n/<locale>/img/` に、その言語の画面で撮った同じ名前のファイルを置きます。
  - アクセストークン、シードフレーズ、個人のブックマークや履歴が写らないようにします。撮影には空のプロファイルを使います。
- 修正の提案は Pull Request で歓迎します。Lunascape Docs の閲覧画面から直接編集して「公開依頼」を送ることもできます。
- 移行元: [lunascape-mobile-user-guide](https://github.com/gu-corp/lunascape-mobile-user-guide)（アーカイブ済み。履歴はそちらに残っています）
- `lunascape-docs/` は Lunascape Docs に同梱されているヘルプガイドと同じ内容です（正本は [lunascape-docs](https://github.com/gu-corp/lunascape-docs) の `apps/vscode/help/`。リリースごとにこちらへ写します）。
