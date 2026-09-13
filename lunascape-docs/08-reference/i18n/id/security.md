# Keamanan dan batas penyimpanan

Batas-batas yang diterapkan Lunascape Docs untuk melindungi dokumen dan perangkat Anda.

## Tampilan

- HTML yang dihasilkan dari Markdown dan SVG yang dihasilkan dari diagram dibersihkan dengan DOMPurify 3.4.14 sebelum ditampilkan.
- Skrip sembarang yang ada di dalam MDX tidak dijalankan.
- KaTeX dijalankan dengan `trust: false`, `maxSize: 50`, dan `maxExpand: 1000`, serta tidak memercayai HTML eksternal maupun perintah sembarang.
- Pustaka penggambar Markmap, WaveDrom, Svgbob, Vega-Lite, dan Penrose dimuat di dalam perangkat pada versi yang dipatok, hanya ketika blok yang bersesuaian ada. Rujukan ke sumber daya eksternal, HTML mentah, dan notasi yang dapat dieksekusi tidak diizinkan; skrip, gambar eksternal, `link`, `style`, dan `foreignObject` dihapus dari SVG yang dihasilkan.
- Penggambaran TikZ tidak menjalankan LaTeX milik host. Penggambaran berjalan berurutan di dalam pekerja TeX WebAssembly dengan sistem berkas dalam memori, dengan batas pada masukan, antrean, memori, waktu eksekusi (15 detik), dan keluaran SVG, serta menolak instruksi I/O berkas.

## Akses ke dokumen dan berkas

- Tautan dokumen dan operasi berkas tidak dapat keluar dari root dokumentasi.
- Pembuatan, penggantian nama, pemindahan, dan penghapusan dari INDEX diperiksa ulang di sisi ekstensi — root dokumentasi, revisi INDEX, jalur dokumen kanonik, jenis sasaran, batas tautan simbolik, dan dokumen yang belum disimpan — sebelum diterapkan. Permintaan operasi dari menu yang usang atau dari root dokumentasi lain tidak diterapkan.
- Operasi pengubahan INDEX dinonaktifkan selama dokumen sedang disunting atau selama operasi INDEX lain sedang diterapkan.
- Pembuatan dari templat memeriksa ulang kepercayaan ruang kerja, identitas root dokumentasi, revisi INDEX, Standard Pack dan isi yang dihasilkan, lokasi penyimpanan, serta batas tautan simbolik setelah pratinjau. Pembuatan tidak menimpa berkas yang sudah ada dan tidak membuat isi yang berbeda dari pratinjau atau hasil pengembangan yang melebihi 4 MiB.
- Penyimpanan berkas pengaturan memeriksa revisinya tepat sebelum disimpan dan dibatalkan jika terdeteksi perubahan dari luar.

## Pengiriman ke luar

- Dokumen tidak pernah dikirim ke luar untuk keperluan menampilkan, menyunting, atau pemeriksaan. Pemeriksaan dokumen dijalankan di dalam perangkat secara deterministik.
- Hanya terjemahan (terjemahan halaman ini dan terjemahan sekaligus) yang mengirim dokumen ke model bahasa, setelah menampilkan tujuan dan cakupan pengiriman terlebih dahulu dan hanya bila disetujui secara eksplisit. <!-- ai-only -->
- Usulan terjemahan disajikan sebagai perbedaan; revisi dokumen kanonik dan dokumen sasaran diperiksa ulang, dan usulan hanya diterapkan bila seseorang menyimpannya secara eksplisit. <!-- ai-only -->
- Alat spesifikasi untuk agen AI tidak mengembalikan isi dokumen, nama ruang kerja, maupun jalur lokal. <!-- ai-only -->

## Git

- Penyimpanan hanya menulis ke berkas. Tidak ada fitur yang melakukan staging atau commit Git secara otomatis.
- Berkas yang sudah ada seperti `_meta.json` tidak pernah dihapus atau diubah secara diam-diam. Versi terjemahan yang terlantar juga tidak dihapus atau dipindahkan secara otomatis.

## Topik terkait

- [Spesifikasi utama](README.md)
- [Penggunaan dari AI](ai-agents.md)
