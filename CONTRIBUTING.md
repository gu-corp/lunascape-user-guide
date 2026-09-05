# このリポジトリについて

Lunascape 製品群のユーザーマニュアルを 1 つのリポジトリで管理しています。製品ごとのディレクトリが、それぞれ独立した文書集合です（[Lunascape Docs](https://docs.lunascape.org/) で配信されます）。

| 製品 | 文書集合 | 読む |
|---|---|---|
| Lunascape Mobile | [mobile/](mobile/) | <https://docs.lunascape.org/?source=github:gu-corp/lunascape-user-guide@main/mobile> |
| Lunascape Docs | [lunascape-docs/](lunascape-docs/) | <https://docs.lunascape.org/?source=github:gu-corp/lunascape-user-guide@main/lunascape-docs> |

`desktop/`（Lunascape Desktop）は準備中です。

- 各文書集合は自分の `lunascape-docs.json`・言語構成・INDEX を持ちます。翻訳は各フォルダー横の `i18n/<locale>/` に置きます。`title` と `description` は言語別に書け、ホームのカードと切替に使われます。
- リポジトリ直下の `README.md` はホーム（製品を選ぶ画面）の本文です。見出しと一文だけにし、開発者向けの注記はこのファイルに書きます。
- 修正の提案は Pull Request で歓迎します。Lunascape Docs の閲覧画面から直接編集して「公開依頼」を送ることもできます。
- 移行元: [lunascape-mobile-user-guide](https://github.com/gu-corp/lunascape-mobile-user-guide)（アーカイブ済み。履歴はそちらに残っています）
- `lunascape-docs/` は Lunascape Docs に同梱されているヘルプガイドと同じ内容です（正本は [lunascape-docs](https://github.com/gu-corp/lunascape-docs) の `apps/vscode/help/`。リリースごとにこちらへ写します）。
