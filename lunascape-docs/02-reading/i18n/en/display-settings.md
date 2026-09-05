# Changing display settings

[表示設定] (Display settings, gear) in the toolbar lets each user change how the INDEX looks and whether the Edit button is shown.

1. Press [表示設定] (Display settings) in the toolbar.
2. Toggle the items you want to change. Changes apply immediately.
3. Press [表示設定] again, or click outside the panel, to close it.

## Available settings

| Section | Item | Function |
|---|---|---|
| 文書言語 (Document language) | (current state) | Shows the project default language and the current display language. [プロジェクト言語を設定…] (Configure project languages…) opens the project language settings |
| コンテンツ (Content) | [ファイル名] (File names) | Shows file names instead of document titles |
| | [文書アイコン] (Document icons) | Shows an icon next to each document |
| | [フォルダアイコン] (Folder icons) | Shows an icon next to each folder |
| | [フォルダ内件数] (Item counts) | Shows the number of documents in each folder |
| | [階層ガイド] (Guide lines) | Shows guide lines for nesting |
| | [文書が1件なら自動的に隠す] (Auto-hide for a single document) | Closes the INDEX once, on first open, in a documentation root with only one document |
| | [文書情報を折りたたむ] (Collapse document information) | Collapses the document-control table at the top of a document into a "Document information" row. When off, the table is shown as is |
| | [表示密度] (Density) | Row spacing of the INDEX: [標準] (Comfortable) / [コンパクト] (Compact) |
| | [編集ボタン] (Edit button) | Shows [編集] (Edit) at the bottom right of the document |
| Actions | [プロジェクト既定に戻す] (Reset to project defaults) | Removes all of your overrides and returns to the project settings |
| | [拡張機能設定を開く] (Open extension settings) | Opens the Lunascape Docs settings in the VS Code Settings editor |

> **Hint**
>
> - Display settings are stored per user and per documentation root, and never written to Git-tracked files.
> - Settings apply in the order "your display settings → VS Code settings → `lunascape-docs.json` → product defaults". Team-wide defaults go into `tree` and `editor` in `lunascape-docs.json`.

## Switch the color theme

Press the theme toggle (sun/moon) in the toolbar to switch between a white background and the VS Code color theme. The initial theme comes from the `lunascapeDocEditor.appearance` setting (`light` or `auto`).

## Related topics

- [Using the INDEX](index-panel.md)
- [Project configuration](../04-document-tools/project-configuration.md)
- [VS Code settings](../08-reference/settings.md)
