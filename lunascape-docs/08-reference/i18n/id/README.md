# Spesifikasi utama

## Lingkungan yang didukung

| Lingkungan | Persyaratan |
|---|---|
| Ekstensi VS Code | VS Code 1.90 atau yang lebih baru. Fitur yang menulis berkas berjalan pada ruang kerja tepercaya |
| Versi peramban web | Chrome, Edge, Safari, atau Firefox versi terbaru. Untuk membuka folder lokal, diperlukan peramban yang mendukung pemilihan folder (File System Access API) |
| Ekstensi Chromium | Manifest V3. Tidak meminta izin host |

## Dokumen yang didukung

| Item | Keterangan |
|---|---|
| Berkas | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tabel, daftar tugas, blok kode, coretan), gambar lokal, YAML front matter |
| MDX | Hanya komponen yang diizinkan yang ditampilkan. Skrip sembarang tidak dijalankan |
| HTML | Ditampilkan setelah dibersihkan dengan DOMPurify 3.4.14 |

## Diagram dan rumus

| Jenis | Nama bahasa | Catatan |
|---|---|---|
| Rumus | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Hanya data tertanam. URL eksternal dan tanda gambar tidak didukung |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Hanya JSON yang ketat |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | Pada versi distribusi, sumbernya ditampilkan terlipat. Batas: masukan 64 KiB, 15 detik, SVG 2 MiB |
| Penrose (eksperimental) | `penrose` | Hanya prasetel `set-theory` |

## Nilai batas

| Item | Nilai |
|---|---|
| Hasil perluasan templat | 4 MiB |
| Konteks rujukan terjemahan | Bawaan 49.152 karakter, maksimum 1.048.576 karakter |
| Sasaran satu kali terjemahan massal | 1.000 dokumen |
| Lebar gambar pilihan sendiri | 16–4096px |

## Berkas

| Berkas | Peran | Dikelola Git |
|---|---|---|
| `lunascape-docs.json` | Pengaturan root dokumentasi | Ya |
| `docs-lint.config.json` | Pengaturan aturan pemeriksaan | Ya |
| `.lunascape-docs/translation-freshness.json` | Catatan kesegaran terjemahan (hanya jalur, bahasa, hash, dan tanggal-waktu) | Ya |
| Pengaturan dan status ruang kerja VS Code | Pengaturan tampilan pribadi, pilihan penyedia, status buka-tutup INDEX | Tidak |

## Standard Pack yang disertakan

`builtin:gu-corp-software` — profil: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Topik terkait

- [Daftar pengaturan VS Code](settings.md)
- [Keamanan dan batas penyimpanan](security.md)
