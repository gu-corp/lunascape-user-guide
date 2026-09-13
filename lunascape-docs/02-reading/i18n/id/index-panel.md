# Menggunakan INDEX

INDEX di sebelah kiri layar adalah pohon folder dan dokumen yang ada di root dokumentasi.

## Menyaring

1. Ketik kata pada [Saring dokumen] di atas INDEX.
2. Hanya item dengan nama dokumen yang cocok yang ditampilkan. Hapus isian untuk kembali seperti semula.

> **Perhatian**
>
> Selama penyaringan aktif, pengurutan dengan seret dan lepas tidak dapat dilakukan.

## Membuka dan menutup folder

- Tekan panah di sebelah kiri nama folder, atau nama folder yang tidak memiliki halaman sampul, untuk membuka atau menutupnya.
- Folder yang memiliki halaman sampul (`README.md` atau `index.md` yang berisi teks) akan membuka halaman sampul itu saat namanya ditekan. Untuk sekadar membuka atau menutup, gunakan [Buka folder] / [Tutup folder] pada menu item.
- Status buka-tutup folder diingat untuk setiap pengguna dan tidak ditulis ke berkas yang dikelola Git.

## README dan halaman sampul folder

`README.md` adalah berkas yang menjelaskan isi folder tersebut.

- Pada folder yang memiliki README, menekan nama folder akan menampilkan README itu.
- Folder tanpa README akan menampilkan dokumen teratas di dalamnya.
- Judul (H1) pada README menjadi nama folder tersebut di INDEX.

README tidak wajib ada. Untuk menambahkannya kemudian, pilih [Buat README] pada menu item folder (hanya muncul pada folder yang belum memiliki README).

## Menampilkan atau menyembunyikan INDEX

- Ikon sebelah kiri pada kontrol kolom di bilah alat menampilkan atau menyembunyikan INDEX. Ikon sebelah kanan menampilkan atau menyembunyikan "Di halaman ini".
- Saat layar sempit, INDEX dimulai dalam keadaan tertutup. Tekan [Buka INDEX] (tiga garis) yang muncul di sebelah kiri [Kembali], maka INDEX terbuka menumpuk di atas teks dokumen. Tutup dengan [×] di dalam INDEX, klik pada latar, `Esc`, atau dengan berpindah dokumen. Buka-tutup sementara ini tidak mengubah pengaturan pada layar lebar.
- Pada root dokumentasi yang hanya menampilkan satu dokumen, INDEX menutup sendiri pada kali pertama saja. Anda dapat membukanya lagi dengan ikon kolom. Perilaku ini dapat dimatikan melalui [Sembunyikan jika dokumen hanya satu] pada [Pengaturan tampilan].

## Menggunakan menu item

Buka menu sebuah item dengan [⋯] yang muncul saat penunjuk diarahkan ke item INDEX, atau dengan klik kanan pada item tersebut. Item tersusun dalam urutan berikut.

| Grup | Item |
|---|---|
| Tindakan yang sering dipakai | [Buka folder] / [Tutup folder], [Buka INDEX] (membuka halaman sampul folder), [Edit], [Ubah judul], [Buka di VS Code], [Salin path] |
| Membuat dan menata | [Buat README] (hanya folder tanpa README), [Dokumen baru], [Folder baru], [Duplikat], [Ubah nama berkas] / [Ubah nama folder], [Pindahkan ke atas], [Pindahkan ke bawah] |
| Menghapus | [Pindahkan ke tempat sampah] |

- Untuk membuat langsung di bawah root dokumentasi, tekan [⋯] di ujung kanan judul INDEX, atau klik kanan pada bagian kosong INDEX, lalu pilih [Dokumen baru] atau [Folder baru]. Pada menu yang sama terdapat [Ubah nama dokumen] dan, jika root dokumentasi belum memiliki README, [Buat README]. Klik kanan pada nama dokumen di bilah alat juga membuka menu yang sama.
- Di dalam menu, `↑` `↓` untuk berpindah antaritem, dan `Home` `End` untuk melompat ke item pertama dan terakhir. Menutup dengan `Esc` mengembalikan fokus ke posisi sebelum menu dibuka.

> **Perhatian**
>
> Item untuk membuat, menata, dan menghapus hanya muncul jika ruang kerja tepercaya di VS Code. Item tersebut juga tidak dapat dipakai selagi dokumen sedang diedit atau selagi operasi INDEX lain sedang diproses.

## Mengubah tampilan

Melalui [Pengaturan tampilan], Anda dapat mengubah tampilan nama berkas, ikon dokumen dan folder, jumlah item di dalam folder, garis panduan hierarki, serta kerapatan tampilan. Untuk keterangan lebih lanjut, lihat [Mengubah pengaturan tampilan](display-settings.md).

## Topik terkait

- [Membuat dan menata dokumen serta folder](../03-editing/organize.md)
- [Mengubah urutan dokumen](../03-editing/reorder.md)
