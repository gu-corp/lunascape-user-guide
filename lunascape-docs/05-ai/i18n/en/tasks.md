# Available work

Choose under [作業] (Task) in the [AI] tab. Each one changes the instruction handed over and the check that follows.

| Work | Contents | Requires | API providers |
|---|---|---|---|
| このページを翻訳 (Translate this page) | Translates the current document into the chosen language | The document open, a target language | Yes |
| 未訳をまとめて翻訳 (Translate what is missing) | Translates the missing and outdated documents of the chosen language, in order | A target language | Session only |
| このページを校正 (Proofread this page) | Checks and corrects terminology, style and the sections the document standard requires | The document open | Yes |
| 新しい文書を作成 (Create a document) | Creates a document following the document standard and its templates | A subject (optional) | Session only |

## What the instruction carries

| No. | Contents |
|---|---|
| 1 | The documentation root, with an instruction to change nothing outside it |
| 2 | The default (canonical) language, and where translations live: an `i18n/<locale>/` folder beside the document |
| 3 | That `navigation.order` belongs to the canonical document only, and that a translation may override `navigation.title` alone |
| 4 | That requirement IDs, links, code, Mermaid, TeX and front matter structure must not change |
| 5 | The document standard and the glossary (`terminology` in `docs-lint.config.json`) |
| 6 | To run the document check afterwards, report the files changed, and perform no Git operations |

> **Hint**
>
> The targets of "Translate what is missing" come from the ledger, up to 200 documents per run. Run it again for the rest.

## Related topics

- [Handing work to an AI](README.md)
- [The ledger and its records](ledger.md)
