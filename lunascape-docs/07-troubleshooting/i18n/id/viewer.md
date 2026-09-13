# Dokumen tidak ditampilkan

## Muncul pesan "Tidak ditemukan Markdown atau folder docs yang dapat dibuka"

- Ruang kerja tidak memiliki folder `docs`, atau menggunakan nama selain `docs`.
  - Jika `lunascape-docs.json` diletakkan di folder tersebut, folder itu dikenali sebagai root dokumentasi terlepas dari namanya.
  - Atau, tambahkan nama folder ke pengaturan `lunascapeDocEditor.rootDirectoryNames`.
- Jika belum ada dokumen, buat dengan "Lunascape Docs: Buat dokumen dari templat".
- Cara lain, buka file Markdown di editor, lalu jalankan "Lunascape Docs: Buka di Penampil Spesifikasi".

## Dokumen tidak muncul di INDEX

- Pastikan ekstensinya `.md`, `.markdown`, atau `.mdx`.
- Folder berikut tidak ditampilkan: folder yang diawali `.`, `node_modules`, dan folder yang ditentukan di `ignoredDirectories` (bawaannya `99-archive`).
- Versi terjemahan di bawah `i18n/` tidak ditampilkan tersendiri di INDEX. Beralihlah melalui menu bahasa.
- Jika file yang baru ditambahkan tidak muncul, tekan [Muat ulang].
- Anda mungkin sedang melihat root dokumentasi lain. Periksa nama root dokumentasi di ujung kiri bilah alat.

## Folder ditekan, tetapi tidak ada yang ditampilkan

`README.md` pada folder tersebut adalah "deskriptor khusus pengaturan" yang hanya berisi front matter tanpa isi. Buka folder di INDEX, lalu pilih dokumen di dalamnya.

## Root dokumentasi yang terbuka bukan yang dimaksud

- Jika pengaturan `lunascapeDocEditor.rootMode` bernilai `fixed`, yang selalu terbuka adalah `lunascapeDocEditor.root`.
- Pada `auto`, root dokumentasi yang paling dekat dengan file Markdown yang dibuka akan dipilih. Anda dapat beralih melalui menu turun di ujung kiri bilah alat.

## Nama root dokumentasi berbeda dari yang diharapkan

Nama ditentukan berurutan dari `title` di `lunascape-docs.json` → `navigation.title` pada `README.md` root → H1 miliknya → `index.md` → nama folder. Jika ingin menetapkannya, atur `title`.

## INDEX menghilang

- Pada root dokumentasi yang hanya berisi 1 dokumen, INDEX menutup sendiri hanya pada kali pertama. Anda dapat membukanya dengan ikon tampilan kolom di bilah alat. Perilaku ini dapat dimatikan melalui [Sembunyikan jika dokumen hanya satu] di [Pengaturan tampilan].
- Jika layar sempit, buka melalui [Buka INDEX] (tiga garis) di sebelah kiri [Kembali].

## Tautan ditekan, tetapi tidak terbuka

- "Tujuan tautan tidak ditemukan": file tujuan tautan tidak ada. Tautan internal dapat diperiksa dengan [Pemeriksaan] di Alat Dokumen.
- "Tautan yang tidak aman atau tidak didukung tidak dibuka": tautan ke luar root dokumentasi, atau ke skema selain `https://` dan `mailto:`, tidak akan dibuka.

## Bahasa yang ditampilkan tidak sesuai

- Periksa bahasa halaman yang sedang ditampilkan beserta dasar penentuannya di menu bahasa.
- Bahasa tampilan yang terakhir dipilih akan diingat. Pilih kembali bahasa bawaan di menu bahasa.
- Jika pengaturan pribadi `lunascapeDocEditor.locale` diatur, versi terjemahan dalam bahasa tersebut akan diprioritaskan.

## Topik terkait

- [Beralih root dokumentasi](../02-reading/roots.md)
- [Root dokumentasi dan konvensi file](../04-document-tools/structure.md)
