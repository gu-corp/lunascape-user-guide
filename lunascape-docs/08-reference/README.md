# 主な仕様

## 動作環境

| 環境 | 要件 |
|---|---|
| VS Code 拡張機能 | VS Code 1.90 以降。書き込みを伴う機能は信頼済みワークスペースで動作します |
| Web ブラウザ版 | 最近の Chrome、Edge、Safari、Firefox。ローカルフォルダの閲覧は、フォルダ選択（File System Access API）に対応したブラウザ |
| Chromium 拡張機能 | Manifest V3。ホスト権限は要求しません |

## 対応する文書

| 項目 | 内容 |
|---|---|
| ファイル | `.md`、`.markdown`、`.mdx` |
| Markdown | GitHub Flavored Markdown（表、タスクリスト、コードブロック、取り消し線）、ローカル画像、YAML front matter |
| MDX | 許可されたコンポーネントのみ表示します。任意のスクリプトは実行しません |
| HTML | DOMPurify 3.4.14 で無害化して表示します |

## 図と数式

| 種類 | 言語名 | 備考 |
|---|---|---|
| 数式 | `$...$`、`$$...$$`、`\(...\)`、`\[...\]` | KaTeX。`trust: false`、`maxSize: 50`、`maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | 埋め込みデータのみ。外部 URL と画像マークは不可 |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | 厳密な JSON のみ |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | 配布版はソースの折りたたみ表示。入力 64 KiB、15 秒、SVG 2 MiB の上限 |
| Penrose（実験的） | `penrose` | `set-theory` プリセットのみ |

## 上限値

| 項目 | 値 |
|---|---|
| テンプレートの展開結果 | 4 MiB |
| 翻訳の参照コンテキスト | 既定 49,152 文字、最大 1,048,576 文字 |
| 一括翻訳の 1 回の対象 | 1,000 文書 |
| 画像の任意幅 | 16〜4096px |

## ファイル

| ファイル | 役割 | Git 管理 |
|---|---|---|
| `lunascape-docs.json` | 文書ルートの設定 | 有 |
| `docs-lint.config.json` | チェックルールの設定 | 有 |
| `.lunascape-docs/translation-freshness.json` | 翻訳の鮮度の記録（パス、言語、ハッシュ、日時のみ） | 有 |
| VS Code の設定・ワークスペース状態 | 個人の表示設定、プロバイダーの選択、INDEX の開閉状態 | 無 |

## 同梱の Standard Pack

`builtin:gu-corp-software` — プロファイル: `base`、`web-application`、`api-service`、`regulated-financial-product`、`smart-contract`

## 関連項目

- [VS Code 設定一覧](settings.md)
- [セキュリティと保存境界](security.md)
