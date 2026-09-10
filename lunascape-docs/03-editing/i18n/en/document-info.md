# Showing document information

A "document-control table" at the top of a document (document ID, version, last update, status and so on) is shown while reading as a compact "文書情報" (Document information) row. The Markdown remains an ordinary table, so it also reads normally on GitHub.

## Conditions

Place a two-column table like the following immediately after the heading (H1).

```markdown
# Functional requirements

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- The table must contain a document ID row and several management fields.
- A table under a `## 文書管理` or `## Document information` heading is also recognized.
- Tables in the middle of the text, and ordinary "item/value" tables, are not converted.

## How it is shown

- While reading, only the status and last update are shown in small type.
- Press the row to show every field.
- When printing, every field is shown.
- In the editor the table appears as a normal table and can be edited as such.

> **Hint**
>
> To always show the table instead of collapsing it, turn off [文書情報を折りたたむ] (Collapse document information) in [表示設定] (Display settings).

## Related topics

- [Editing a document](README.md)
- [Changing display settings](../02-reading/display-settings.md)
