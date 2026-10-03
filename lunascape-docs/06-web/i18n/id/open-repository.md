# Membuka repositori GitHub

Di versi Web, Anda dapat membuka dan membaca repositori GitHub secara langsung tanpa mengklonnya. Repositori publik dapat dibaca tanpa masuk.

## Membuka dari layar

1. Tekan [Buka dokumen] (ikon folder) di bilah alat. Layar “Buka dokumen” akan terbuka.
2. Di kolom kiri, pilih lokasi yang ingin dibuka.

   | Lokasi | Isi daftar |
   |---|---|
   | Semua | Semua yang ada di bawah. Yang baru dibuka ditampilkan paling atas |
   | Baru dibuka | Repositori dan folder yang pernah Anda buka |
   | Rekomendasi | Panduan yang ditampilkan oleh situs |
   | Repositori GitHub | Repositori yang dapat Anda baca, saat Anda masuk dengan GitHub |
   | Komputer ini | Folder di perangkat ini |

3. Tekan [Buka] pada baris yang ingin dibuka. Ketik di [Saring menurut nama dokumen atau repositori] di bagian atas untuk menyaring baris.

Untuk repositori yang tidak ada dalam daftar, tentukan melalui [Masukkan owner/repo untuk membuka] di kolom kiri.

> **Tips**
>
> - Repositori GitHub yang muncul dalam daftar adalah repositori yang telah dipasangi GitHub App “Lunascape Docs” dan yang dapat Anda baca. Jika repositori tidak ditemukan, mintalah pemilik repositori untuk menambahkan App tersebut.

## Memeriksa lokasi dokumen

Ikon kecil di sisi kiri bilah alat (cip lokasi) menunjukkan lokasi dokumen yang sedang Anda baca.

| Ikon | Lokasi |
|---|---|
| Logo GitHub | Dibaca dari GitHub. Tidak disimpan di perangkat ini |
| Folder | Folder di perangkat ini |

Tekan ikon untuk menampilkan lokasi, status, dan tindakan yang dapat dilakukan dari sana (seperti [Lihat di GitHub] dan [Salin tautan]).

## Membuka dengan URL

Alamat disusun dari repositori dan letak dokumen apa adanya. Jalurnya adalah letak di dalam repositori, sehingga urutannya sama dengan URL GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Yang ditentukan | Cara penulisan |
|---|---|
| Repositori saja (cabang bawaan) | `/github/owner/repo` |
| Dokumen di dalam repositori | `/github/owner/repo/docs/01-product/vision.md` |
| Cabang atau tag tertentu | Tambahkan `?ref=v1.2.0` di akhir |

Alamat juga berubah saat Anda berpindah halaman. Tekan [Bagikan dokumen ini] di bilah alat untuk membagikan tautan ke halaman yang sedang Anda baca. Tombol [Kembali] dan [Maju] pada browser juga dapat digunakan.

Bentuk `?source=` yang lama tetap dapat dibuka seperti sebelumnya. Setelah dibuka, alamat diubah ke bentuk yang baru.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Catatan**
>
> - Jika belum masuk, berlaku batas penggunaan GitHub API (60 kali per jam). Untuk repositori dengan banyak dokumen atau pembacaan berulang, gunakan [Masuk dengan GitHub].
> - Nama cabang yang mengandung `/` (seperti `feature/xxx`) dapat ditentukan dengan `?ref=` pada bentuk alamat di atas. Bentuk `?source=` tidak dapat menuliskannya.
> - Dokumen dimuat dengan izin GitHub milik pembaca. Dokumen tidak ditampilkan kepada orang yang tidak memiliki izin baca.

## Membuka dokumen dari folder lokal

Tekan [Buka dokumen] di bilah alat, lalu pilih folder di perangkat melalui [Buka dokumen dari folder lokal] di kolom kiri. File diproses di dalam browser dan tidak dikirim ke luar. Fitur ini dapat digunakan di browser yang mendukung pemilihan folder (Chrome, Edge, dan lainnya).

## Topik terkait

- [Melihat repositori privat](private-repository.md)
- [Versi Web tidak dapat dibuka atau tidak dapat masuk](../07-troubleshooting/web.md)
