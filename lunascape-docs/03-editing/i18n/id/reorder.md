# Mengubah urutan dokumen

Urutan yang ditampilkan di INDEX dapat diubah dengan seret dan lepas atau melalui papan ketik. Urutan yang diubah disimpan di front matter dokumen sebagai `navigation.order`.

## Mengubah urutan dengan seret dan lepas

1. Seret dokumen atau folder di INDEX.
2. Lepaskan sebelum atau sesudah item yang sejajar, atau di atas sebuah folder.
   Di dalam tingkat yang sama, urutannya berubah. Jika dilepaskan ke folder lain, item dipindahkan ke folder tersebut.

## Mengubah urutan dengan papan ketik atau menu

- Tempatkan fokus pada item INDEX, lalu tekan `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Pilih [Pindahkan ke atas] / [Pindahkan ke bawah] pada menu item.

## Isi yang disimpan

- Saat urutan diubah dalam tingkat yang sama, `navigation.order` pada front matter dokumen kanonik diperbarui. Untuk folder, nilai itu ditulis ke `README.md` folder tersebut. Pada folder yang tidak memiliki `README.md`, sebuah `README.md` berisi front matter saja akan dibuat.
- Saat dipindahkan ke folder lain, dokumen kanonik dan versi terjemahannya dipindahkan bersama-sama. Sebelum pemindahan, muncul konfirmasi mengenai pengaruhnya terhadap tautan relatif.
- Git tidak melakukan staging maupun commit.

> **Perhatian**
>
> - Urutan tidak dapat diubah saat penyaringan aktif, saat dokumen sedang disunting, dan pada ruang kerja yang tidak tepercaya.
> - Jika muncul "INDEX telah diperbarui", berarti perubahan lain baru saja diterapkan. Lakukan operasinya sekali lagi.
> - Halaman awal tidak dapat dipindahkan ke folder lain.

> **Tips**
>
> Jika `navigation.order` diberi nilai dengan kelipatan 100, seperti 100, 200, 300, dokumen akan lebih mudah disisipkan di antaranya nanti. Untuk keterangan lebih lanjut, lihat [Mengatur informasi navigasi](../04-document-tools/navigation-metadata.md).

## Topik terkait

- [Membuat dan menata dokumen serta folder](organize.md)
- [Mengatur informasi navigasi](../04-document-tools/navigation-metadata.md)
