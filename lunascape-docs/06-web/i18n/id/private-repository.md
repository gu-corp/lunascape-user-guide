# Membaca repositori privat

Setelah masuk dengan GitHub, Anda dapat membaca dokumen dari repositori privat, terbatas pada repositori yang Anda miliki akses bacanya. Lunascape Docs tidak pernah memiliki akun atau izin sendiri.

## Masuk dan buka

1. Buka <https://docs.lunascape.org/>.
   Ketika Anda menentukan dokumen privat atau belum masuk, layar masuk akan muncul.
2. Tekan [Masuk dengan GitHub].
   Layar otorisasi GitHub terbuka dalam pop-up.
3. Setelah masuk, tekan [Buka dokumen] di bilah alat, lalu pilih repositori yang ingin dibuka di [Pilih dari repositori yang dapat dibaca].

> **Petunjuk**
>
> - Nama akun yang sedang masuk ditampilkan di bilah alat. Anda juga dapat [Keluar] atau [Masuk dengan akun lain] dari sini.
> - Daftar menampilkan repositori dari akun (organisasi atau perorangan) yang telah memasang GitHub App "Lunascape Docs", terbatas pada repositori yang dapat Anda baca.

## Pengaturan yang dilakukan oleh pemilik repositori

Jika repositori yang dituju tidak muncul dalam daftar, pemilik repositori atau administrator organisasi perlu memasang GitHub App "Lunascape Docs".

- Izin yang diminta adalah Contents (baca dan tulis) dan Pull requests (baca dan tulis). Izin baca untuk membaca; izin tulis untuk mengirim permintaan publikasi (Pull Request) dari Web. Lunascape Docs tidak pernah menyimpan isi dokumen.
- Pemasangan dilakukan per akun (organisasi atau perorangan). Tentukan apakah targetnya "All repositories" (yang otomatis mencakup repositori yang dibuat kemudian) atau hanya repositori yang dipilih.

| Situasi | Langkah |
|---|---|
| Memasang pada organisasi atau akun perorangan yang baru | Lakukan dari [halaman pemasangan](https://github.com/apps/lunascape-docs/installations/new) |
| Menambahkan repositori pada organisasi yang sudah memasangnya | Atur di Settings organisasi → GitHub Apps → Lunascape Docs → Configure → Repository access |

Meskipun dipasang untuk seluruh organisasi, setiap anggota hanya dapat membaca repositori yang izin bacanya dimiliki. Permintaan publikasi juga hanya dapat dikirim untuk repositori yang izin tulisnya dimiliki.

> **Petunjuk**
> - Saat pemasangan baru, izin yang diminta ditampilkan sebagai daftar di layar pemasangan, dan menekan "Install" berarti Anda telah menyetujuinya. Tidak ada langkah tambahan.
> - Organisasi yang telah memasang aplikasi sebelum ada izin yang ditambahkan akan menerima email konfirmasi kepada administratornya, dan tombol persetujuan muncul di bagian atas Settings organisasi → GitHub Apps → Lunascape Docs → Configure. Sampai disetujui, organisasi itu hanya dapat membaca, dan bila mengirim permintaan publikasi akan muncul pesan "Pemberian izin tulis diperlukan".
> - Izin yang sedang berlaku saat ini dapat diperiksa di layar Configure yang sama. Untuk akun perorangan, tempatnya adalah Settings → Applications → Installed GitHub Apps.
> - Jika repositori target keliru dilepas atau aplikasi tidak sengaja dicopot, memasangnya kembali dari [halaman pemasangan](https://github.com/apps/lunascape-docs/installations/new) akan mengembalikannya. Pesan penolakan permintaan publikasi disertai tautan ke layar untuk memperbaikinya.
> - Jika pada sisi repositori Anda tidak ingin menerima permintaan publikasi, tuliskan `"publish": { "enabled": false }` di `lunascape-docs.json`. Membaca tetap dapat dilakukan seperti biasa.

## Topik terkait

- [Membuka repositori GitHub](open-repository.md)
- [Tidak dapat membuka atau masuk di versi Web](../07-troubleshooting/web.md)
