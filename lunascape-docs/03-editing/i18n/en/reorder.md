# Changing the document order

The order shown in the INDEX can be changed by drag and drop or from the keyboard. The new order is saved into the document's front matter as `navigation.order`.

## Reorder by drag and drop

1. Drag a document or folder in the INDEX.
2. Drop it before or after a sibling, or onto a folder.
   Within a level the order changes. Dropping onto another folder moves the item into that folder.

## Reorder with the keyboard or the menu

- Focus an INDEX item and press `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Choose [1つ上へ移動] (Move up) / [1つ下へ移動] (Move down) in the item menu.

## What is saved

- Reordering within a level updates `navigation.order` in the front matter of the canonical document. For a folder it is written to the folder's `README.md`; if the folder has none, a front-matter-only `README.md` is created.
- Moving to another folder moves the canonical document together with its translations. Before the move you are asked to confirm, because relative links may be affected.
- Git staging and committing are never performed.

> **Note**
>
> - Reordering is unavailable while filtering, while editing a document, and in an untrusted workspace.
> - "INDEXが更新されています" (The INDEX has been updated) means another change was just applied. Repeat the operation.
> - The start page cannot be moved to another folder.

> **Hint**
>
> Giving `navigation.order` values in steps of 100, such as 100, 200, 300, makes it easy to insert documents in between later. See [Setting navigation metadata](../04-document-tools/navigation-metadata.md).

## Related topics

- [Creating and organizing documents and folders](organize.md)
- [Setting navigation metadata](../04-document-tools/navigation-metadata.md)
