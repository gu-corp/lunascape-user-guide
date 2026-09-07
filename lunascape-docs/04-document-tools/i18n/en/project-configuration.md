# Project configuration

`lunascape-docs.json` directly under the documentation root holds the team-shared configuration of that root. It is managed in Git.

## Create or edit the configuration file

- Press [文書ツール] (Document Tools) in the toolbar → the [チェック] (Check) tab → [ルールの提供元と文書設定] (Rule sources and document settings) → [文書設定を編集] (Edit document settings) to open the file in VS Code. If the file does not exist, an initial file is created at that moment.
- The file name `lunascape-docs.json` is automatically associated with the bundled JSON Schema, which provides completion and a description for every field. A `$schema` entry is not needed.

## Example

```json
{
  "id": "product-docs",
  "title": "Product documentation",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Fields

| Field | Meaning | Default |
|---|---|---|
| `id` | The key under which per-user display settings are stored. Give it a fixed value to keep settings when the folder moves | The folder path |
| `title` | The name shown at the far left of the toolbar and in the documentation-root list. It does not change with the display language | The heading of the root README/index, otherwise the folder name |
| `indexTitle` | The heading of the INDEX | `INDEX` |
| `startPage` | The document opened first (relative to the documentation root) | `README.md` |
| `appearance` | Color theme: `light` (always light) or `auto` (follow the VS Code theme) | `light` |
| `defaultLocale` | The default language (the language of the canonical documents) as a BCP 47 tag such as `ja`, `en` or `zh-Hant`. It is the translation source | Unset (inferred from the text for display only) |
| `fallbackLocale` | The language first shown to readers whose environment language matches none of the supported languages. Name a language contained in `locales` | Unset (`defaultLocale` is used) |
| `locales` | The supported languages, including `defaultLocale`. They appear in the language menu and are the translation targets | `defaultLocale` only |
| `ignoredDirectories` | Folder names excluded from the INDEX, search and checks. Specifying it replaces the default | `["99-archive"]` |
| `tree` | Defaults for how the INDEX is displayed. Users can override them in Display settings | As in the example above |
| `editor.defaultMode` | The editing view used until a user switches: `visual` or `source` | `visual` |
| `editor.showEditButton` | Whether [編集] (Edit) is shown at the bottom right of the document | `true` |
| `documentStandards.pack` | The Standard Pack used for checks and templates: `builtin:<name>` or a path relative to the documentation root | None |
| `documentStandards.profile` | A profile name defined by the pack | None |
| `translation.enabled` | Enables translation proposals and batch translation | `true` |
| `translation.contextFiles` | Canonical Markdown files (relative to the documentation root) passed to translation as terminology and style references | `[]` |
| `translation.maxContextCharacters` | Upper limit on the total size of reference documents (maximum 1048576) | `49152` |
| `description` | A line about the documentation set, shown on the cards of a repository home. Like `title`, a string or an object per language | None |

## Say where the documents are

A `lunascape-docs.json` at the top of a repository can hold a **map of the repository** rather than settings for that folder. Writing any of the first two fields below makes it a map, and the folder holding it is then not a documentation root itself.

| Field | What it does | Default |
|---|---|---|
| `defaultFolder` | Which folder holds the documents (a path relative to this folder). The folder it names needs no configuration of its own | None (`docs` applies) |
| `roots` | The documentation sets, when there are several (paths relative to this folder, in display order). This folder then becomes the home | None |
| `excludes` | Folders to keep out of root discovery (paths relative to this folder). Added to the built-in exclusions such as `node_modules` | `[]` |
| `home.cards` | Whether a home shows the cards for its sets under its README. Set it to `false` if you write the links yourself | `true` |

A documentation root is found in this order, first match wins.

1. A folder named by a setting or by the command you ran
2. Whatever `defaultFolder` or `roots` points at in the `lunascape-docs.json` at the top
3. A folder that has a `lunascape-docs.json` (two or more under a common parent make that parent a home)
4. A folder named `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. The top of the repository itself

> **Tip**
>
> With nothing written, step 4 applies, so an ordinary repository with a single `docs/` behaves exactly as before. Write `defaultFolder` only when the folder is called something else, such as `manual`.

### An example map

```json
{
  "title": "Lunascape Help",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Precedence

Display-related fields apply in this order.

1. The user's display settings (the [表示設定] (Display settings) panel)
2. VS Code settings (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Product defaults

Languages (`defaultLocale`, `fallbackLocale`, `locales`) are the exception: `lunascape-docs.json` is authoritative. Personal VS Code settings cannot override the project languages.

> **Note**
>
> A Standard Pack can also be specified as `standard` in `docs-lint.config.json`. When both are present, `docs-lint.config.json` wins.

## Related topics

- [Changing check rules](rules.md)
- [Changing display settings](../02-reading/display-settings.md)
- [VS Code settings](../08-reference/settings.md)
