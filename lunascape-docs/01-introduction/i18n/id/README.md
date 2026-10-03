# Apa itu Lunascape Docs

Lunascape Docs adalah alat untuk menggunakan dokumen Markdown di repositori Git apa adanya sebagai "situs spesifikasi". Anda tidak memerlukan proses build terlebih dahulu, server dokumen, atau basis data khusus.

## Yang dapat dilakukan

| Tujuan | Fitur utama |
|---|---|
| Membaca | INDEX (daftar isi), tautan dalam teks, tautan jejak, Kembali/Maju, daftar isi dalam halaman, pencarian dengan filter |
| Melihat | Tabel, blok kode, gambar yang menyesuaikan ukuran otomatis, rumus KaTeX, diagram Mermaid/Vega-Lite/Markmap/WaveDrom/Svgbob, tabel pengendalian dokumen yang ditampilkan terlipat |
| Menulis | Beralih antara pengeditan visual dan pengeditan sumber Markdown; membuat, menduplikasi, mengganti nama, dan mengubah urutan dari INDEX |
| Memeriksa | Pemeriksaan dokumen dengan docs-lint, pemeriksaan dokumen, bab, dan istilah wajib berdasarkan Standard Pack, pembuatan dari templat |
| Menerjemahkan | Membuat usulan terjemahan per halaman atau sekaligus. Tinjau dahulu sebelum disimpan <!-- ai-only --> |
| Menggunakan dari AI | Alat spesifikasi hanya-baca yang dapat dirujuk oleh agen VS Code <!-- ai-only --> |

## Lingkungan yang dapat digunakan

| Lingkungan | Kegunaan |
|---|---|
| Ekstensi VS Code | Membaca, mengedit, memeriksa, dan menerjemahkan repositori di komputer Anda. Bantuan ini berfokus pada lingkungan ini |
| Versi peramban web | Membaca dokumen di GitHub (publik maupun privat), draf di perangkat, membaca folder lokal |
| Ekstensi Chromium | Membuka versi peramban web di tab peramban |

## Prinsip dasar

- **Markdown adalah dokumen kanonik.** Dokumen tetap berupa berkas Markdown yang dikelola dengan Git. Lunascape Docs tidak pernah mengonversinya ke format lain untuk disimpan.
- **Anda yang menyimpan.** Hasil pengeditan hanya ditulis ke berkas saat Anda menekan [Simpan]. Staging dan commit Git tidak pernah dilakukan secara otomatis.
- **Dokumen diproses di perangkat Anda.** Dokumen tidak pernah dikirim ke luar untuk dibaca atau diedit. Hanya saat menerjemahkan, tujuan dan isi kiriman ditampilkan terlebih dahulu, lalu dikirim setelah Anda menyetujuinya.
- **Terjemahan diletakkan di `i18n/<bahasa>/`.** Dokumen dalam bahasa bawaan tetap di tempatnya; terjemahan diletakkan dengan jalur relatif yang sama di `i18n/en/` dan seterusnya.
- **AI hanya sebatas mengusulkan.** Usulan terjemahan disimpan setelah Anda meninjau perbedaannya. Dokumen tidak pernah ditulis ulang tanpa sepengetahuan Anda. <!-- ai-only -->

## Topik terkait

- [Nama dan fungsi bagian layar](screen.md)
- [Memasang ekstensi](install.md)
- [Operasi dasar](../02-reading/README.md)
