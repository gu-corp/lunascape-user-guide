# 设置导航信息

INDEX 中显示的名称和顺序，写在各文档的 YAML front matter 中。即使不写，文档也会显示，此时使用标题（H1）和文件名顺序。

## 文档的名称和顺序

在文档的开头，按如下方式书写。

```yaml
---
navigation:
  title: 快速开始
  order: 200
---
```

| 项目 | 内容 |
|---|---|
| `navigation.title` | INDEX 中显示的名称。省略时使用 H1，若仍无则使用文件名 |
| `navigation.order` | 决定排序的整数，按从小到大排列。省略时采用稳定的默认排序（按文件名） |

> **提示**
>
> - `order` 以 100、200、300 这样每隔 100 设置，便于之后在中间插入 150 之类的值。
> - 即使存在未指定、非法或重复的 `order`，文档也不会被隐藏。
> - 在 INDEX 中重新排序时，会自动写入 `navigation.order`，无需手动书写。

## 文件夹的名称和顺序

文件夹的名称和顺序，由该文件夹的 `README.md`（若无则为 `index.md`）的 front matter 持有。封面页可以没有正文内容。

```yaml
---
navigation:
  title: 产品规划
  order: 100
---
```

没有封面页的文件夹，按文件夹名和默认顺序显示。在 INDEX 中更改标题或重新排序而有需要时，会创建仅含 front matter 的 `README.md`。仅浏览不会创建文件。

## 翻译版中的处理

- 顺序，以及文件夹的角色（封面页还是仅用于配置），仅由默认语言的文档决定。
- 翻译版只能覆盖 `navigation.title`。当正本文档有正文内容时，翻译版的 H1 也会用作名称。
- 仅有翻译版不会增加页面。

## 子项的排序与折叠

在文件夹的封面页中，定义了用于指定其直属子项排序方式和初始折叠状态的 `navigation.children.sort` 和 `navigation.children.defaultCollapsed`。在 VS Code 中读取和编辑将在后续支持。

## 相关项目

- [更改文档的排序](../03-editing/reorder.md)
- [文档根目录与文件规约](structure.md)
