# 更改检查规则

您可以更改各检查项的通知级别（错误、警告、信息），也可以将其关闭。更改会保存到文档根目录的 `docs-lint.config.json` 中，并与团队共享。

## 更改通知级别

1. 按工具栏中的 [文档工具]，打开 [检查] 选项卡。
2. 按 [查看和更改规则]。
   检查项列表会在同一张卡片中展开。每个项目都会显示其用途，以及当前设置的来源（Project、Profile、Pack、Default）。
3. 选择要更改的项目的通知级别。
4. 按 [保存并重新检查]。
   设置会被保存，并使用新设置重新检查整个文档根目录。

| 选项 | 含义 |
|---|---|
| [标准设置（…）] | 删除覆盖设置，按配置文件、Standard Pack、默认值的顺序恢复为标准设置 |
| [不使用] | 不检查此项目 |
| [信息] / [警告] / [错误] | 以该通知级别报告 |

> **注意**
>
> - 保存需要受信任的工作区。
> - 保存的仅为各项目的通知级别。各项目的选项将保持不变。Standard Pack 和配置文件本身不在此界面中更改。
> - 如果在保存之前 `docs-lint.config.json` 已被外部更改，则保存会中止。请加载最新状态后重试。
> - 如果没有 `docs-lint.config.json`，保存时会创建该文件。

## 直接编辑配置文件

- 按 [打开详细设置]，即可在 VS Code 中打开 `docs-lint.config.json`。
- 打开 [规则的来源与文档设置]，按 [编辑文档设置]，即可在 VS Code 中打开 `lunascape-docs.json`。Standard Pack 和配置文件在此处选择。

这两个文件都可使用扩展内置的 JSON Schema 提供的输入补全和说明。

## Standard Pack 与配置文件

Standard Pack 是一套文档标准，汇总了所需的文档种类、章节结构、术语和模板。在 `lunascape-docs.json` 的 `documentStandards` 中选择。

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

内置的 Pack `builtin:gu-corp-software` 提供 `base`、`web-application`、`api-service`、`regulated-financial-product`、`smart-contract` 这几种配置文件。

## 相关主题

- [检查文档](check.md)
- [项目设置](project-configuration.md)
