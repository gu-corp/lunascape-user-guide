# Mengubah pengaturan tampilan

Melalui [Pengaturan tampilan] (roda gigi) di bilah alat, setiap pengguna dapat mengubah tampilan INDEX dan penampilan tombol edit.

1. Tekan [Pengaturan tampilan] di bilah alat.
2. Alihkan item yang ingin Anda ubah. Perubahan langsung diterapkan.
3. Tekan [Pengaturan tampilan] sekali lagi, atau tekan di luar panel, untuk menutupnya.

## Item yang dapat diatur

| Bagian | Item | Fungsi |
|---|---|---|
| Bahasa dokumen | (keadaan saat ini) | Menampilkan bahasa bawaan proyek dan bahasa yang sedang ditampilkan. [Atur bahasa proyek…] membuka pengaturan bahasa proyek |
| Konten | [Nama berkas] | Menampilkan nama berkas sebagai ganti nama dokumen |
| | [Ikon dokumen] | Menampilkan ikon pada item dokumen |
| | [Ikon folder] | Menampilkan ikon pada item folder |
| | [Jumlah isi folder] | Menampilkan jumlah dokumen yang ada di dalam folder |
| | [Panduan hierarki] | Menampilkan garis panduan yang menunjukkan hierarki |
| | [Sembunyikan jika dokumen hanya satu] | Pada root dokumentasi yang hanya berisi 1 dokumen, INDEX ditutup otomatis hanya pada pembukaan pertama |
| | [Ciutkan detail dokumen] | Menciutkan tabel pengelolaan di awal dokumen menjadi baris "Detail dokumen". Jika dimatikan, tabel ditampilkan apa adanya |
| | [Kerapatan tampilan] | Memilih jarak antarbaris INDEX dari [Standar] / [Ringkas] |
| | [Tombol edit] | Menampilkan [Edit] di kanan bawah isi dokumen |
| Tindakan | [Kembalikan ke bawaan proyek] | Menghapus semua perubahan pengguna dan kembali ke pengaturan proyek |
| | [Buka pengaturan ekstensi] | Membuka pengaturan Lunascape Docs di layar pengaturan VS Code |

> **Tips**
>
> - Pengaturan tampilan disimpan per pengguna dan per root dokumentasi, dan tidak ditulis ke berkas yang dikelola Git.
> - Pengaturan diprioritaskan dengan urutan "pengaturan tampilan pengguna → pengaturan VS Code → `lunascape-docs.json` → bawaan produk". Nilai bawaan bersama untuk tim ditentukan pada `tree` dan `editor` di `lunascape-docs.json`.

## Mengganti skema warna

Menekan pengalih tema (matahari／bulan) di bilah alat akan mengganti antara latar putih dan skema warna VS Code. Skema warna saat pertama dibuka ditentukan oleh pengaturan `lunascapeDocEditor.appearance` (`light` atau `auto`).

## Topik terkait

- [Menggunakan INDEX](index-panel.md)
- [Pengaturan proyek](../04-document-tools/project-configuration.md)
- [Daftar pengaturan VS Code](../08-reference/settings.md)
