# Keeping drafts

When you edit a document in the Web viewer, the changes are not written to the repository. They are kept inside your browser as a "draft".

## Create a draft

1. Open a document and press [編集] (Edit) at the bottom right.
2. Edit and press [保存] (Save).
   "下書きとして保存しました" (Saved as a draft) is shown and the change is stored in the browser.

- Documents with a draft carry a badge in the INDEX. Above the text, "この文書は端末内の下書きです（未公開）" (This document is a draft on this device, not published) is shown.
- [下書き] (Drafts) in the toolbar shows the count and opens the list of drafts.

## Discard a draft

- To discard one document's draft, press [下書きを破棄] (Discard draft) above the text.
- To discard all drafts, use the drafts list.

## Apply drafts to the repository

"Publish request", which sends drafts as a pull request, is implemented but not enabled on the public viewer. To change the repository, edit with the VS Code extension or in a local clone.

> **Note**
>
> - Drafts are stored in the browser (IndexedDB). They do not carry over to another browser or device, and clearing the site data deletes them.
> - When the document in the repository changes after you made a draft, "上流が更新されています" (Upstream has changed) is shown. Check the content and decide whether to discard the draft or keep it.
> - When editing a local folder opened with [ローカルフォルダの文書を開く] (Open documents in a local folder), changes are written straight to the file if the browser supports it. Otherwise they are kept for the current session only.

## Related topics

- [What the Web viewer does](README.md)
- [Editing a document](../03-editing/README.md)
