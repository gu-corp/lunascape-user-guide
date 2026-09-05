# Handing work to an AI

Lunascape Docs does not call a language model. It prepares **context, tools and checks**, and leaves the translating, proofreading and authoring to the AI you already use.

## The idea

| What the product supplies | Contents |
|---|---|
| Context | The documentation conventions (where translations live, front matter, the document standard, the glossary) and the location of the target document |
| Working tools | The ledger of missing and outdated translations, reading and writing documents, creation from templates |
| Checks | docs-lint, and the coverage and freshness difference |

The instruction carries no document text: the AI reads the files, writes them, and verifies them itself.

## Hand work over

1. Press [文書ツール] (Document Tools) in the toolbar and open the [AI] tab.
2. Choose the work under [作業] (Task).
3. Fill in what it needs (target language, subject).
4. Press [この作業を渡す] (Hand this over).
   A VS Code terminal opens and the AI you chose takes the instruction and starts.

> **Hint**
>
> A Claude Code session travels with working tools (the `lunascape-docs` MCP server): it can fetch the missing/outdated list, run docs-lint, and record translation freshness by itself.

## Reviewing the result

| Provider shape | Where the result lands |
|---|---|
| Session (Claude Code, Codex) | Writes to the working tree. **Review it in the Git diff** |
| API (VS Code language models, Anthropic, OpenAI-compatible) | Returns one document at a time. Review it with [差分を開く] (Open diff), then write it with [保存] (Save) |

### Reviewing an API proposal

Running with an API provider delivers a proposal to the [AI] tab.

1. Press [差分を開く] (Open diff) and compare it with the current content.
2. Press [保存] (Save) to write it -- a translation also records its freshness -- or [破棄] (Discard) to drop it.
   Press [中止] (Cancel) to stop a generation midway.

> **Note**
>
> - Lunascape Docs never stages or commits in Git. Always review the diff.
> - Work cannot be handed over in an untrusted workspace, or while browsing a folder outside any documentation root.

## Related topics

- [Available work](tasks.md)
- [AI settings](settings.md)
- [The ledger and its records](ledger.md)
