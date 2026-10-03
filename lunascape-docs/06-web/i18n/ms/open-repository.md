# Membuka repositori GitHub

Dalam versi Web dan Lunascape, anda boleh membuka dan membaca repositori GitHub secara terus tanpa menyalinnya. Repositori awam tidak memerlukan log masuk.

## Membuka dari skrin

1. Tekan [Buka dokumen] (ikon folder) pada bar alat. Skrin “Buka dokumen” dibuka.
2. Dalam lajur kiri, pilih lokasi yang hendak dibuka.

   | Lokasi | Kandungan senarai |
   |---|---|
   | Semua | Semua lokasi di bawah. Item yang dibuka baru-baru ini disenaraikan dahulu |
   | Dibuka baru-baru ini | Repositori dan folder yang pernah anda buka |
   | Pilihan | Manual yang diperkenalkan oleh laman ini |
   | Repositori GitHub | Repositori yang boleh anda baca semasa anda log masuk ke GitHub |
   | Komputer ini | Folder pada peranti ini. Dalam Lunascape, repositori yang telah anda salin juga disenaraikan di sini |

3. Tekan [Buka] pada baris yang hendak dibuka. Untuk menapis baris, taip dalam [Tapis mengikut nama dokumen atau repositori] di bahagian atas.

Untuk repositori yang tiada dalam senarai, nyatakannya melalui [Masukkan owner/repo untuk membuka] dalam lajur kiri.

> **Petua**
>
> - Repositori GitHub dalam senarai ialah repositori yang dipasang dengan GitHub App “Lunascape Docs” dan yang anda ada kebenaran untuk membacanya. Jika repositori tidak kelihatan, minta pemilik repositori menambah App itu.

## Menyemak lokasi dokumen

Ikon kecil di sebelah kiri bar alat (cip lokasi) menunjukkan lokasi dokumen yang sedang anda baca.

| Ikon | Lokasi |
|---|---|
| Tanda GitHub | Dibaca dari GitHub. Tidak disimpan pada peranti ini |
| Komputer | Folder pada peranti ini yang diuruskan oleh Lunascape. Nama cabang Git dan bilangan fail yang diubah juga dipaparkan |
| Folder | Folder pada peranti ini |

Tekan ikon untuk melihat lokasi, status dan tindakan yang boleh dilakukan dari situ (seperti [Lihat di GitHub] dan [Salin pautan]).

## Menyalin repositori dalam Lunascape

Dalam Lunascape, anda boleh menyalin repositori GitHub ke peranti ini, kemudian menyunting dan membuat komit dengan Git.

- Pada skrin “Buka dokumen”, tekan [Salin] pada baris repositori.
- Semasa membaca repositori yang dibuka dari GitHub, tekan cip lokasi, kemudian tekan [Salin ke komputer ini]. Apabila penyalinan selesai, dokumen yang sama dibuka daripada salinan pada peranti ini.

Repositori yang telah disalin ditandakan “Ada di komputer ini” dalam senarai, dan [Buka di komputer ini] disenaraikan dahulu.

## Membuka melalui URL

Alamat menyusun repositori dan lokasi dokumen seperti yang ada. Laluan ialah lokasi dalam repositori, jadi susunannya sama seperti URL GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Yang dinyatakan | Cara menulis |
|---|---|
| Repositori sahaja (cabang lalai) | `/github/owner/repo` |
| Dokumen dalam repositori | `/github/owner/repo/docs/01-product/vision.md` |
| Cabang atau tag | Tambah `?ref=v1.2.0` di hujung |

Alamat turut berubah apabila anda berpindah halaman. Tekan [Kongsi dokumen ini] pada bar alat untuk memberikan pautan ke halaman yang sedang anda baca. Butang [Kembali] dan [Ke hadapan] pelayar juga boleh digunakan.

Bentuk `?source=` yang lama masih boleh dibuka seperti biasa. Selepas dibuka, alamat ditukar kepada bentuk baharu.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Perhatian**
>
> - Tanpa log masuk, had penggunaan API GitHub (60 kali sejam) dikenakan. Untuk repositori yang mempunyai banyak dokumen atau untuk pembacaan berulang, tekan [Log masuk dengan GitHub].
> - Nama cabang yang mengandungi `/` (seperti `feature/xxx`) boleh dinyatakan dengan `?ref=` dalam bentuk alamat di atas. Nama ini tidak boleh ditulis dalam bentuk `?source=`.
> - Dokumen dimuatkan dengan kebenaran GitHub pembaca. Dokumen tidak dipaparkan kepada orang yang tiada kebenaran membaca.

## Membuka dokumen daripada folder setempat

Tekan [Buka dokumen] pada bar alat, kemudian pilih folder pada peranti melalui [Buka dokumen daripada folder setempat] dalam lajur kiri. Fail diproses di dalam pelayar dan tidak dihantar ke luar. Ciri ini boleh digunakan dalam pelayar yang menyokong pemilihan folder (Chrome, Edge dan lain-lain).

## Topik berkaitan

- [Membaca repositori persendirian](private-repository.md)
- [Tidak dapat membuka atau log masuk dalam versi Web](../07-troubleshooting/web.md)
