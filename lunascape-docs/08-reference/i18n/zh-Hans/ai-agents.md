# 从 AI 使用

扩展会向 VS Code 注册只读的 Language Model Tool `lunascape_getDocsSpecification`。当兼容的 VS Code 代理被问及 Lunascape Docs 的功能、设置或文档规约时，可以通过该工具获取本帮助的内容（通用规格说明）。

## 使用方法

在 VS Code 的聊天中带上 `#lunascapeDocs` 提问，或直接就 Lunascape Docs 的设置或文档结构提问。

```text
#lunascapeDocs 如何在 lunascape-docs.json 中启用英文翻译？
```

## 工具参数

| 参数 | 内容 |
|---|---|
| `topic` | 要获取的章节：`all`、`usage`（基本操作）、`structure`（文档根目录与文件规约）、`editing`（编辑文档）、`configuration`（项目设置）、`security`（安全与写入边界）、`ai`（从 AI 使用） |
| `locale` | 帮助的语言（`ja`、`en` 等，随附帮助的语言标签）。省略时使用 VS Code 的显示语言，否则返回日文帮助 |

> **注意**
>
> - 该工具不会将文档正文发送到外部。
> - 该工具不会返回工作区名称或本地路径。
> - 该工具不会修改文件。
> - 即使没有 `AGENTS.md`，也可以从兼容的 VS Code 代理使用。对于不使用扩展工具 API 的其他 AI 客户端，不会自动共享。

## 相关主题

- [显示帮助](../02-reading/help.md)
- [安全与写入边界](security.md)
