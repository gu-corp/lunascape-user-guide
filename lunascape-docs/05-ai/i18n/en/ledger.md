# The ledger and its records

The ledger at the top of the [AI] tab is the translation state of each supported language. It is useful without an AI: it says what is missing.

| Label | Meaning |
|---|---|
| 未訳 (Missing) | Documents with no translation yet |
| 要更新 (Outdated) | Documents whose translation exists but whose canonical document is newer than the record |
| 翻訳済み (Translated) | Translations that follow their canonical document |

The ledger is computed by walking the documentation root. No AI and no language model is involved.

## Update the translation records

Reporting "outdated" needs a record of the canonical document and the translation as they were when translated. A session provider writes files directly, so no record is created automatically.

1. When the translation is done and you have reviewed it, press [翻訳の記録を更新] (Update translation records).
2. Translations without a record are recorded as matching the current canonical document.

Claude Code sessions and API-provider saves record this automatically (a session is instructed to call the `record_translation_freshness` MCP tool). The button matters when you translated with Codex or the VS Code chat.

From then on, changing a canonical document marks its translation outdated.

> **Note**
>
> - Translations that already have a record are left alone, so an existing "outdated" state is never erased.
> - Records live in `.lunascape-docs/translation-freshness.json` and hold only relative paths, languages, content hashes and a timestamp -- never document text.

## Related topics

- [Available work](tasks.md)
- [Reading in another language](../02-reading/languages.md)
