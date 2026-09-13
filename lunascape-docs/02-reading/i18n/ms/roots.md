# Menukar akar dokumentasi

Akar dokumentasi ialah folder teratas bagi satu set dokumen. INDEX, penapisan, semakan dan terjemahan semuanya beroperasi mengikut setiap akar dokumentasi.

## Cara akar dokumentasi ditemukan

Lunascape Docs menyusur ke atas daripada fail Markdown yang dibuka, dan menjadikan folder terdekat yang menepati salah satu daripada berikut sebagai akar dokumentasi.

- Folder yang mengandungi `lunascape-docs.json` (apa-apa nama folder)
- Folder bernama `docs` (nama lain boleh ditambah dengan tetapan `lunascapeDocEditor.rootDirectoryNames`)

Apabila anda menjalankan "Lunascape Docs: Buka Pemapar Spesifikasi", akar dokumentasi daripada tetapan `lunascapeDocEditor.root` (lalai `docs`) akan dibuka.

## Bertukar ke akar dokumentasi lain

Apabila ruang kerja mempunyai beberapa akar dokumentasi, nama akar dokumentasi di hujung kiri bar alat menjadi senarai juntai bawah.

1. Tekan nama akar dokumentasi di hujung kiri bar alat.
2. Pilih satu akar dokumentasi daripada senarai.
   Halaman mula akar dokumentasi yang dipilih akan dipaparkan dan INDEX bertukar.

> **Petua**
>
> Nama yang dipaparkan dalam senarai ditentukan mengikut susunan berikut. Nama itu tidak berubah walaupun anda menukar bahasa paparan.
>
> 1. `title` dalam `lunascape-docs.json`
> 2. `navigation.title` pada `README.md` akar, jika tiada, H1 fail itu
> 3. `navigation.title` pada `index.md` akar, jika tiada, H1 fail itu
> 4. Nama folder (bagi folder `docs` yang standard, nama folder induknya)

## Membuka Markdown yang tiada dalam akar dokumentasi

Apabila anda membuka fail Markdown yang tidak terkandung dalam mana-mana akar dokumentasi, folder fail itu dipaparkan sebagai akar dokumentasi sementara. INDEX menyenaraikan fail Markdown dalam folder itu dan di bawahnya.

- Tekan [Naik satu folder] pada bar alat untuk meluaskan julat paparan sehingga ke folder induk dalam ruang kerja.
- Dalam paparan ini, tetapan bahasa projek dan terjemahan pukal tidak boleh digunakan. Letakkan `lunascape-docs.json` dalam folder itu untuk menjadikannya akar dokumentasi, barulah kedua-duanya boleh digunakan.

## Sentiasa membuka akar dokumentasi yang tetap

Tetapkan `lunascapeDocEditor.rootMode` kepada `fixed` supaya akar dokumentasi dalam `lunascapeDocEditor.root` sentiasa dibuka, apa jua fail Markdown yang anda buka.

## Topik berkaitan

- [Akar dokumentasi dan konvensyen fail](../04-document-tools/structure.md)
- [Tetapan projek](../04-document-tools/project-configuration.md)
- [Senarai tetapan VS Code](../08-reference/settings.md)
