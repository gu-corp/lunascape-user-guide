# Membuat dokumen pertama Anda

Pada proyek yang belum memiliki folder dokumentasi, Anda dapat membuat satu set dokumen awal dari Command Palette.

1. Buka folder proyek di VS Code dan percayai ruang kerjanya.
2. Jalankan "Lunascape Docs: Buat dokumentasi dari templat" dari Command Palette (`⇧⌘P` / `Ctrl+Shift+P`).
   Jika ruang kerja memiliki beberapa folder, pilih ruang kerja tempat dokumen akan dibuat.
3. Pilih struktur yang akan dibuat.
   - [Dokumen satu halaman]: struktur minimal yang hanya berisi `README.md`. Cocok untuk spesifikasi singkat, catatan, atau dokumen penjelasan mandiri.
   - [Set dokumentasi]: membuat halaman utama beserta halaman masuk untuk `specification/` (spesifikasi), `manual/` (manual), dan `help/` (bantuan).
4. Masukkan judul dokumentasi. Judul ini digunakan untuk README dan judul setiap dokumen.
5. Masukkan folder dokumentasi yang akan dibuat. Gunakan jalur relatif dari ruang kerja; bawaannya adalah `docs`.
6. Periksa daftar berkas yang akan dibuat, lalu tekan [Buat].
   Setelah pembuatan selesai, `README.md` yang baru akan terbuka di penampil.

> **Catatan**
>
> - Berkas yang sudah ada tidak akan ditimpa. Jika salah satu berkas yang akan dibuat sudah ada, tidak ada yang dibuat dan proses dibatalkan.
> - Pembuatan tidak dapat dilakukan di ruang kerja yang tidak tepercaya.

> **Tips**
>
> - Jika Anda sudah memiliki folder dokumentasi, langkah ini tidak diperlukan. Lanjutkan ke [Operasi dasar](../02-reading/README.md).
> - Seiring bertambahnya dokumen, Anda dapat menambahkan dokumen satu per satu dengan memilih templat dari tab [Buat] pada Alat Dokumen.

## Topik terkait

- [Membuat dokumen dari templat](../04-document-tools/templates.md)
- [Root dokumentasi dan konvensi berkas](../04-document-tools/structure.md)
