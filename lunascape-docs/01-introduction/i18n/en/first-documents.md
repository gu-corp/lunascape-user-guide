# Creating your first documents

In a project that has no documentation folder yet, you can create an initial set of documents from the Command Palette.

1. Open the project folder in VS Code and trust the workspace.
2. Run "Lunascape Docs: テンプレートからドキュメントを作成" (Create documentation from template) from the Command Palette (`⇧⌘P` / `Ctrl+Shift+P`).
   If the workspace has several folders, choose the one to create the documents in.
3. Choose the structure to create.
   - [1ページ文書] (Single-page document): just a `README.md`. Suitable for a short specification, notes or a standalone explanation.
   - [ドキュメント一式] (Documentation set): a top page plus entry pages for `specification/`, `manual/` and `help/`.
4. Enter the document title. It is used for the README and the headings of each document.
5. Enter the documentation folder to create, relative to the workspace. The default is `docs`.
6. Review the list of files to be created and press [作成] (Create).
   When creation finishes, the new `README.md` opens in the viewer.

> **Note**
>
> - Existing files are never overwritten. If even one of the files to be created already exists, nothing is created and the operation stops.
> - Creation is not available in an untrusted workspace.

> **Hint**
>
> - If you already have a documentation folder, skip this and go to [Basic operations](../02-reading/README.md).
> - As the documentation grows, add documents one at a time from templates in the [作成] (Create) tab of Document Tools.

## Related topics

- [Creating a document from a template](../04-document-tools/templates.md)
- [Documentation roots and file conventions](../04-document-tools/structure.md)
