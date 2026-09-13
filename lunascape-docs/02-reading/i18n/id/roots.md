# Mengganti root dokumentasi

Root dokumentasi adalah folder teratas dari satu set dokumen. INDEX, penyaringan, pemeriksaan, dan terjemahan semuanya bekerja per root dokumentasi.

## Cara root dokumentasi ditemukan

Lunascape Docs menelusuri folder induk dari berkas Markdown yang dibuka, lalu menjadikan folder terdekat yang cocok dengan salah satu berikut sebagai root dokumentasi.

- Folder yang berisi `lunascape-docs.json` (nama folder bebas)
- Folder bernama `docs` (nama lain dapat ditambahkan lewat pengaturan `lunascapeDocEditor.rootDirectoryNames`)

Saat Anda menjalankan "Lunascape Docs: Buka Penampil Spesifikasi", root dokumentasi dari pengaturan `lunascapeDocEditor.root` (bawaan `docs`) akan dibuka.

## Beralih ke root dokumentasi lain

Bila ruang kerja memiliki beberapa root dokumentasi, nama root di ujung kiri bilah alat menjadi menu tarik-turun.

1. Tekan nama root dokumentasi di ujung kiri bilah alat.
2. Pilih root dokumentasi dari daftar.
   Halaman awal root tersebut ditampilkan dan INDEX ikut berganti.

> **Petunjuk**
>
> Nama yang muncul dalam daftar ditentukan dengan urutan berikut. Nama tersebut tidak berubah meskipun Anda mengganti bahasa tampilan.
>
> 1. `title` pada `lunascape-docs.json`
> 2. `navigation.title` pada `README.md` di root, atau H1-nya bila tidak ada
> 3. `navigation.title` pada `index.md` di root, atau H1-nya bila tidak ada
> 4. Nama folder (untuk folder `docs` standar, nama folder induknya)

## Membuka Markdown di luar root dokumentasi

Bila Anda membuka berkas Markdown yang tidak berada di dalam root dokumentasi, folder tempat berkas itu berada ditampilkan sebagai root dokumentasi sementara. INDEX menampilkan berkas Markdown pada folder tersebut dan di bawahnya.

- Tekan [Naik satu folder] pada bilah alat untuk memperluas cakupan tampilan hingga folder induk di dalam ruang kerja.
- Pada tampilan ini, pengaturan bahasa proyek dan terjemahan sekaligus tidak dapat digunakan. Letakkan `lunascape-docs.json` pada folder tersebut agar menjadi root dokumentasi, sehingga keduanya dapat digunakan.

## Selalu membuka root dokumentasi tertentu

Bila pengaturan `lunascapeDocEditor.rootMode` disetel ke `fixed`, root dokumentasi pada `lunascapeDocEditor.root` selalu dibuka, apa pun berkas Markdown yang Anda buka.

## Topik terkait

- [Root dokumentasi dan konvensi berkas](../04-document-tools/structure.md)
- [Pengaturan proyek](../04-document-tools/project-configuration.md)
- [Daftar pengaturan VS Code](../08-reference/settings.md)
