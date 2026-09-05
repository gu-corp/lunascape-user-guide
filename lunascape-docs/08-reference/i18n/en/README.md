# Specifications

## Requirements

| Surface | Requirements |
|---|---|
| VS Code extension | VS Code 1.90 or later. Features that write files require a trusted workspace |
| Web viewer | Recent Chrome, Edge, Safari or Firefox. Opening a local folder requires a browser that supports folder selection (File System Access API) |
| Chromium extension | Manifest V3. No host permissions are requested |

## Supported documents

| Item | Details |
|---|---|
| Files | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tables, task lists, code blocks, strikethrough), local images, YAML front matter |
| MDX | Only allowlisted components are rendered. Arbitrary scripts are never executed |
| HTML | Sanitized with DOMPurify 3.4.14 before display |

## Diagrams and math

| Kind | Language name | Notes |
|---|---|---|
| Math | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX with `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Embedded data only. No external URLs or image marks |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Strict JSON only |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | Collapsed source in the distributed build. Limits: 64 KiB input, 15 seconds, 2 MiB SVG |
| Penrose (experimental) | `penrose` | `set-theory` preset only |

## Limits

| Item | Value |
|---|---|
| Rendered template size | 4 MiB |
| Translation reference context | 49,152 characters by default, 1,048,576 at most |
| Documents per batch translation run | 1,000 |
| Custom image width | 16–4096px |

## Files

| File | Role | In Git |
|---|---|---|
| `lunascape-docs.json` | Documentation root configuration | Yes |
| `docs-lint.config.json` | Check rule configuration | Yes |
| `.lunascape-docs/translation-freshness.json` | Translation freshness records (paths, languages, hashes and timestamps only) | Yes |
| VS Code settings and workspace state | Personal display settings, provider choice, INDEX expansion state | No |

## Bundled Standard Pack

`builtin:gu-corp-software` — profiles: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Related topics

- [VS Code settings](settings.md)
- [Security and write boundaries](security.md)
