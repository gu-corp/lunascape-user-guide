# Reading in another language

When a document has translations, you can switch languages from the language menu (globe) in the toolbar.

## Switch the language

1. Press the language menu in the toolbar.
   It shows the language of the current page and how it was determined (translation path, automatic detection, or the project default).
2. Choose the language you want to read.
   The translation of the same document opens. The choice is remembered, and the next document you open is shown in that language when a translation exists.

The list shows whether each language has a translation of this document.

| Label | Meaning |
|---|---|
| 翻訳あり (Translated) | A translation exists and can be opened |
| 翻訳なし (Not translated) | The language is supported by the project, but this document has no translation yet |
| 更新あり (Outdated) | A translation exists, but the source document changed after it was translated |

> **Note**
>
> - Choosing a language only opens an existing translation. It never generates a translation or creates a file. To create a translation, use [翻訳を作成・管理…] (Create or manage translations…) in the same menu.
> - When the language of the current page appears to differ from the project default, a warning is shown. The configuration is never rewritten.

## The language a document opens in

When you open a document root, the first display language is decided in this order.

1. The language you chose here before. Your choice is saved (choosing the default language is saved as a choice too).
2. The VS Code display language (in the Web viewer, the browser's language settings). A matching supported language is selected automatically; a regional tag such as `en-US` also matches its base language `en`.
3. The project's fallback language (`fallbackLocale` in `lunascape-docs.json`).
4. The project's default language.

> **Hint**
>
> - When the language was selected automatically, the current language in the language menu carries an 自動選択 (auto-selected) badge. Hover over it to see the reason.
> - `fallbackLocale` is the language shown to readers whose environment language matches none of the supported languages. On a project whose canonical language is Japanese with an English translation, setting `"en"` opens the English edition for, say, a Spanish-language environment. When unset, the default language is used.

## Where translations live

Default-language documents stay in place; a translation goes into an **`i18n/<locale>/` folder beside the document**, under the same file name.

```text
docs/
  README.md                  ← default language (for example Japanese)
  i18n/en/README.md          ← its English translation
  guide/
    setup.md
    i18n/en/setup.md         ← its English translation
```

> **Note**
>
> - Rebuilding the folder structure under `i18n/` (`i18n/en/guide/setup.md`) is not recognized. The `i18n/` folder always sits beside the document it translates.
> - That one location is the only place a translation is resolved from. Putting the same document's translation in a parent folder's `i18n/` as well creates no precedence contest: the parent-side copy simply becomes an orphan that neither the language menu nor the ledger ever sees (and is never deleted automatically). Keep each translation in one place.

## In the Web viewer

The Web viewer switches languages the same way when translations exist. To read a language that has no translation, use your browser's page translation. Code, math and diagrams are excluded from browser translation.

## Related topics

- [Handing work to an AI](../05-ai/README.md)
- [Available work](../05-ai/tasks.md)
- [Changing display settings](../02-reading/display-settings.md)
