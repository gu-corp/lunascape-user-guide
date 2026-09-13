# Root dokumentasi dan konvensi berkas

Aturan yang diikuti Lunascape Docs saat menemukan dokumen dan menyusun INDEX. Sistem berkas itu sendiri yang menjadi sumber resmi, sehingga tidak diperlukan daftar induk maupun pengaturan build.

## Root dokumentasi

- Folder `docs` terdekat, atau folder yang memuat `lunascape-docs.json`, menjadi root dokumentasi.
- Jika ada `lunascape-docs.json`, nama foldernya tidak harus `docs`.
- Membuka berkas Markdown di luar root dokumentasi mana pun akan menampilkan foldernya sebagai root dokumentasi sementara.

## Berkas yang ditampilkan di INDEX

- Berkas `.md`, `.markdown`, dan `.mdx` ditampilkan. Berkas baru selalu muncul, meskipun tanpa front matter atau informasi navigasi.
- Folder yang diawali `.`, `node_modules`, serta folder yang tercantum pada `ignoredDirectories` (bawaan `99-archive`) tidak ditampilkan.
- Semua yang berada di bawah `i18n/` diperlakukan sebagai terjemahan dan tidak ditampilkan tersendiri di INDEX.

## Halaman sampul folder

- `README.md` yang memiliki isi (atau `index.md` bila tidak ada README) menjadi halaman sampul folder tersebut. Menekan nama folder di INDEX akan membukanya.
- `README.md` yang hanya berisi front matter tanpa isi diperlakukan sebagai "deskriptor khusus pengaturan" dan tidak ditampilkan sebagai halaman. Gunakan ini bila folder hanya perlu judul atau urutan.
- Bila `README.md` dan `index.md` sama-sama ada, `README.md` yang diutamakan.

## Bahasa bawaan dan terjemahan

- Dokumen dalam bahasa bawaan (dokumen kanonik) tetap berada di tempatnya.
- Terjemahan diletakkan di `i18n/<bahasa>/` pada folder yang sama dengan dokumen kanonik, dengan nama berkas yang sama. Menyusun ulang struktur folder di bawah `i18n/` tidak dikenali.
- Hanya dari satu lokasi itulah terjemahan dikenali. Berkas dengan nama sama yang diletakkan di tempat lain menjadi berkas terlantar yang tidak diakui sebagai terjemahan dokumen mana pun.

```text
docs/
  lunascape-docs.json
  README.md                  ← halaman sampul root dokumentasi (halaman awal)
  i18n/en/README.md          ← versi bahasa Inggrisnya
  01-product/
    README.md                ← halaman sampul folder
    requirements.md
    i18n/en/README.md        ← versi bahasa Inggris dari dua dokumen di atas
    i18n/en/requirements.md
  99-archive/                ← dikecualikan dari INDEX secara bawaan
```

## Tentang `_meta.json`

`_meta.json` milik Nextra tidak digunakan untuk navigasi. Berkas yang sudah ada tidak diubah maupun dihapus. Ke depannya, berkas tersebut hanya akan ditangani oleh fitur impor/ekspor yang eksplisit.

## Topik terkait

- [Mengatur informasi navigasi](navigation-metadata.md)
- [Pengaturan proyek](project-configuration.md)
- [Mengganti root dokumentasi](../02-reading/roots.md)
