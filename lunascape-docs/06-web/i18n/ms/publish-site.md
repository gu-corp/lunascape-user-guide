# Menerbitkan dokumen anda di Web

Anda boleh menerbitkan dokumen daripada repositori anda sendiri sebagai tapak web di GitHub Pages atau mana-mana hosting statik. Terdapat dua cara. Langkah ini ditujukan kepada pembangun yang boleh melakukan clone pada repositori Lunascape Docs dan menggunakan `npm`.

## Cara 1: letakkan dua fail pemapar

Hanya pemapar itu sendiri (`index.html` dan `lsdoc.js`) yang diletakkan, manakala dokumen dimuatkan daripada GitHub. Dokumen itu sendiri tidak termasuk dalam tapak, jadi cara ini selamat untuk repositori persendirian (pembaca log masuk dengan GitHub).

1. Jalankan arahan berikut dalam repositori Lunascape Docs.

   ```sh
   npm run build:viewer
   ```

   `index.html` dan `lsdoc.js` dijana dalam `dist/viewer/`.
2. Letakkan kedua-dua fail itu ke dalam `docs/` bagi repositori yang hendak anda terbitkan.
3. Aktifkan GitHub Pages.

Akar dokumentasi yang dipaparkan ditentukan mengikut susunan berikut.

1. Tetapan `source` di dalam `index.html`
2. `repository` yang tercatat dalam `lunascape-docs.json` di dalam folder yang sama
3. Anggaran daripada URL `*.github.io` dan susunan cawangan

## Cara 2: eksport tapak statik yang mengandungi dokumen

Pemapar dan fail dokumen dieksport sekali gus, lalu dihoskan seadanya.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Keluarannya mengandungi set pemapar, dokumen di bawah `docs/`, fail senarai `lunascape-docs-manifest.json` dan `.nojekyll`. Letakkan destinasi keluaran itu di S3 atau GitHub Pages untuk menerbitkannya. Untuk contoh penerbitan automatik dengan GitHub Actions, rujuk `examples/workflows/publish-docs-pages.yml` dalam repositori.

> **Perhatian**
>
> - **Jangan eksport dokumen repositori persendirian dan letakkannya di GitHub Pages.** GitHub Pages selain Enterprise Cloud boleh dibaca oleh sesiapa sahaja. Jika anda memerlukan penerbitan terhad, gunakan cara 1 dan minta pembaca log masuk dengan GitHub.
> - Membuka `index.html` terus melalui `file://` tidak berfungsi. Ini kerana pelayar melarang pemuatan fail bersebelahan dan pelaksanaan modul ES. Untuk menyemak di komputer anda, gunakan versi VS Code atau pelayan HTTP.
> - Pustaka lukisan untuk TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob dan Penrose dimuatkan semasa paparan. Pada tapak yang dieksport, letakkan folder `vendor/` bersama-sama.

## Topik berkaitan

- [Apa yang boleh dilakukan dengan versi Web](README.md)
- [Membaca repositori persendirian](private-repository.md)
