# Apa itu Lunascape Docs

Lunascape Docs adalah alat untuk memperlakukan dokumen Markdown yang ada di repositori Git apa adanya sebagai "situs spesifikasi". Tidak diperlukan proses build sebelumnya, server dokumentasi, maupun basis data khusus.

## Yang bisa dilakukan

| Tujuan | Fitur utama |
|---|---|
| Membaca | INDEX (daftar isi), tautan dalam teks, tautan jejak, Kembali/Maju, daftar isi halaman, pencarian penyaring |
| Melihat | Tabel, blok kode, penyesuaian gambar otomatis, rumus KaTeX, diagram Mermaid, Vega-Lite, Markmap, WaveDrom, dan Svgbob, serta tampilan terlipat tabel pengelolaan dokumen |
| Menulis | Beralih antara penyuntingan visual dan penyuntingan sumber Markdown; membuat, menggandakan, mengganti nama, dan mengubah urutan dari INDEX |
| Memeriksa | Pemeriksaan dokumen dengan docs-lint, pemeriksaan dokumen, bab, dan istilah wajib berdasarkan Standard Pack, pembuatan dari templat |
| Menerjemahkan | Membuat usulan terjemahan per halaman atau sekaligus. Disimpan setelah Anda periksa <!-- ai-only --> |
| Menggunakan dari AI | Alat spesifikasi hanya-baca yang dapat dirujuk oleh agen VS Code <!-- ai-only --> |

## Lingkungan yang tersedia

| Lingkungan | Kegunaan |
|---|---|
| Ekstensi VS Code | Membaca, menyunting, memeriksa, dan menerjemahkan repositori di perangkat Anda. Bantuan ini berpusat pada lingkungan ini |
| Versi peramban web | Membaca dokumen di GitHub (publik maupun non-publik), draf di dalam perangkat, membaca folder lokal |
| Ekstensi Chromium | Membuka versi peramban web di tab peramban |
| Peramban Lunascape | Direncanakan untuk menyertakan model dokumen yang sama |

## Pemikiran dasar

- **Markdown adalah dokumen kanonik.** Dokumen tetap berupa berkas Markdown yang dikelola dengan Git. Lunascape Docs tidak mengubahnya ke format lain lalu menyimpannya.
- **Penyimpanan dilakukan oleh pengguna.** Isi yang Anda sunting ditulis ke berkas hanya ketika Anda menekan [Simpan]. Staging dan commit Git tidak dilakukan secara otomatis.
- **Dokumen diproses di dalam perangkat.** Dokumen tidak dikirim ke luar untuk keperluan membaca atau menyunting. Hanya pada saat penerjemahan, tujuan pengiriman dan isinya ditampilkan lebih dahulu, lalu dikirim setelah Anda menyetujuinya.
- **Versi terjemahan diletakkan di `i18n/<bahasa>/`.** Dokumen dalam bahasa bawaan tetap di tempatnya, sedangkan versi terjemahan diletakkan dengan jalur relatif yang sama di `i18n/en/` dan seterusnya.
- **AI hanya sebatas mengusulkan.** Usulan terjemahan disimpan setelah Anda memeriksa perbedaannya. Dokumen tidak akan diubah tanpa sepengetahuan Anda. <!-- ai-only -->

## Topik terkait

- [Nama dan fungsi bagian-bagian layar](screen.md)
- [Memasang ekstensi](install.md)
- [Operasi dasar](../02-reading/README.md)
