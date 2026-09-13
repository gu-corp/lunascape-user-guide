# Tugas yang dapat diserahkan

Pilih dari [Tugas] pada tab [AI]. Instruksi yang diserahkan dan pemeriksaan setelahnya berbeda untuk setiap tugas.

| Tugas | Isi | Yang diperlukan | Tipe API |
|---|---|---|---|
| Terjemahkan halaman ini | Menerjemahkan dokumen yang sedang ditampilkan ke bahasa yang dipilih | Dokumen sasaran sedang terbuka, bahasa sasaran | ○ |
| Terjemahkan sekaligus yang belum diterjemahkan | Menerjemahkan dokumen yang belum diterjemahkan dan yang perlu diperbarui untuk bahasa yang dipilih, satu per satu | Bahasa sasaran | Hanya tipe sesi |
| Koreksi halaman ini | Memeriksa dan memperbaiki istilah, gaya bahasa, serta susunan bab yang dituntut standar dokumen | Dokumen sasaran sedang terbuka | ○ |
| Buat dokumen baru | Membuat dokumen baru mengikuti standar dokumen dan templat | Pokok bahasan (boleh dikosongkan) | Hanya tipe sesi |

## Yang termuat dalam instruksi

| No. | Isi |
|---|---|
| 1 | Letak root dokumentasi. Ada instruksi untuk tidak mengubah apa pun di luarnya |
| 2 | Bahasa bawaan (dokumen kanonik) dan tempat versi terjemahan disimpan (`i18n/<bahasa>/` di folder yang sama dengan dokumen) |
| 3 | Bahwa `navigation.order` hanya dimiliki dokumen kanonik, dan versi terjemahan hanya boleh menimpa `navigation.title` |
| 4 | Bahwa ID persyaratan, tautan, kode, Mermaid, TeX, dan struktur front matter tidak boleh diubah |
| 5 | Standar dokumen dan glosarium (`terminology` dalam `docs-lint.config.json`) |
| 6 | Setelah selesai, menjalankan pemeriksaan dokumen, melaporkan file yang diubah, dan tidak melakukan operasi Git |

> **Tips**
>
> Sasaran "Terjemahkan sekaligus yang belum diterjemahkan" dibuat dari buku besar, paling banyak 200 dokumen sekali jalan. Jika jumlahnya lebih, jalankan berulang kali.

## Topik terkait

- [Menyerahkan pekerjaan ke AI](README.md)
- [Buku besar dan catatannya](ledger.md)
