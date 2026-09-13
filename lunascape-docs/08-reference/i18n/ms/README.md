# Spesifikasi utama

## Persekitaran pengendalian

| Persekitaran | Keperluan |
|---|---|
| Sambungan VS Code | VS Code 1.90 atau lebih baharu. Ciri yang melibatkan penulisan berfungsi dalam ruang kerja dipercayai |
| Versi pelayar web | Chrome, Edge, Safari atau Firefox terkini. Untuk melihat folder setempat, pelayar mesti menyokong pemilihan folder (File System Access API) |
| Sambungan Chromium | Manifest V3. Tiada kebenaran hos diminta |

## Dokumen yang disokong

| Perkara | Kandungan |
|---|---|
| Fail | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (jadual, senarai tugasan, blok kod, garis batal), imej setempat, YAML front matter |
| MDX | Hanya komponen yang dibenarkan dipaparkan. Skrip sewenang-wenangnya tidak dijalankan |
| HTML | Dipaparkan selepas dinyahbahaya dengan DOMPurify 3.4.14 |

## Rajah dan rumus matematik

| Jenis | Nama bahasa | Catatan |
|---|---|---|
| Rumus matematik | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Data terbenam sahaja. URL luaran dan tanda imej tidak dibenarkan |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | JSON ketat sahaja |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | Versi edaran memaparkan sumber dalam keadaan terlipat. Had: input 64 KiB, 15 saat, SVG 2 MiB |
| Penrose (eksperimen) | `penrose` | Pratetap `set-theory` sahaja |

## Nilai had

| Perkara | Nilai |
|---|---|
| Hasil pengembangan templat | 4 MiB |
| Konteks rujukan terjemahan | Lalai 49,152 aksara, maksimum 1,048,576 aksara |
| Sasaran satu larian terjemahan pukal | 1,000 dokumen |
| Lebar imej pilihan | 16–4096px |

## Fail

| Fail | Peranan | Diurus Git |
|---|---|---|
| `lunascape-docs.json` | Tetapan akar dokumentasi | Ya |
| `docs-lint.config.json` | Tetapan peraturan semakan | Ya |
| `.lunascape-docs/translation-freshness.json` | Rekod kesegaran terjemahan (laluan, bahasa, cincangan dan cap masa sahaja) | Ya |
| Tetapan dan keadaan ruang kerja VS Code | Tetapan paparan peribadi, pilihan penyedia, keadaan buka tutup INDEX | Tidak |

## Standard Pack yang disertakan

`builtin:gu-corp-software` — profil: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Topik berkaitan

- [Senarai tetapan VS Code](settings.md)
- [Keselamatan dan sempadan penyimpanan](security.md)
