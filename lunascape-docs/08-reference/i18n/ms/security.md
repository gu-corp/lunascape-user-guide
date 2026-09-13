# Keselamatan dan sempadan penyimpanan

Sempadan yang disediakan oleh Lunascape Docs untuk melindungi dokumen anda dan peranti anda.

## Paparan

- HTML yang dijana daripada Markdown dan SVG yang dijana daripada rajah dinyahbahaya dengan DOMPurify 3.4.14 sebelum dipaparkan.
- Skrip sewenang-wenangnya yang terkandung dalam MDX tidak dilaksanakan.
- KaTeX dijalankan dengan `trust: false`, `maxSize: 50` dan `maxExpand: 1000`, serta tidak mempercayai HTML luaran mahupun arahan sewenang-wenangnya.
- Pustaka pelukisan Markmap, WaveDrom, Svgbob, Vega-Lite dan Penrose dimuatkan dalam peranti pada versi yang ditetapkan, hanya apabila blok yang berkenaan ada. Rujukan kepada sumber luaran, HTML mentah dan notasi boleh laksana tidak dibenarkan, dan skrip, imej luaran, `link`, `style` serta `foreignObject` dibuang daripada SVG yang dijana.
- Pelukisan TikZ tidak melancarkan LaTeX pada hos, sebaliknya dijalankan satu demi satu dalam pekerja TeX WebAssembly yang mempunyai sistem fail dalam ingatan. Terdapat had pada input, baris gilir, ingatan, masa pelaksanaan (15 saat) dan output SVG, dan arahan I/O fail ditolak.

## Akses kepada dokumen dan fail

- Pautan dokumen dan operasi fail tidak boleh keluar daripada akar dokumentasi.
- Pembuatan, penamaan semula, pemindahan dan pemadaman daripada INDEX disahkan semula di pihak sambungan — akar dokumentasi, versi INDEX, laluan dokumen kanonik, jenis sasaran, sempadan pautan simbolik dan dokumen yang belum disimpan — sebelum digunakan. Permintaan operasi daripada menu lama atau daripada akar dokumentasi lain tidak digunakan.
- Operasi pengubahan INDEX dilumpuhkan semasa dokumen sedang disunting atau semasa operasi INDEX yang lain sedang digunakan.
- Pembuatan daripada templat mengesahkan semula kepercayaan ruang kerja, entiti sebenar akar dokumentasi, versi INDEX, Standard Pack dan kandungan yang dijana, destinasi penyimpanan serta sempadan pautan simbolik selepas pratonton. Fail sedia ada tidak ditulis ganti, dan kandungan yang berbeza daripada pratonton atau hasil pengembangan yang melebihi 4 MiB tidak dibuat.
- Penyimpanan fail tetapan memeriksa versinya sejurus sebelum disimpan, dan dibatalkan apabila perubahan luaran dikesan.

## Penghantaran ke luar

- Dokumen tidak pernah dihantar ke luar untuk tujuan paparan, penyuntingan atau semakan. Semakan dokumen dijalankan secara berketentuan dalam peranti.
- Hanya terjemahan (terjemahan halaman ini, terjemahan pukal) yang menghantar dokumen kepada model bahasa, setelah destinasi dan skop penghantaran dipaparkan terlebih dahulu dan hanya apabila diluluskan secara jelas. <!-- ai-only -->
- Cadangan terjemahan dipaparkan sebagai perbezaan, versi dokumen kanonik dan sasaran terjemahan disahkan semula, dan hanya digunakan apabila seseorang menyimpannya secara jelas. <!-- ai-only -->
- Alat spesifikasi untuk ejen AI tidak memulangkan teks dokumen, nama ruang kerja atau laluan setempat. <!-- ai-only -->

## Git

- Penyimpanan hanya menulis ke fail. Tiada ciri yang melakukan pementasan atau komit Git secara automatik.
- Fail sedia ada seperti `_meta.json` tidak dipadam atau diubah secara senyap. Versi terjemahan yang terpencil juga tidak dipadam atau dipindahkan secara automatik.

## Berkaitan

- [Spesifikasi utama](README.md)
- [Penggunaan daripada AI](ai-agents.md)
