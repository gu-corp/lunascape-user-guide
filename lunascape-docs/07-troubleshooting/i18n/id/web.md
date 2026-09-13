# Tidak dapat membuka atau masuk di versi Web

## Sudah masuk, tetapi repositori tidak muncul di daftar

GitHub App "Lunascape Docs" belum dipasang pada akun tersebut, atau repositori yang dimaksud tidak termasuk di dalamnya. Mintalah pemilik repositori atau administrator organisasi untuk memasangnya sesuai langkah di [Membaca repositori privat](../06-web/private-repository.md).

## Tidak dapat melanjutkan dari layar masuk

- Anda tidak memiliki izin baca untuk repositori tersebut. Mintalah pemilik repositori untuk memberikan izin.
- "Masuk dengan GitHub belum diatur untuk situs ini": penampil yang Anda pasang sendiri belum memiliki layanan masuk. Administrator perlu mengatur layanan masuk tersebut.

## Pop-up untuk masuk tidak terbuka

Peramban memblokir pop-up. Izinkan pop-up untuk situs ini, lalu coba lagi.

## Muncul pesan "Sesi masuk Anda telah berakhir"

Masa berlaku sesi masuk telah berakhir. Tekan [Masuk dengan GitHub] sekali lagi.

## Repositori publik menampilkan 404

- Periksa penulisan `owner/repo@ref/dir`.
- Nama cabang yang mengandung `/` tidak dapat ditentukan.

## Setelah beberapa saat, halaman tidak dapat dimuat

Selama Anda belum masuk, berlaku batas penggunaan GitHub API (60 kali per jam). Jika muncul "Batas jumlah permintaan tercapai", tunggu beberapa saat atau lakukan [Masuk dengan GitHub].

## Muncul pesan "Situs ini tidak dapat menampilkan repositori ini"

Untuk membukanya dari penampil yang Anda pasang sendiri, URL situs tersebut harus ditambahkan ke `viewer.origins` pada `lunascape-docs.json` di sisi repositori.

## Membuka `index.html` tidak menampilkan apa pun

Membukanya langsung melalui `file://` tidak berfungsi. Bukalah melalui server HTTP, atau gunakan versi VS Code.

## Situs hasil ekspor menampilkan "lunascape-docs-manifest.json tidak ditemukan"

Tempatkan seluruh berkas hasil `npm run export:web` (termasuk manifesnya) apa adanya.

## Draf tidak dapat disimpan

- "IndexedDB tidak dapat dibuka", "Sedang digunakan oleh tab lain": penyebabnya adalah mode privat peramban, atau tab lain yang membuka situs yang sama. Bukalah di jendela biasa dan tutup tab lainnya.
- Draf disimpan per perangkat dan per peramban. Draf tidak diteruskan ke perangkat lain.

## Topik terkait

- [Membuka repositori GitHub](../06-web/open-repository.md)
- [Menyimpan draf](../06-web/drafts.md)
