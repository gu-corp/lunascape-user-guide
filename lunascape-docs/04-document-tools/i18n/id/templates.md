# Membuat dokumen dari templat

Di tab [Buat] pada Alat Dokumen, Anda dapat memilih templat, melihat pratinjau isinya, lalu membuat dokumen baru.

1. Tekan [Alat Dokumen] pada bilah alat, lalu buka tab [Buat].
2. Tekan [Buat dari templat], lalu pilih sebuah templat.
3. Isi kolom masukan (judul, ringkasan, dan sebagainya). Kolom yang wajib diisi ditandai dengan "Wajib".
4. Masukkan lokasi penyimpanan sebagai jalur relatif terhadap root dokumentasi (misalnya `03-design/api.md`).
5. Tekan [Pratinjau], lalu periksa Markdown yang dihasilkan.
6. Tekan [Buat dengan isi ini].
   Dokumen dibuat dan ditampilkan di penampil. Selanjutnya, pemeriksaan atas seluruh root dokumentasi dijalankan.

## Templat yang tersedia

| Templat | Isi |
|---|---|
| Dokumen satu halaman | Membuat spesifikasi singkat, catatan, atau dokumen penjelasan mandiri dalam satu berkas |
| Spesifikasi, manual, bantuan | Membuat satu berkas dengan susunan bab umum yang dapat dipakai untuk spesifikasi, manual, atau bantuan |
| Templat Standard Pack | Jika Standard Pack dipilih di `lunascape-docs.json`, jenis dokumen yang tersedia pada profil tersebut (dokumen definisi kebutuhan, dokumen desain, dan sebagainya) akan ditambahkan |

> **Perhatian**
>
> - Pembuatan memerlukan ruang kerja tepercaya.
> - Berkas yang sudah ada tidak akan ditimpa. Dokumen tidak dapat dibuat jika sudah ada dokumen dengan nama yang sama di lokasi penyimpanan.
> - Lokasi penyimpanan memerlukan ekstensi `.md` atau `.mdx`. Dokumen tidak dapat dibuat di bawah `i18n` (lokasi versi terjemahan).
> - Setelah mengubah masukan, tekan [Pratinjau] sekali lagi sebelum membuat dokumen.

> **Tips**
>
> Pada proyek yang belum memiliki folder dokumen, Anda dapat membuat satu set awal melalui "Lunascape Docs: Buat dokumen dari templat" di Command Palette. Lihat [Membuat dokumen pertama Anda](../01-introduction/first-documents.md).

## Topik terkait

- [Menggunakan Alat Dokumen](README.md)
- [Mengubah aturan pemeriksaan](rules.md)
