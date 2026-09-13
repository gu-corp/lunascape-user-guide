# 项目设置

文档根目录下的 `lunascape-docs.json` 是团队共享的文档根目录设置，通过 Git 管理。

## 创建、编辑设置文件

- 按工具栏的 [文档工具] →[检查] 标签页 →[规则的来源与文档设置] →[编辑文档设置]，即可在 VS Code 中打开。文件不存在时，此时会创建初始文件。
- 文件名 `lunascape-docs.json` 会自动关联随附的 JSON Schema，从而显示输入补全和各项目的说明。无需编写 `$schema`。

## 设置示例

```json
{
  "id": "product-docs",
  "title": "产品文档",
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

## 项目说明

| 项目 | 内容 | 默认 |
|---|---|---|
| `id` | 保存各用户显示设置的键。想在移动文件夹后仍沿用设置时，指定一个固定的 ID | 文件夹的路径 |
| `title` | 显示在工具栏最左端和文档根目录列表中的名称。切换显示语言时不会改变 | 根目录 README/index 的标题，没有则为文件夹名 |
| `indexTitle` | INDEX 的标题 | `INDEX` |
| `startPage` | 最先打开的文档（相对于文档根目录的路径） | `README.md` |
| `appearance` | 配色。`light`（始终为浅色）或 `auto`（跟随 VS Code 的主题） | `light` |
| `defaultLocale` | 默认语言（正本的语言）。用 BCP 47 的语言标签（如 `ja`、`en`、`zh-Hant`）指定。作为翻译来源 | 未设置（根据正文推断显示） |
| `fallbackLocale` | 当阅读环境的语言与任何支持语言都不匹配时，首先向读者展示的语言。指定 `locales` 中包含的语言 | 未设置（使用 `defaultLocale`） |
| `locales` | 支持语言的列表。需包含 `defaultLocale`。作为语言菜单和翻译目标的候选 | 仅 `defaultLocale` |
| `ignoredDirectories` | 从 INDEX、搜索、检查中排除的文件夹名。指定后会替换默认值 | `["99-archive"]` |
| `tree` | INDEX 显示的默认值。用户可在显示设置中覆盖 | 如上例所示 |
| `editor.defaultMode` | 用户尚未切换时的编辑视图。`visual` 或 `source` | `visual` |
| `editor.showEditButton` | 是否在正文右下角显示 [编辑] | `true` |
| `documentStandards.pack` | 用于文档检查和模板的 Standard Pack。`builtin:<名称>`，或相对于文档根目录的路径 | 无 |
| `documentStandards.profile` | Pack 定义的配置文件名 | 无 |
| `translation.enabled` | 启用翻译草案的生成和批量翻译 | `true` |
| `translation.contextFiles` | 翻译时作为术语和文体参考传入的正本 Markdown（相对于文档根目录的路径） | `[]` |
| `translation.maxContextCharacters` | 参考文档合计字符数的上限（最大 1048576） | `49152` |
| `description` | 文档集合的一行说明。显示在仓库主页的卡片上。与 `title` 一样，可写为字符串或按语言区分的对象 | 无 |

## 告知仓库中文档所在的位置

放在仓库直属目录下的 `lunascape-docs.json`，可以写入的不是该文件夹的设置，而是**仓库的地图**。只要写入下列 3 个项目中的任意一个，它就成为地图，该文件夹本身也就不再是文档根目录。

| 项目 | 内容 | 默认 |
|---|---|---|
| `defaultFolder` | 文档位于哪个文件夹（相对于直属目录的路径）。所指向的位置不需要设置文件 | 无（使用 `docs`） |
| `roots` | 拥有多个文档集合时，它们的列表（相对于直属目录的路径，按显示顺序）。此时直属目录成为主页 | 无 |
| `excludes` | 从文档根目录发现中排除的文件夹（相对于直属目录的路径）。追加到 `node_modules` 等默认排除项之上 | `[]` |
| `home.cards` | 是否在主页 README 下方显示文档集合的卡片。若在 README 中自行编写链接，则设为 `false` | `true` |

文档根目录按以下顺序确定。从上到下，使用最先找到的那一个。

1. 在设置或命令中指定文件夹时，即该文件夹
2. 直属目录下 `lunascape-docs.json` 的 `defaultFolder` 或 `roots` 所指向的位置
3. 存在 `lunascape-docs.json` 的文件夹（若在同一父目录下有 2 个以上，则该父目录成为主页）
4. `docs` 文件夹（`lunascapeDocEditor.rootDirectoryNames`）
5. 仓库直属目录本身

> **提示**
>
> 若什么都不写，第 4 项就会生效，因此拥有一个 `docs/` 的普通仓库仍与以往一致。仅当想将文件夹名设为 `manual` 时，才编写 `defaultFolder`。

### 地图示例

```json
{
  "title": "Lunascape 帮助",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## 设置的优先级

与显示相关的项目，按以下顺序优先。

1. 用户的显示设置（[显示设置] 面板）
2. VS Code 的设置（`lunascapeDocEditor.*`）
3. `lunascape-docs.json`
4. 产品的默认值

只有语言（`defaultLocale`、`fallbackLocale`、`locales`）是例外，以 `lunascape-docs.json` 为正本。无法通过 VS Code 的个人设置覆盖项目的语言。

> **注意**
>
> 也可以在 `docs-lint.config.json` 中以 `standard` 指定 Standard Pack。两处都有时，以 `docs-lint.config.json` 为优先。

## 相关项目

- [更改检查规则](rules.md)
- [更改显示设置](../02-reading/display-settings.md)
- [VS Code 设置一览](../08-reference/settings.md)
