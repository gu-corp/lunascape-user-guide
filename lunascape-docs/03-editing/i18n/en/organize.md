# Creating and organizing documents and folders

From the INDEX item menu you can create, duplicate, rename and delete documents and folders. Input happens in a small dialog inside the viewer, without interrupting reading.

> **Note**
>
> These actions are available only when the workspace is trusted in VS Code. They cannot run while a document is being edited, while another operation is in progress, or when the target has unsaved changes.

## Create a document or folder

1. Open the item menu ([⋯] or right-click) of the destination folder.
   To create directly under the documentation root, use [⋯] at the right end of the INDEX heading or right-click an empty part of the INDEX.
2. Choose [新しい文書] (New document) or [新しいフォルダ] (New folder).
3. Enter a name and press [作成] (Create).
   A document name needs a Markdown extension (`.md`, `.markdown`, `.mdx` and so on).

New documents are created as default-language (canonical) documents.

## Duplicate a document

1. Open the document's item menu and choose [複製] (Duplicate).
2. Enter a new name and press [作成] (Create).

Only the canonical document is duplicated; its translations are not.

## Change the title

Changes the document heading (H1). The file name stays the same.

1. Open the item menu of a document or folder and choose [タイトルを変更] (Change title).
2. Enter the new title on one line and press [変更] (Change).

For a folder, the heading of its `README.md` is changed. When a translation is being displayed, the title of that language's document is changed.

## Change the documentation name

Changes the documentation name shown in the toolbar (the name of the documentation root).

1. Right-click the documentation name in the toolbar. The [⋯] at the right of the INDEX heading opens the same menu.
2. Choose [文書名を変更] (Change documentation name) and enter a new name.

While nothing is configured, the folder name is shown as is.

A name you set is written to **whichever place currently supplies the documentation name**, so a heading you can see never ends up ignored.

| Current state | Written to |
|---|---|
| `lunascape-docs.json` holds a name | `lunascape-docs.json` is updated |
| No name, but the documentation root has a README | The README's heading (H1) is rewritten |
| Neither | `lunascape-docs.json` is created and the name saved there |

The message shown after the change says which one was written.

> **Hint**
>
> The documentation name is resolved in this order: the name in `lunascape-docs.json`, then the heading of the documentation root's README, then the folder name.

## Rename a file or folder

1. Open the item menu and choose [ファイル名を変更] (Rename file) or [フォルダ名を変更] (Rename folder).
2. Enter the new name and press [変更] (Change).

The corresponding translations (the same path under `i18n/<locale>/`) are renamed together.

## Delete

1. Open the item menu and choose [ゴミ箱へ移動] (Move to trash).
2. Check the confirmation message and approve the move.

The target is moved to the operating system's trash, so it can be restored if needed. Translations are not deleted and remain in place.

## Names that cannot be used

- Names starting with `.` (they would not appear in the INDEX)
- `i18n` (reserved for translation files)
- Names reserved by Windows (`CON`, `PRN` and so on)
- Names ending with a period or a space
- Names containing control characters or characters not allowed in file names
- Names that already exist in the same folder (including names that differ only in letter case)

> **Note**
>
> The start page (normally the root `README.md`) cannot be renamed or moved. Change `startPage` in `lunascape-docs.json` first.

## Related topics

- [Changing the document order](reorder.md)
- [Using the INDEX](../02-reading/index-panel.md)
