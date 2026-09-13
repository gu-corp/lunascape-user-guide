# Membuka repositori GitHub

Dalam versi Web, anda membuka dokumen dengan menyatakan repositori GitHub. Repositori awam tidak memerlukan log masuk.

## Membuka daripada skrin

1. Buka <https://docs.lunascape.org/>.
2. Tekan [Buka dokumen] (ikon folder) pada bar alat.
3. Masukkan repositori pada [Nyatakan repositori secara terus], kemudian tekan [Buka].
   Apabila anda telah log masuk ke GitHub, anda juga boleh memilih daripada senarai pada [Pilih daripada repositori yang boleh dibaca].

> **Petua**
>
> - Ikon GitHub di sebelahnya membuka dokumen yang sedang anda baca di github.com. Ia bukan tindakan untuk membuka dokumen.

## Membuka melalui URL

Alamatnya menyusun kedudukan repositori dan dokumen sebagaimana adanya. Oleh sebab laluan itu ialah kedudukan di dalam repositori, susunannya sama dengan URL GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Yang dinyatakan | Cara menulisnya |
|---|---|
| Repositori sahaja (cabang lalai) | `/github/owner/repo` |
| Dokumen di dalam repositori | `/github/owner/repo/docs/01-product/vision.md` |
| Menyatakan cabang atau tag | Tambah `?ref=v1.2.0` pada hujungnya |

Alamat turut berubah apabila anda berpindah halaman. Tekan [Kongsi dokumen ini] pada bar alat untuk menyerahkan pautan ke halaman yang sedang anda baca. Butang [Kembali] dan [Ke hadapan] pada pelayar juga boleh digunakan.

Bentuk `?source=` yang lama masih boleh dibuka seperti biasa. Selepas dibuka, ia ditulis semula kepada bentuk yang baharu.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Perhatian**
>
> - Dalam keadaan tidak log masuk, had penggunaan API GitHub (60 kali sejam) terpakai. Bagi repositori yang mempunyai banyak dokumen atau bacaan berulang, sila [Log masuk dengan GitHub].
> - Nama cabang yang mengandungi `/` (seperti `feature/xxx`) boleh dinyatakan dengan `?ref=` dalam bentuk alamat di atas. Ia tidak dapat ditulis dalam bentuk `?source=`.
> - Dokumen dimuatkan dengan kebenaran GitHub pembaca itu sendiri. Orang yang tiada kebenaran membaca tidak dapat melihatnya.

## Membuka dokumen dalam folder setempat

Tekan [Buka dokumen] pada bar alat, kemudian pilih folder dalam peranti anda melalui [Buka dokumen daripada folder setempat] di bawah senarai. Fail diproses di dalam pelayar dan tidak dihantar ke luar. Ia boleh digunakan pada pelayar yang menyokong pemilihan folder (Chrome, Edge dan lain-lain).

## Topik berkaitan

- [Melihat repositori tidak awam](private-repository.md)
- [Tidak dapat membuka atau log masuk pada versi Web](../07-troubleshooting/web.md)
