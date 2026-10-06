# Apakah Lunascape Docs

Lunascape Docs ialah alat untuk menggunakan dokumen Markdown dalam repositori Git terus sebagai “laman spesifikasi”. Binaan terlebih dahulu, pelayan dokumen dan pangkalan data khusus tidak diperlukan.

## Perkara yang boleh dilakukan

| Tujuan | Ciri utama |
|---|---|
| Membaca | INDEX (jadual kandungan), pautan dalam teks, jejak laluan, Kembali/Maju, kandungan dalam halaman, carian tapisan |
| Melihat | Jadual, blok kod, imej yang dilaraskan saiznya secara automatik, rumus matematik KaTeX, rajah Mermaid/Vega-Lite/Markmap/WaveDrom/Svgbob, paparan jadual kawalan dokumen yang dilipat |
| Menulis | Bertukar antara penyuntingan visual dan penyuntingan sumber Markdown; mencipta, menduplikasi, menamakan semula dan menyusun semula dari INDEX |
| Menyemak | Semakan dokumen dengan docs-lint, pengesahan dokumen, bab dan istilah wajib berdasarkan Standard Pack, penciptaan daripada templat |
| Menterjemah | Menjana cadangan terjemahan bagi setiap halaman atau secara pukal. Disimpan selepas disemak <!-- ai-only --> |
| Menggunakan daripada AI | Alat spesifikasi baca sahaja yang boleh dirujuk oleh ejen VS Code <!-- ai-only --> |

## Persekitaran yang boleh digunakan

| Persekitaran | Kegunaan |
|---|---|
| Sambungan VS Code | Membaca, menyunting, menyemak dan menterjemah repositori pada komputer anda. Bantuan ini memberi tumpuan kepadanya |
| Versi pelayar web | Membaca dokumen di GitHub (awam atau peribadi), draf pada peranti anda, membaca folder tempatan |
| Sambungan Chromium | Membuka versi pelayar web dalam tab pelayar |

## Prinsip asas

- **Markdown ialah dokumen kanonik.** Dokumen kekal sebagai fail Markdown yang diurus oleh Git. Lunascape Docs tidak menukarnya kepada format lain untuk disimpan.
- **Anda yang menentukan bila hendak menyimpan.** Suntingan ditulis ke fail hanya apabila anda menekan [Simpan]. Staging dan komit Git tidak dilakukan secara automatik.
- **Dokumen diproses pada peranti anda.** Dokumen tidak dihantar ke luar untuk dibaca atau disunting. Hanya semasa terjemahan, destinasi dan kandungan yang akan dihantar dipaparkan terlebih dahulu, dan dihantar selepas anda meluluskannya.
- **Terjemahan diletakkan di bawah `i18n/<locale>/`.** Dokumen dalam bahasa lalai kekal di tempat asalnya; terjemahan diletakkan dengan laluan relatif yang sama di bawah `i18n/en/` dan sebagainya.
- **AI hanya memberi cadangan.** Cadangan terjemahan disimpan selepas anda menyemak perbezaannya. Dokumen tidak akan ditulis semula tanpa pengetahuan anda. <!-- ai-only -->

## Topik berkaitan

- [Nama dan fungsi bahagian skrin](screen.md)
- [Memasang sambungan](install.md)
- [Operasi asas](../02-reading/README.md)
