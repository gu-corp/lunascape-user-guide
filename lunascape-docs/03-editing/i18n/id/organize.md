# Membuat dan menata dokumen serta folder

Dari menu item INDEX Anda dapat membuat, menduplikat, mengubah nama, dan menghapus dokumen serta folder. Masukan dilakukan di dialog kecil di dalam penampil, tanpa mengganggu pembacaan.

> **Catatan**
>
> Tindakan ini hanya tersedia bila ruang kerja tepercaya di VS Code. Tindakan tidak dapat dijalankan saat dokumen sedang disunting, saat operasi lain sedang diproses, atau saat objek sasaran memiliki perubahan yang belum disimpan.

## Membuat dokumen atau folder

1. Buka menu item ([⋯] atau klik kanan) pada folder tujuan.
   Untuk membuat langsung di bawah root dokumentasi, gunakan [⋯] di ujung kanan judul INDEX atau klik kanan bagian kosong pada INDEX.
2. Pilih [Dokumen baru] atau [Folder baru].
3. Masukkan nama, lalu tekan [Buat].
   Nama dokumen memerlukan ekstensi Markdown (`.md`, `.markdown`, `.mdx`, dan sejenisnya).

Dokumen baru dibuat sebagai dokumen bahasa bawaan (dokumen kanonik).

## Menduplikat dokumen

1. Buka menu item dokumen, lalu pilih [Duplikat].
2. Masukkan nama baru, lalu tekan [Buat].

Yang diduplikat hanya dokumen kanonik. Versi terjemahannya tidak ikut diduplikat.

## Mengubah judul

Mengubah judul dokumen (H1). Nama berkas tidak berubah.

1. Buka menu item dokumen atau folder, lalu pilih [Ubah judul].
2. Masukkan judul baru dalam satu baris, lalu tekan [Ubah].

Untuk folder, judul pada `README.md` folder tersebut yang diubah. Bila yang sedang ditampilkan adalah versi terjemahan, judul dokumen dalam bahasa itulah yang berubah.

## Mengubah nama dokumen

Mengubah nama dokumen yang tampil di bilah alat (nama root dokumentasi).

1. Klik kanan nama dokumen di bilah alat. Menu yang sama juga dapat dibuka dari [⋯] di ujung kanan judul INDEX.
2. Pilih [Ubah nama dokumen], lalu masukkan nama baru.

Selama belum diatur, nama folder ditampilkan apa adanya.

Nama yang diubah ditulis ke **tempat yang saat ini dipakai sebagai nama dokumen**, sehingga judul yang terlihat tidak pernah berakhir diabaikan.

| Keadaan saat ini | Ditulis ke |
|---|---|
| `lunascape-docs.json` memuat nama | `lunascape-docs.json` diperbarui |
| Tidak ada nama, tetapi root dokumentasi memiliki README | Judul (H1) pada README ditulis ulang |
| Keduanya tidak ada | `lunascape-docs.json` dibuat dan nama disimpan di sana |

Tempat penulisan tersebut ditampilkan pada pesan setelah perubahan.

> **Tips**
>
> Nama dokumen ditentukan dengan urutan ini: nama di `lunascape-docs.json`, lalu judul README root dokumentasi, lalu nama folder.

## Mengubah nama berkas atau folder

1. Buka menu item, lalu pilih [Ubah nama berkas] atau [Ubah nama folder].
2. Masukkan nama baru, lalu tekan [Ubah].

Versi terjemahan yang bersesuaian (jalur yang sama di bawah `i18n/<bahasa>/`) ikut diubah namanya.

## Menghapus

1. Buka menu item, lalu pilih [Pindahkan ke tempat sampah].
2. Periksa isi pesan konfirmasi, lalu setujui pemindahannya.

Objek sasaran dipindahkan ke tempat sampah sistem operasi, sehingga dapat dipulihkan bila perlu. Versi terjemahan tidak dihapus dan tetap ada.

## Nama yang tidak dapat digunakan

- Nama yang diawali `.` (karena tidak tampil di INDEX)
- `i18n` (dicadangkan untuk berkas terjemahan)
- Nama yang dicadangkan Windows (`CON`, `PRN`, dan sejenisnya)
- Nama yang diakhiri titik atau spasi
- Nama yang memuat karakter kontrol atau karakter yang tidak boleh dipakai pada nama berkas
- Nama yang sudah ada di folder yang sama (termasuk nama yang hanya berbeda huruf besar-kecil)

> **Catatan**
>
> Halaman awal (biasanya `README.md` di root) tidak dapat diubah namanya atau dipindahkan. Ubah dulu `startPage` di `lunascape-docs.json`.

## Topik terkait

- [Mengubah urutan dokumen](reorder.md)
- [Menggunakan INDEX](../02-reading/index-panel.md)
