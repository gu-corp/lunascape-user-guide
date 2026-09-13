# Akar dokumentasi dan konvensyen fail

Peraturan yang diikuti Lunascape Docs semasa mencari dokumen dan membina INDEX. Sistem fail itu sendiri ialah sumber rujukan, jadi tiada daftar atau tetapan binaan diperlukan.

## Akar dokumentasi

- Folder `docs` yang terdekat, atau folder yang mengandungi `lunascape-docs.json`, menjadi akar dokumentasi.
- Dengan adanya `lunascape-docs.json`, nama folder tidak semestinya `docs`.
- Apabila anda membuka fail Markdown yang tidak tergolong dalam mana-mana akar dokumentasi, foldernya dipaparkan sebagai akar dokumentasi sementara.

## Fail yang dipaparkan dalam INDEX

- Fail `.md`, `.markdown` dan `.mdx` dipaparkan. Fail baharu sentiasa muncul, walaupun tanpa front matter atau maklumat navigasi.
- Folder yang bermula dengan `.`, `node_modules`, dan folder yang disenaraikan dalam `ignoredDirectories` (lalai `99-archive`) tidak dipaparkan.
- Segala-galanya di bawah `i18n/` dianggap sebagai terjemahan dan tidak disenaraikan secara berasingan dalam INDEX.

## Halaman muka depan folder

- `README.md` (atau `index.md` jika tiada README) yang mempunyai isi kandungan menjadi halaman muka depan folder tersebut. Menekan nama folder dalam INDEX akan membukanya.
- `README.md` yang hanya mengandungi front matter tanpa isi kandungan dianggap sebagai "deskriptor khusus tetapan" dan tidak dipaparkan sebagai halaman. Gunakannya apabila folder hanya memerlukan tajuk atau susunan.
- Apabila `README.md` dan `index.md` kedua-duanya wujud, `README.md` diutamakan.

## Bahasa lalai dan terjemahan

- Dokumen dalam bahasa lalai (dokumen kanonik) kekal di tempatnya.
- Terjemahan diletakkan dalam `i18n/<bahasa>/` di dalam folder yang sama dengan dokumen kanonik, dengan nama fail yang sama. Membina semula struktur folder di bawah `i18n/` tidak dikenali.
- Itu sahaja satu-satunya lokasi terjemahan diselesaikan. Fail dengan nama yang sama yang diletakkan di tempat lain menjadi fail terpencil yang tidak dituntut oleh mana-mana dokumen sebagai terjemahannya.

```text
docs/
  lunascape-docs.json
  README.md                  ← halaman muka depan akar (halaman mula)
  i18n/en/README.md          ← versi bahasa Inggerisnya
  01-product/
    README.md                ← halaman muka depan folder
    requirements.md
    i18n/en/README.md        ← versi bahasa Inggeris bagi dua dokumen di atas
    i18n/en/requirements.md
  99-archive/                ← dikecualikan daripada INDEX secara lalai
```

## Tentang `_meta.json`

`_meta.json` daripada Nextra tidak digunakan untuk navigasi. Fail sedia ada tidak diubah dan tidak dipadamkan. Pada masa hadapan, hanya fungsi import/eksport yang eksplisit akan mengendalikannya.

## Topik berkaitan

- [Menetapkan maklumat navigasi](navigation-metadata.md)
- [Tetapan projek](project-configuration.md)
- [Menukar akar dokumentasi](../02-reading/roots.md)
