# Membaca dalam bahasa lain

Dokumen yang memiliki terjemahan dapat dibaca dengan mengganti bahasa dari menu bahasa (globe) di bilah alat.

## Mengganti bahasa

1. Tekan menu bahasa di bilah alat.
   Bahasa halaman yang sedang ditampilkan beserta dasar penentuannya (jalur terjemahan, deteksi otomatis, atau bahasa bawaan proyek) akan ditampilkan.
2. Pilih bahasa yang ingin Anda baca.
   Terjemahan dari dokumen yang sama akan terbuka. Bahasa yang Anda pilih akan diingat, dan dokumen berikutnya yang Anda buka pun ditampilkan dalam bahasa itu apabila terjemahannya tersedia.

Daftar bahasa menunjukkan apakah dokumen tersebut memiliki terjemahan atau tidak.

| Tampilan | Arti |
|---|---|
| Ada terjemahan | Terjemahan tersedia dan dapat dibuka |
| Belum diterjemahkan | Bahasa ini didukung oleh proyek, tetapi dokumen ini belum memiliki terjemahan |
| Perlu diperbarui | Terjemahan tersedia, tetapi dokumen asli berubah setelah diterjemahkan |

> **Catatan**
>
> - Memilih bahasa hanya membuka terjemahan yang sudah ada. Tindakan ini tidak membuat terjemahan maupun berkas baru. Untuk membuat terjemahan, gunakan [Buat atau kelola terjemahan…] pada menu yang sama.
> - Bila bahasa halaman yang sedang ditampilkan dinilai berbeda dari bahasa bawaan proyek, sebuah peringatan akan ditampilkan. Pengaturan tidak akan diubah.

## Bahasa yang ditampilkan pertama kali

Saat dokumen dibuka, bahasa tampilan pertama ditentukan dengan urutan berikut.

1. Bahasa yang sebelumnya Anda pilih sendiri pada root dokumentasi ini. Pilihan tersebut disimpan (memilih bahasa bawaan pun disimpan sebagai sebuah pilihan).
2. Bahasa tampilan VS Code (pada versi peramban web, pengaturan bahasa peramban). Bahasa yang cocok dengan bahasa yang didukung akan dipilih secara otomatis. Bahasa dengan kode wilayah (seperti `en-US`) juga cocok dengan bahasa dasarnya (`en`).
3. Bahasa cadangan proyek (`fallbackLocale` pada `lunascape-docs.json`).
4. Bahasa bawaan proyek.

> **Tips**
>
> - Bila bahasa dipilih secara otomatis, bahasa aktif pada menu bahasa ditampilkan dengan keterangan “Dipilih otomatis”. Arahkan penunjuk ke lencana tersebut untuk melihat alasannya.
> - `fallbackLocale` adalah bahasa yang ditampilkan kepada pembaca yang bahasa lingkungannya tidak cocok dengan satu pun bahasa yang didukung. Pada proyek yang dokumen kanoniknya berbahasa Jepang dan memiliki versi bahasa Inggris, menetapkan `"en"` membuat versi bahasa Inggris terbuka bagi pembaca dengan lingkungan berbahasa Spanyol, misalnya. Bila tidak ditetapkan, bahasa bawaan yang digunakan.

## Tempat menyimpan terjemahan

Dokumen dalam bahasa bawaan tetap berada di tempatnya, sedangkan terjemahannya diletakkan di **`i18n/<bahasa>/` dalam folder yang sama**, dengan nama berkas yang sama.

```text
docs/
  README.md                  ← bahasa bawaan (misalnya bahasa Jepang)
  i18n/en/README.md          ← versi bahasa Inggrisnya
  guide/
    setup.md
    i18n/en/setup.md         ← versi bahasa Inggrisnya
```

> **Catatan**
>
> - Bentuk yang menyusun ulang struktur folder di bawah `i18n/` (`i18n/en/guide/setup.md`) tidak dikenali. Folder `i18n/` harus selalu berada dalam folder yang sama dengan dokumen tersebut.
> - Hanya satu tempat itulah tujuan penyelesaian terjemahan. Meletakkan terjemahan dokumen yang sama pada `i18n/` di folder induk tidak menimbulkan pertentangan “mana yang diutamakan”; berkas di sisi induk itu menjadi berkas terlantar yang tidak muncul di menu bahasa maupun di buku besar (dan tidak dihapus secara otomatis). Jangan menaruh terjemahan yang sama di dua tempat.

## Jika membaca di versi peramban web

Pada versi peramban web pun, bahasa dapat diganti dengan cara yang sama apabila terjemahannya tersedia. Bila Anda ingin membaca dalam bahasa yang belum memiliki terjemahan, Anda dapat menggunakan fitur terjemahan halaman pada peramban. Kode, rumus, dan diagram dikecualikan dari terjemahan tersebut.

## Topik terkait

- [Menyerahkan pekerjaan kepada AI](../05-ai/README.md)
- [Pekerjaan yang dapat diserahkan](../05-ai/tasks.md)
- [Mengubah pengaturan tampilan](../02-reading/display-settings.md)
