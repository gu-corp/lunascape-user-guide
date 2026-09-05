# 自分の文書を Web に公開する

自分のリポジトリの文書を、GitHub Pages や任意の静的ホスティングで Web サイトとして公開できます。公開のしかたは 2 とおりあります。この手順は、Lunascape Docs のリポジトリを clone して `npm` を使える開発者向けです。

## 方法 1: ビューアーの 2 ファイルを置く

ビューアー本体（`index.html` と `lsdoc.js`）だけを配置し、文書は GitHub から読み込む方法です。文書自体はサイトに含まれないため、非公開リポジトリでも安全です（閲覧者は GitHub でログインします）。

1. Lunascape Docs のリポジトリで次のコマンドを実行します。

   ```sh
   npm run build:viewer
   ```

   `dist/viewer/` に `index.html` と `lsdoc.js` が生成されます。
2. 2 つのファイルを、公開したいリポジトリの `docs/` に置きます。
3. GitHub Pages を有効にします。

表示する文書ルートは、次の順で決まります。

1. `index.html` 内の設定 `source`
2. 同じフォルダの `lunascape-docs.json` に記載された `repository`
3. `*.github.io` の URL とブランチ構成からの推定

## 方法 2: 文書を含む静的サイトを書き出す

ビューアーと文書ファイルをまとめて書き出し、そのままホスティングする方法です。

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

ビューアー一式、`docs/` の下の文書、一覧ファイル `lunascape-docs-manifest.json`、`.nojekyll` が出力されます。出力先を S3 や GitHub Pages に配置すると公開できます。GitHub Actions で自動的に公開する例は、リポジトリの `examples/workflows/publish-docs-pages.yml` を参照してください。

> **ご注意**
>
> - **非公開リポジトリの文書を書き出して GitHub Pages に置かないでください。** Enterprise Cloud 以外の GitHub Pages は誰でも閲覧できます。限定公開が必要な場合は方法 1 を使い、閲覧者に GitHub でログインさせてください。
> - `index.html` を `file://` で直接開いても動作しません。ブラウザが隣接ファイルの読み込みと ES モジュールの実行を禁止するためです。手元で確認するときは、VS Code 版か HTTP サーバーを使ってください。
> - TikZ、Vega-Lite、Markmap、WaveDrom、Svgbob、Penrose の描画ライブラリは表示時に読み込まれます。書き出したサイトでは `vendor/` フォルダも一緒に配置してください。

## 関連項目

- [Web 版でできること](README.md)
- [非公開リポジトリを閲覧する](private-repository.md)
