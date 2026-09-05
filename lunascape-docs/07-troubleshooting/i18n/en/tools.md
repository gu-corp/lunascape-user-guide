# Check, Create or Translation fails

## Check

### "docs-lintを利用できません" (docs-lint is unavailable) is shown

- The docs-lint runtime is missing from the extension, or the configuration has a problem. Reinstall the extension.
- "ローカルPackと設定を安全に読み込むには、VS Codeでこのワークスペースを信頼してください" (Trust this workspace to load the local pack and configuration safely): using a local Standard Pack requires a trusted workspace.

### The result stays at "revalidation required"

Changing a document or a setting invalidates the previous result. Press [文書ルートを検証] (Validate documentation root) again. Unsaved changes are not included.

### Pressing a finding does not open anything

"文書ルート全体" (Entire documentation root) items are not tied to a specific document and have no position. Check the documents described in the finding.

### Rules cannot be saved

- A trusted workspace is required.
- "Lint設定が別の操作で変更されました" (The lint configuration was changed by another operation): `docs-lint.config.json` was changed externally. Reload the latest state and try again.
- Configuration files that are symbolic links or outside the documentation root cannot be edited.

## Creating from a template

- "テンプレートのプレビューが期限切れです" (The template preview has expired) / "入力内容が変更されました" (The input has changed): press [プレビュー] (Preview) again before creating.
- "保存先の文書は既に存在します" (A document already exists at the destination): existing files are never overwritten. Choose another destination.
- The destination needs a path relative to the documentation root and a `.md` / `.mdx` extension. Nothing can be created under `i18n`.
- "文書を作成するにはワークスペースを信頼してください" (Trust the workspace to create documents): trust the workspace in VS Code.

## Translation

### The translation buttons are disabled

- "この文書ルートではAI翻訳が有効になっていません" (AI translation is not enabled for this documentation root): set `translation.enabled` to `true` in `lunascape-docs.json`.
- "プロジェクト既定言語が未設定です" (The project default language is not set): save the default language as described in [Changing display settings](../02-reading/display-settings.md).
- "対応言語に翻訳先を追加してください" (Add the target to the supported languages): add the target language to `locales`.
- "翻訳する正本文書が見つかりません" (No canonical document to translate): a translation is open. Switch to the default-language page.
- Batch translation is unavailable while a folder is open temporarily. Put a `lunascape-docs.json` in the folder to make it a documentation root.

### The provider is unavailable

- "VS Code Language Model APIを利用できません" (The VS Code Language Model API is unavailable): check that you are signed in to the extension that provides language models, or set `lunascapeDocEditor.translation.provider` to `claude`.
- "設定したVS Code言語モデル「…」を利用できません" (The configured VS Code language model "…" is unavailable): check the name in `lunascapeDocEditor.translation.model`, or clear it.
- For the Claude CLI, check that it is installed and logged in.

### A proposal is rejected or must be regenerated

- "正本文書が変更されました。翻訳案を作り直してください" (The canonical document has changed; regenerate the proposal): the source or the target changed after the proposal was generated. Translate again.
- A response that lost protected identifiers or code is not accepted. The response is logged in the "Lunascape Docs 翻訳" output channel.
- "一括翻訳は1回1000文書までです" (Batch translation handles up to 1000 documents per run): split the scope by folder or by selection.

## Related topics

- [Checking documents](../04-document-tools/check.md)
- [Creating a document from a template](../04-document-tools/templates.md)
- [Handing work to an AI](../05-ai/README.md)
