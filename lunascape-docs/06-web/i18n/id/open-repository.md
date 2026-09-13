# Membuka repositori GitHub

Pada versi Web, Anda membuka dokumen dengan menentukan repositori GitHub. Untuk repositori publik, tidak perlu masuk.

## Membuka dari layar

1. Buka <https://docs.lunascape.org/>.
2. Tekan [Buka dokumen] (ikon folder) pada bilah alat.
3. Masukkan repositori pada [Tentukan repositori secara langsung], lalu tekan [Buka].
   Saat Anda masuk ke GitHub, Anda juga dapat memilih dari daftar pada [Pilih dari repositori yang dapat dibaca].

> **Tips**
>
> - Ikon GitHub di sebelahnya membuka dokumen yang sedang Anda baca di github.com. Itu bukan tindakan untuk membuka dokumen.

## Membuka dengan URL

Alamatnya menyusun letak repositori dan dokumen apa adanya. Karena path adalah letak di dalam repositori, susunannya sama dengan URL GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Yang ditentukan | Cara penulisan |
|---|---|
| Hanya repositori (branch bawaan) | `/github/owner/repo` |
| Dokumen di dalam repositori | `/github/owner/repo/docs/01-product/vision.md` |
| Menentukan branch atau tag | Tambahkan `?ref=v1.2.0` di bagian akhir |

Saat Anda berpindah halaman, alamatnya ikut berubah. Tekan [Bagikan dokumen ini] pada bilah alat untuk memberikan tautan ke halaman yang sedang Anda baca. Tombol [Kembali] dan [Maju] pada peramban juga dapat digunakan.

Bentuk `?source=` yang lama pun tetap dapat dibuka seperti sebelumnya. Setelah terbuka, alamatnya ditulis ulang ke bentuk yang baru.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Perhatian**
>
> - Saat tidak masuk, berlaku batas penggunaan GitHub API (60 kali per jam). Untuk repositori dengan banyak dokumen atau pembacaan berulang, gunakan [Masuk dengan GitHub].
> - Nama branch yang mengandung `/` (seperti `feature/xxx`) dapat ditentukan dengan `?ref=` pada bentuk alamat di atas. Bentuk `?source=` tidak dapat menuliskannya.
> - Dokumen dimuat dengan izin GitHub milik pembaca. Orang tanpa izin baca tidak dapat melihatnya.

## Membuka dokumen dari folder lokal

Tekan [Buka dokumen] pada bilah alat, lalu pilih folder di dalam perangkat Anda dari [Buka dokumen dari folder lokal] yang berada di bawah daftar. Berkas diproses di dalam peramban dan tidak dikirim ke luar. Fitur ini dapat digunakan pada peramban yang mendukung pemilihan folder (Chrome, Edge, dan lainnya).

## Topik terkait

- [Membaca repositori non-publik](private-repository.md)
- [Tidak dapat membuka atau masuk pada versi Web](../07-troubleshooting/web.md)
