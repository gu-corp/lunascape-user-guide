# 主要规格

## 运行环境

| 环境 | 要求 |
|---|---|
| VS Code 扩展 | VS Code 1.90 及以上版本。涉及写入的功能需在受信任的工作区中运行 |
| Web 浏览器版 | 较新版本的 Chrome、Edge、Safari、Firefox。浏览本地文件夹需使用支持文件夹选择（File System Access API）的浏览器 |
| Chromium 扩展 | Manifest V3。不请求主机权限 |

## 支持的文档

| 项目 | 内容 |
|---|---|
| 文件 | `.md`、`.markdown`、`.mdx` |
| Markdown | GitHub Flavored Markdown（表格、任务列表、代码块、删除线）、本地图片、YAML front matter |
| MDX | 仅显示允许的组件。不执行任意脚本 |
| HTML | 使用 DOMPurify 3.4.14 净化后显示 |

## 图与公式

| 种类 | 语言名 | 备注 |
|---|---|---|
| 公式 | `$...$`、`$$...$$`、`\(...\)`、`\[...\]` | KaTeX。`trust: false`、`maxSize: 50`、`maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | 仅支持内嵌数据。不支持外部 URL 和图片标记 |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | 仅支持严格的 JSON |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | 发行版中源代码以折叠形式显示。上限为输入 64 KiB、15 秒、SVG 2 MiB |
| Penrose（实验性） | `penrose` | 仅支持 `set-theory` 预设 |

## 上限值

| 项目 | 值 |
|---|---|
| 模板的展开结果 | 4 MiB |
| 翻译的参考上下文 | 默认 49,152 个字符，最大 1,048,576 个字符 |
| 批量翻译单次的对象数 | 1,000 个文档 |
| 图片的自定义宽度 | 16〜4096px |

## 文件

| 文件 | 作用 | Git 管理 |
|---|---|---|
| `lunascape-docs.json` | 文档根目录的设置 | 有 |
| `docs-lint.config.json` | 检查规则的设置 | 有 |
| `.lunascape-docs/translation-freshness.json` | 翻译时效性的记录（仅路径、语言、哈希值和日期时间） | 有 |
| VS Code 的设置与工作区状态 | 个人的显示设置、提供程序的选择、INDEX 的展开状态 | 无 |

## 随附的 Standard Pack

`builtin:gu-corp-software` — 配置文件：`base`、`web-application`、`api-service`、`regulated-financial-product`、`smart-contract`

## 相关项目

- [VS Code 设置一览](settings.md)
- [安全与保存边界](security.md)
