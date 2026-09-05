# AI settings

Choose the AI and the model that receive your work. This screen uses its own drop-downs, not the VS Code quick pick.

1. Press [文書ツール] (Document Tools) → the [AI] tab → [AI 設定…] (AI settings…).
2. Choose a provider under [プロバイダー].
   Providers this machine cannot use appear unselectable, with the reason.
3. Choose a model under [モデル]. The choices change per provider.
4. Close the screen. The choice is saved per user and reused next time.

## Providers

| Provider | Shape | Detection |
|---|---|---|
| Claude Code | Session | The `claude` command |
| Codex | Session | The `codex` command |
| VS Code language models | API | Models registered with the VS Code Language Model API |
| Anthropic API | API | A registered API key |
| OpenAI-compatible API | API | A registered API key and endpoint |

A **session** provider reads and writes files itself and runs the document check itself. Its results land in the working tree and are reviewed in the Git diff.

An **API** provider returns one document of Markdown, and the extension shows a diff before saving.

## Registering an API key

The Anthropic API and OpenAI-compatible APIs become usable once a key is registered.

1. Choose the provider under [プロバイダー]. The key field appears.
2. Enter the key under [API キー]. For an OpenAI-compatible API, also enter the [エンドポイント] (for example `https://api.openai.com/v1`).
3. Press [保存] (Save). "キー登録済み" (Key registered) is shown.

> **Note**
>
> - Keys live in VS Code's SecretStorage and are never shown again -- and never written to `settings.json` or any document. [キーを削除] (Delete key) removes one.
> - Model lists are fetched from each service with the registered key; a known list stands in until that answers.
> - An API provider can run only "Translate this page" and "Proofread this page". Walking many documents and creating documents are session work.

> **Hint**
>
> When no provider is found, install Claude Code or Codex, or register an API key. Reopen [AI 設定…] and it is detected.

## Related topics

- [Handing work to an AI](README.md)
- [VS Code settings](../08-reference/settings.md)
