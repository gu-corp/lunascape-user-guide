# Using the INDEX

The INDEX on the left is the tree of folders and documents in the documentation root.

## Filter

1. Type a word into [文書を絞り込み] (Filter documents) above the INDEX.
2. Only documents whose names match are shown. Clear the field to show everything again.

> **Note**
>
> Drag-and-drop reordering is disabled while a filter is active.

## Expand and collapse folders

- Press the arrow to the left of a folder name, or the name of a folder without a landing page, to expand or collapse it.
- A folder with a landing page (a `README.md` or `index.md` with body content) opens that page when you press its name. To expand or collapse only, use [フォルダを開く] (Expand folder) / [フォルダを閉じる] (Collapse folder) in the item menu.
- Expansion state is remembered per user and never written to Git-tracked files.

## README and the folder cover

`README.md` is the file that describes what a folder holds.

- Pressing the name of a folder that has a README shows that README.
- A folder without one shows the first document inside it instead.
- The README's heading (H1) becomes the folder's name in the INDEX.

A README is not required. To add one later, choose [READMEを作成] (Create README) from the folder's item menu; it appears only for folders that have none.

## Show or hide the INDEX

- The left icon in the toolbar's column controls shows or hides the INDEX. The right icon shows or hides "This page".
- On narrow screens the INDEX starts closed. Press [INDEXを開く] (Open INDEX, three lines) to the left of [戻る] (Back) to open it as an overlay on top of the document. Close it with the [×] inside the INDEX, a click on the backdrop, `Esc`, or by navigating. This transient state never changes the wide-layout setting.
- In a documentation root with only one document, the INDEX closes itself once on first open. Reopen it with the column icon. Turn this off with [文書が1件なら自動的に隠す] (Auto-hide for a single document) in [表示設定] (Display settings).

## Use the item menu

Hover an INDEX item to reveal [⋯], or right-click the item, to open its menu. The items appear in this order.

| Group | Items |
|---|---|
| Frequent actions | [フォルダを開く] / [フォルダを閉じる] (Expand / Collapse folder), [INDEXを開く] (Open the folder's landing page), [編集] (Edit), [タイトルを変更] (Change title), [VS Codeで開く] (Open in VS Code), [パスをコピー] (Copy path) |
| Create and organize | [READMEを作成] (Create README, folders without one only), [新しい文書] (New document), [新しいフォルダ] (New folder), [複製] (Duplicate), [ファイル名を変更] / [フォルダ名を変更] (Rename file / folder), [1つ上へ移動] (Move up), [1つ下へ移動] (Move down) |
| Delete | [ゴミ箱へ移動] (Move to trash) |

- To create directly under the documentation root, use [⋯] at the right end of the INDEX heading or right-click an empty part of the INDEX, then choose [新しい文書] (New document) or [新しいフォルダ] (New folder).
- Inside a menu, `↑` `↓` move between items and `Home` `End` jump to the first and last. `Esc` closes the menu and returns focus to where it was opened.

> **Note**
>
> The create, organize and delete items appear only when the workspace is trusted in VS Code. They are also unavailable while a document is being edited or another INDEX operation is in progress.

## Change the appearance

From [表示設定] (Display settings) you can show file names, document and folder icons, item counts, guide lines, and change the density. See [Changing display settings](display-settings.md).

## Related topics

- [Creating and organizing documents and folders](../03-editing/organize.md)
- [Changing the document order](../03-editing/reorder.md)
