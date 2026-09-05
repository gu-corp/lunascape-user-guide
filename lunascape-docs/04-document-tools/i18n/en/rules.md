# Changing check rules

You can change the notification level (error, warning, information) of each check, or turn a check off. Changes are saved to `docs-lint.config.json` in the documentation root and shared with the team.

## Change a notification level

1. Press [文書ツール] (Document Tools) in the toolbar and open the [チェック] (Check) tab.
2. Press [ルールを確認・変更] (Review or change rules).
   The list of checks expands inside the same card. Each check shows its purpose and where its current setting comes from (Project, Profile, Pack or Default).
3. Choose the notification level of the check you want to change.
4. Press [保存して再チェック] (Save and re-check).
   The setting is saved and the whole documentation root is checked again with the new configuration.

| Option | Meaning |
|---|---|
| [標準設定（…）] (Default (…)) | Removes the override and returns to the standard setting resolved from the profile, the Standard Pack and the default, in that order |
| [使わない] (Off) | Does not run this check |
| [情報] (Information) / [警告] (Warning) / [エラー] (Error) | Reports at this level |

> **Note**
>
> - Saving requires a trusted workspace.
> - Only the notification level of each check is saved. Per-check options are kept as they are. The Standard Pack and profile themselves are not changed from this screen.
> - If `docs-lint.config.json` was changed externally just before saving, the save is aborted. Reload the latest state and try again.
> - If `docs-lint.config.json` does not exist, it is created when you save.

## Edit the configuration files directly

- [詳細設定を開く] (Open advanced settings) opens `docs-lint.config.json` in VS Code.
- Expand [ルールの提供元と文書設定] (Rule sources and document settings) and press [文書設定を編集] (Edit document settings) to open `lunascape-docs.json` in VS Code. The Standard Pack and profile are chosen there.

Both files come with completion and descriptions from the JSON Schemas bundled with the extension.

## Standard Packs and profiles

A Standard Pack is a documentation standard that bundles required document types, section structures, terminology and templates. Select one with `documentStandards` in `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

The bundled pack `builtin:gu-corp-software` provides the profiles `base`, `web-application`, `api-service`, `regulated-financial-product` and `smart-contract`.

## Related topics

- [Checking documents](check.md)
- [Project configuration](project-configuration.md)
