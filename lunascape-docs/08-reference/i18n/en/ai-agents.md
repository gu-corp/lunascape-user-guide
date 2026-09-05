# Use from AI agents

The extension registers the read-only Language Model Tool `lunascape_getDocsSpecification` with VS Code. When a compatible VS Code agent is asked about Lunascape Docs features, configuration or document conventions, it can fetch the content of this help (the general specification) through the tool.

## How to use it

Ask in VS Code chat with `#lunascapeDocs`, or simply ask about Lunascape Docs configuration or document structure.

```text
#lunascapeDocs How do I enable English translations in lunascape-docs.json?
```

## Tool arguments

| Argument | Meaning |
|---|---|
| `topic` | The section to fetch: `all`, `usage` (Basic operations), `structure` (Documentation roots and file conventions), `editing` (Editing a document), `configuration` (Project configuration), `security` (Security and write boundaries) or `ai` (Use from AI agents) |
| `locale` | The help language (`ja` or `en`). When omitted, the VS Code display language is used, falling back to the Japanese help |

> **Note**
>
> - The tool never sends document content anywhere.
> - The tool never returns workspace names or local paths.
> - The tool never modifies files.
> - It works from compatible VS Code agents without an `AGENTS.md`. It is not shared automatically with other AI clients that do not use the extension's tool API.

## Related topics

- [Showing this help](../02-reading/help.md)
- [Security and write boundaries](security.md)
