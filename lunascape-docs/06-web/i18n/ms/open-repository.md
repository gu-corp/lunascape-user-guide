# Membuka repositori GitHub

Dalam versi Web, anda boleh terus membuka dan membaca repositori GitHub tanpa menyalinnya. Repositori awam tidak memerlukan log masuk.

## Buka dari skrin

1. Tekan [Buka dokumen] (ikon folder) pada bar alat. Skrin "Buka dokumen" dibuka.
2. Dalam lajur kiri, pilih lokasi yang hendak dibuka.

   | Lokasi | Yang disenaraikan |
   |---|---|
   | Semua | Semua lokasi di bawah. Item yang dibuka baru-baru ini disenaraikan dahulu |
   | Dibuka baru-baru ini | Repositori dan folder yang pernah anda buka |
   | Pilihan | Manual yang diketengahkan oleh tapak |
   | Repositori GitHub | Repositori yang boleh anda baca, apabila anda telah log masuk ke GitHub |
   | Komputer ini | Folder pada peranti ini |

3. Tekan [Buka] pada baris yang anda mahu. Untuk menapis baris, taip dalam [Tapis mengikut nama dokumen atau repositori] di bahagian atas.

Untuk repositori yang tiada dalam senarai, nyatakannya melalui [Masukkan owner/repo dan buka] dalam lajur kiri.

> **Petua**
>
> - Repositori GitHub dalam senarai ialah repositori yang telah dipasang dengan GitHub App "Lunascape Docs" dan yang boleh anda baca. Jika repositori tidak kelihatan, minta pemilik repositori menambah App tersebut.

## Semak lokasi dokumen

Ikon kecil di sebelah kiri bar alat (cip lokasi) menunjukkan lokasi dokumen yang sedang anda baca.

| Ikon | Lokasi |
|---|---|
| Tanda GitHub | Dibaca daripada GitHub. Tidak disimpan pada peranti ini |
| Folder | Folder pada peranti ini |

Tekan ikon untuk melihat lokasi, status dan tindakan yang boleh dilakukan dari situ (seperti [Lihat di GitHub] dan [Salin pautan]).

## Buka melalui URL

Alamat menyusun repositori dan kedudukan dokumen mengikut urutan. Laluan ialah kedudukan dalam repositori, jadi susunannya sama seperti URL GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Yang dinyatakan | Cara penulisan |
|---|---|
| Repositori sahaja (cawangan lalai) | `/github/owner/repo` |
| Dokumen dalam repositori | `/github/owner/repo/docs/01-product/vision.md` |
| Cawangan atau teg tertentu | Tambah `?ref=v1.2.0` di hujung |

Apabila anda beralih halaman, alamat turut berubah. Tekan [Kongsi dokumen ini] pada bar alat untuk memberikan pautan halaman yang sedang anda baca. [Kembali] dan [Ke hadapan] pada pelayar juga boleh digunakan.

Bentuk `?source=` yang lama masih boleh dibuka seperti sebelum ini. Selepas dibuka, alamat ditulis semula ke bentuk baharu.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Perhatian**
>
> - Tanpa log masuk, had penggunaan API GitHub (60 kali sejam) dikenakan. Untuk repositori yang mempunyai banyak dokumen atau bacaan berulang, gunakan [Log masuk dengan GitHub].
> - Nama cawangan yang mengandungi `/` (seperti `feature/xxx`) boleh dinyatakan dengan `?ref=` dalam bentuk alamat di atas. Nama ini tidak dapat ditulis dalam bentuk `?source=`.
> - Dokumen dimuatkan dengan kebenaran GitHub pembaca. Dokumen tidak dipaparkan kepada orang yang tiada kebenaran membaca.

## Buka dokumen daripada folder setempat

Tekan [Buka dokumen] pada bar alat, kemudian pilih folder pada peranti anda melalui [Buka dokumen daripada folder setempat] dalam lajur kiri. Fail diproses di dalam pelayar dan tidak dihantar ke luar. Ciri ini boleh digunakan dalam pelayar yang menyokong pemilihan folder (Chrome, Edge dan lain-lain).

## Topik berkaitan

- [Membaca repositori persendirian](private-repository.md)
- [Versi Web tidak dapat dibuka atau tidak dapat log masuk](../07-troubleshooting/web.md)
