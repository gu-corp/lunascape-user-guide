# Menggunakan INDEX

INDEX di sebelah kiri skrin ialah pepohon folder dan dokumen yang terdapat dalam akar dokumentasi.

## Menapis

1. Taipkan perkataan pada [Tapis dokumen] di bahagian atas INDEX.
2. Hanya item yang namanya sepadan akan dipaparkan. Kosongkan medan itu untuk kembali seperti asal.

> **Perhatian**
>
> Semasa penapis aktif, susunan tidak boleh diubah dengan seret dan lepas.

## Membuka dan menutup folder

- Tekan anak panah di sebelah kiri nama folder, atau nama folder yang tiada halaman muka, untuk membuka atau menutupnya.
- Folder yang mempunyai halaman muka (`README.md` atau `index.md` yang berisi teks) akan membuka halaman itu apabila namanya ditekan. Untuk membuka atau menutup sahaja, gunakan [Buka folder] / [Tutup folder] dalam menu item.
- Keadaan buka atau tutup folder diingati bagi setiap pengguna dan tidak ditulis ke dalam fail yang diurus oleh Git.

## README dan halaman muka folder

`README.md` ialah fail yang menerangkan isi kandungan folder tersebut.

- Bagi folder yang mempunyai README, menekan nama folder akan memaparkan README itu.
- Bagi folder yang tiada README, dokumen teratas di dalamnya akan dipaparkan.
- Tajuk (H1) dalam README menjadi nama folder itu dalam INDEX.

README tidak diwajibkan. Untuk menambahnya kemudian, pilih [Cipta README] dalam menu item folder (pilihan ini hanya muncul bagi folder yang tiada README).

## Menunjukkan atau menyembunyikan INDEX

- Ikon sebelah kiri pada kawalan lajur dalam bar alat menunjukkan atau menyembunyikan INDEX. Ikon sebelah kanan pula untuk "Pada halaman ini".
- Apabila skrin sempit, INDEX bermula dalam keadaan tertutup. Tekan [Buka INDEX] (tiga garis) di sebelah kiri [Kembali], dan INDEX akan terbuka bertindih di atas teks dokumen. Ia ditutup dengan [×] dalam INDEX, klik pada latar belakang, `Esc`, atau apabila anda berpindah dokumen. Keadaan sementara ini tidak mengubah tetapan bagi skrin lebar.
- Dalam akar dokumentasi yang hanya memaparkan satu dokumen, INDEX akan tertutup sendiri pada kali pertama sahaja. Ia boleh dibuka semula dengan ikon lajur. Kelakuan ini boleh dimatikan melalui [Sembunyikan jika hanya ada satu dokumen] dalam [Tetapan paparan].

## Menggunakan menu item

Tuding tetikus pada item INDEX untuk memaparkan [⋯], atau klik kanan pada item itu, bagi membuka menunya. Item disusun mengikut urutan berikut.

| Kumpulan | Item |
|---|---|
| Tindakan lazim | [Buka folder] / [Tutup folder], [Buka INDEX] (membuka halaman muka folder), [Edit], [Tukar tajuk], [Buka dalam VS Code], [Salin laluan] |
| Cipta dan susun | [Cipta README] (folder yang tiada README sahaja), [Dokumen baharu], [Folder baharu], [Salin], [Tukar nama fail] / [Tukar nama folder], [Alih ke atas satu], [Alih ke bawah satu] |
| Padam | [Alih ke tong sampah] |

- Untuk mencipta terus di bawah akar dokumentasi, tekan [⋯] di hujung kanan tajuk INDEX, atau klik kanan pada ruang kosong dalam INDEX, kemudian pilih [Dokumen baharu] atau [Folder baharu]. Menu yang sama turut memuatkan [Tukar nama dokumen] dan, jika akar dokumentasi tiada README, [Cipta README]. Klik kanan pada nama dokumen yang terpapar pada bar alat juga membuka menu yang sama.
- Dalam menu, `↑` `↓` menggerakkan pilihan, manakala `Home` `End` melompat ke item pertama dan terakhir. Menutupnya dengan `Esc` mengembalikan fokus ke kedudukan sebelum menu dibuka.

> **Perhatian**
>
> Item cipta, susun dan padam hanya dipaparkan apabila ruang kerja dipercayai dalam VS Code. Item itu juga tidak boleh digunakan semasa dokumen sedang diedit atau semasa operasi INDEX yang lain sedang diproses.

## Mengubah rupa paparan

Melalui [Tetapan paparan], anda boleh mengubah paparan nama fail, ikon dokumen dan folder, bilangan item dalam folder, garis panduan hierarki, serta kepadatan paparan. Untuk butiran, rujuk [Menukar tetapan paparan](display-settings.md).

## Topik berkaitan

- [Mencipta dan menyusun dokumen dan folder](../03-editing/organize.md)
- [Menukar susunan dokumen](../03-editing/reorder.md)
