# Apa itu Lunascape Docs

Lunascape Docs ialah alat untuk menggunakan dokumen Markdown yang disimpan dalam repositori Git terus sebagai "tapak spesifikasi". Tiada binaan awal, pelayan dokumentasi atau pangkalan data khusus yang diperlukan.

## Apa yang boleh anda lakukan

| Tujuan | Fungsi utama |
|---|---|
| Membaca | INDEX (senarai kandungan), pautan dalam teks, jejak laluan, undur dan maju, senarai kandungan dalam halaman, carian penapisan |
| Melihat | Jadual, blok kod, imej yang dimuatkan secara automatik, rumus matematik KaTeX, rajah Mermaid, Vega-Lite, Markmap, WaveDrom dan Svgbob, paparan terlipat jadual pengurusan dokumen |
| Menulis | Bertukar antara penyuntingan visual dan penyuntingan sumber Markdown; cipta, salin, namakan semula dan susun semula daripada INDEX |
| Memastikan | Semakan dokumen dengan docs-lint, pengesahan dokumen, bab dan istilah wajib berdasarkan Standard Pack, penciptaan daripada templat |
| Menterjemah | Penjanaan cadangan terjemahan bagi satu halaman atau secara pukal. Semak dahulu sebelum menyimpan <!-- ai-only --> |
| Menggunakan daripada AI | Alat spesifikasi baca sahaja yang boleh dirujuk oleh ejen VS Code <!-- ai-only --> |

## Persekitaran yang boleh digunakan

| Persekitaran | Kegunaan |
|---|---|
| Sambungan VS Code | Membaca, menyunting, menyemak dan menterjemah repositori pada mesin anda. Bantuan ini berpusat padanya |
| Versi pelayar web | Membaca dokumen di GitHub (awam atau persendirian), draf dalam peranti, membaca folder setempat |
| Sambungan Chromium | Membuka versi pelayar web dalam tab pelayar |
| Pelayar Lunascape | Model dokumen yang sama akan diterapkan |

## Pemikiran asas

- **Markdown ialah dokumen kanonik.** Dokumen kekal sebagai fail Markdown yang diurus dengan Git. Lunascape Docs tidak menukarnya kepada format lain untuk disimpan.
- **Penyimpanan dilakukan oleh pengguna.** Kandungan yang disunting ditulis ke fail hanya apabila anda menekan [Simpan]. Pementasan dan komit Git tidak dilakukan secara automatik.
- **Dokumen diproses dalam peranti.** Dokumen tidak dihantar ke luar untuk dibaca atau disunting. Hanya ketika terjemahan, destinasi dan kandungan dipaparkan terlebih dahulu, dan penghantaran dilakukan selepas kelulusan.
- **Versi terjemahan diletakkan dalam `i18n/<bahasa>/`.** Dokumen dalam bahasa lalai kekal di tempatnya, manakala versi terjemahan diletakkan dengan laluan relatif yang sama dalam `i18n/en/` dan seumpamanya.
- **AI hanya mencadangkan.** Cadangan terjemahan disimpan selepas anda menyemak perbezaannya. Dokumen tidak ditulis semula secara senyap. <!-- ai-only -->

## Berkaitan

- [Nama dan fungsi setiap bahagian skrin](screen.md)
- [Memasang sambungan](install.md)
- [Operasi asas](../02-reading/README.md)
