# Checking documents

docs-lint checks heading structure, broken links, missing required documents and sections, inconsistent terminology, requirement ID consistency and more. A check always covers the whole documentation root.

## Run a check

1. Press [文書ツール] (Document Tools) in the toolbar and open the [チェック] (Check) tab.
2. Press [文書ルートを検証] (Validate documentation root).
   You can also run "Lunascape Docs: 文書ルートを検証" from the Command Palette.
3. Review the list of findings.

## Read the results

- [この文書] (This document) / [すべて] (All) above the list filter what is shown. The scope of the check itself is always the whole documentation root.
- Findings have four levels: error, warning, information and hint. [文書ツール] (Document Tools) in the toolbar shows the number of errors and warnings.
- Press a finding to open the corresponding position in the Markdown source in the VS Code editor.
- Findings that concern the whole documentation root (such as a missing test document) appear as "文書ルート全体" (Entire documentation root) items without a position.
- The same findings also appear in the VS Code Problems panel.

## What is checked

Press [ルールを確認・変更] (Review or change rules) to see the list of active checks and the purpose of each. The main ones are:

| Check | Meaning |
|---|---|
| 見出しの構成 (Heading structure) | There is exactly one H1 and heading levels do not skip |
| 内部リンク (Internal links) | Linked documents exist and stay inside the documentation root |
| コードブロックの言語 (Code block language) | Code blocks specify a language |
| 必要なフォルダーと文書 (Required folders and documents) | The folders and documents required by the Standard Pack profile exist |
| 文書に必要な章 (Required sections) | Each document type has its required sections |
| 用語の統一 (Terminology) | Discouraged expressions are flagged and preferred terms suggested |
| 要件IDの命名と重複 (Requirement ID naming and duplicates) | Requirement IDs follow the naming rule and are not defined twice |
| 要件IDの参照整合 (Requirement ID references) | Requirement IDs referenced from design, tests and status tables exist |
| 要件とテストの対応 (Requirements to tests) | Requirement IDs are referenced from test documents |

Which checks are active depends on the Standard Pack and profile selected in `lunascape-docs.json` and on `docs-lint.config.json`.

> **Note**
>
> - Changing a document or a setting marks the previous result as "revalidation required". Nothing passes automatically; press [文書ルートを検証] again.
> - Unsaved changes are not included in a check. Save first.
> - Checks run locally and deterministically. AI assessments and translation results never mix into check results.

## Related topics

- [Changing check rules](rules.md)
- [Project configuration](project-configuration.md)
- [Check, Create or Translation fails](../07-troubleshooting/tools.md)
