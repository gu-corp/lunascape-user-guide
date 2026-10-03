# Membuka repositori GitHub

Di versi Web dan di Lunascape, Anda dapat membuka dan membaca repositori GitHub secara langsung tanpa menduplikatnya. Untuk repositori publik, Anda tidak perlu masuk.

## Membuka dari layar

1. Tekan [Buka dokumen] (ikon folder) di bilah alat. Layar "Buka dokumen" terbuka.
2. Di kolom kiri, pilih tempat yang ingin dibuka.

   | Tempat | Isi daftar |
   |---|---|
   | Semua | Semua yang ada di bawah ini. Yang baru dibuka ditampilkan paling atas |
   | Baru dibuka | Repositori dan folder yang pernah Anda buka |
   | Unggulan | Manual yang diperkenalkan oleh situs |
   | Repositori GitHub | Saat Anda masuk dengan GitHub, repositori yang dapat Anda baca |
   | Komputer ini | Folder di perangkat ini. Di Lunascape, repositori yang telah diduplikat juga ditampilkan di sini |

3. Tekan [Buka] pada baris yang ingin dibuka. Ketik di [Saring menurut nama dokumen atau repositori] di bagian atas untuk menyaring baris.

Repositori yang tidak ada dalam daftar dapat ditentukan melalui [Masukkan owner/repo untuk membuka] di kolom kiri.

> **Tips**
>
> - Repositori GitHub yang muncul dalam daftar adalah repositori yang telah dipasangi GitHub App "Lunascape Docs" dan yang dapat Anda baca. Jika repositori yang dicari tidak ditemukan, mintalah pemilik repositori untuk menambahkan App tersebut.

## Memeriksa lokasi dokumen

Ikon kecil di sisi kiri bilah alat (chip lokasi) menunjukkan lokasi dokumen yang sedang Anda baca.

| Ikon | Lokasi |
|---|---|
| Logo GitHub | Dibaca dari GitHub. Tidak disimpan di perangkat ini |
| Komputer | Folder di perangkat ini yang dikelola oleh Lunascape. Nama cabang Git dan jumlah file yang diubah juga ditampilkan |
| Folder | Folder di perangkat ini |

Tekan ikon untuk menampilkan lokasi, status, dan tindakan yang dapat dilakukan dari sana ([Lihat di GitHub], [Salin tautan], dan lainnya).

## Menduplikat repositori di Lunascape

Di Lunascape, Anda dapat menduplikat repositori GitHub ke perangkat ini, lalu mengedit dan melakukan commit dengan Git.

- Di layar "Buka dokumen", tekan [Duplikat] pada baris repositori.
- Saat membaca repositori yang dibuka dari GitHub, tekan chip lokasi, lalu tekan [Duplikat ke komputer ini]. Setelah duplikasi selesai, dokumen yang sama terbuka dari salinan di perangkat ini.

Repositori yang telah diduplikat ditandai "Ada di komputer ini" dalam daftar, dan [Buka di komputer ini] ditampilkan lebih dulu.

## Membuka dengan URL

Alamat terdiri atas repositori dan posisi dokumen yang disusun apa adanya. Jalurnya adalah posisi di dalam repositori, sehingga susunannya sama dengan URL GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Yang ditentukan | Cara menulis |
|---|---|
| Repositori saja (cabang bawaan) | `/github/owner/repo` |
| Dokumen di dalam repositori | `/github/owner/repo/docs/01-product/vision.md` |
| Menentukan cabang atau tag | Tambahkan `?ref=v1.2.0` di akhir |

Alamat juga berubah saat Anda berpindah halaman. Tekan [Bagikan dokumen ini] di bilah alat untuk membagikan tautan ke halaman yang sedang Anda baca. Tombol [Kembali] dan [Maju] di browser juga dapat digunakan.

Bentuk lama `?source=` tetap dapat dibuka seperti sebelumnya. Setelah dibuka, alamat diubah ke bentuk baru.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Perhatian**
>
> - Jika Anda belum masuk, berlaku batas penggunaan GitHub API (60 kali per jam). Untuk repositori dengan banyak dokumen atau pembacaan berulang, gunakan [Masuk dengan GitHub].
> - Nama cabang yang mengandung `/` (seperti `feature/xxx`) dapat ditentukan dengan `?ref=` pada format alamat di atas. Bentuk `?source=` tidak dapat menuliskannya.
> - Dokumen dimuat dengan izin GitHub milik pembaca. Dokumen tidak ditampilkan kepada orang yang tidak memiliki izin baca.

## Membuka dokumen dari folder lokal

Tekan [Buka dokumen] di bilah alat, lalu pilih folder di perangkat Anda melalui [Buka dokumen dari folder lokal] di kolom kiri. File diproses di dalam browser dan tidak dikirim ke luar. Fitur ini dapat digunakan di browser yang mendukung pemilihan folder (Chrome, Edge, dan lainnya).

## Topik terkait

- [Melihat repositori privat](private-repository.md)
- [Tidak dapat membuka atau masuk di versi Web](../07-troubleshooting/web.md)
