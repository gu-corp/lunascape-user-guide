# Menerbitkan dokumen Anda di Web

Anda dapat menerbitkan dokumen dari repositori Anda sendiri sebagai situs web di GitHub Pages atau hosting statis mana pun. Ada dua cara. Langkah-langkah ini ditujukan bagi pengembang yang dapat melakukan clone repositori Lunascape Docs dan menggunakan `npm`.

## Cara 1: menempatkan dua berkas penampil

Terapkan hanya penampilnya saja (`index.html` dan `lsdoc.js`), lalu biarkan dokumen dimuat dari GitHub. Dokumennya sendiri tidak termasuk dalam situs, sehingga cara ini aman untuk repositori privat (pembaca masuk dengan GitHub).

1. Jalankan perintah berikut di repositori Lunascape Docs.

   ```sh
   npm run build:viewer
   ```

   `index.html` dan `lsdoc.js` dibuat di `dist/viewer/`.
2. Letakkan kedua berkas tersebut di `docs/` pada repositori yang ingin Anda terbitkan.
3. Aktifkan GitHub Pages.

Root dokumentasi yang ditampilkan ditentukan dengan urutan berikut.

1. Pengaturan `source` di dalam `index.html`
2. `repository` yang tercantum pada `lunascape-docs.json` di folder yang sama
3. Perkiraan dari URL `*.github.io` dan susunan cabang

## Cara 2: mengekspor situs statis beserta dokumennya

Ekspor penampil bersama berkas dokumen, lalu hosting hasilnya apa adanya.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Keluarannya berisi satu set penampil, dokumen di bawah `docs/`, berkas daftar `lunascape-docs-manifest.json`, dan `.nojekyll`. Tempatkan hasil keluaran di S3 atau GitHub Pages untuk menerbitkannya. Untuk contoh penerbitan otomatis dengan GitHub Actions, lihat `examples/workflows/publish-docs-pages.yml` di repositori.

> **Perhatian**
>
> - **Jangan mengekspor dokumen dari repositori privat dan menempatkannya di GitHub Pages.** GitHub Pages selain Enterprise Cloud dapat dibaca siapa saja. Jika Anda memerlukan penerbitan terbatas, gunakan cara 1 dan minta pembaca masuk dengan GitHub.
> - Membuka `index.html` langsung melalui `file://` tidak berfungsi. Hal ini karena peramban melarang pemuatan berkas di sebelahnya dan eksekusi modul ES. Untuk memeriksanya secara lokal, gunakan versi VS Code atau server HTTP.
> - Pustaka penggambaran untuk TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob, dan Penrose dimuat saat ditampilkan. Pada situs yang diekspor, tempatkan juga folder `vendor/`.

## Topik terkait

- [Apa yang bisa dilakukan versi Web](README.md)
- [Membaca repositori privat](private-repository.md)
