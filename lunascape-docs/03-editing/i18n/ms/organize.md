# Mencipta dan menyusun dokumen dan folder

Daripada menu item INDEX, anda boleh mencipta, menyalin, menukar nama dan memadam dokumen serta folder. Input dilakukan dalam dialog kecil di dalam pemapar, tanpa mengganggu bacaan.

> **Perhatian**
>
> Tindakan ini hanya boleh digunakan apabila ruang kerja dipercayai dalam VS Code. Tindakan ini tidak boleh dijalankan semasa dokumen sedang disunting, semasa operasi lain sedang diproses, atau apabila sasaran mempunyai perubahan yang belum disimpan.

## Mencipta dokumen atau folder

1. Buka menu item ([⋯] atau klik kanan) bagi folder destinasi.
   Untuk mencipta terus di bawah akar dokumentasi, gunakan [⋯] di hujung kanan tajuk INDEX atau klik kanan pada bahagian kosong INDEX.
2. Pilih [Dokumen baharu] atau [Folder baharu].
3. Masukkan nama dan tekan [Cipta].
   Nama dokumen memerlukan sambungan Markdown (`.md`, `.markdown`, `.mdx` dan sebagainya).

Dokumen baharu dicipta sebagai dokumen bahasa lalai (dokumen kanonik).

## Menyalin dokumen

1. Buka menu item dokumen dan pilih [Salin].
2. Masukkan nama baharu dan tekan [Cipta].

Hanya dokumen kanonik yang disalin. Versi terjemahan tidak disalin.

## Menukar tajuk

Menukar tajuk dokumen (H1). Nama fail tidak berubah.

1. Buka menu item dokumen atau folder dan pilih [Tukar tajuk].
2. Masukkan tajuk baharu dalam satu baris dan tekan [Tukar].

Bagi folder, tajuk `README.md` folder tersebut yang ditukar. Apabila versi terjemahan sedang dipaparkan, tajuk dokumen dalam bahasa itulah yang berubah.

## Menukar nama dokumen

Menukar nama dokumen yang dipaparkan pada bar alat (nama akar dokumentasi).

1. Klik kanan nama dokumen pada bar alat. Menu yang sama boleh dibuka daripada [⋯] di hujung kanan tajuk INDEX.
2. Pilih [Tukar nama dokumen] dan masukkan nama baharu.

Selagi tiada tetapan dibuat, nama folder dipaparkan seadanya.

Nama yang ditukar ditulis ke **tempat yang kini digunakan sebagai nama dokumen**. Nama tidak ditulis ke tempat yang tidak digunakan untuk paparan, supaya tajuk yang kelihatan tidak diabaikan.

| Keadaan semasa | Ditulis ke |
|---|---|
| `lunascape-docs.json` mempunyai nama | `lunascape-docs.json` dikemas kini |
| Tiada nama, tetapi akar dokumentasi mempunyai README | Tajuk README (H1) ditulis semula |
| Kedua-duanya tiada | `lunascape-docs.json` dicipta dan disimpan |

Tempat yang ditulis dinyatakan dalam mesej selepas perubahan.

> **Petua**
>
> Nama dokumen ditentukan mengikut susunan ini: nama dalam `lunascape-docs.json`, kemudian tajuk README akar dokumentasi, kemudian nama folder.

## Menukar nama fail atau nama folder

1. Buka menu item dan pilih [Tukar nama fail] atau [Tukar nama folder].
2. Masukkan nama baharu dan tekan [Tukar].

Versi terjemahan yang berkaitan (laluan yang sama di bawah `i18n/<bahasa>/`) turut ditukar bersama.

## Memadam

1. Buka menu item dan pilih [Alih ke tong sampah].
2. Semak kandungan mesej pengesahan dan luluskan pemindahan itu.

Sasaran dialihkan ke tong sampah sistem pengendalian, jadi ia boleh dipulihkan jika perlu. Versi terjemahan tidak dipadam dan kekal seperti sedia ada.

## Nama yang tidak boleh digunakan

- Nama yang bermula dengan `.` (kerana ia tidak dipaparkan dalam INDEX)
- `i18n` (dikhaskan untuk fail terjemahan)
- Nama yang dikhaskan oleh Windows (`CON`, `PRN` dan sebagainya)
- Nama yang berakhir dengan noktah atau ruang kosong
- Nama yang mengandungi aksara kawalan atau aksara yang tidak boleh digunakan dalam nama fail
- Nama yang sudah wujud dalam folder yang sama (termasuk nama yang berbeza hanya pada huruf besar dan huruf kecil)

> **Perhatian**
>
> Halaman mula (biasanya `README.md` pada akar) tidak boleh ditukar nama atau dialihkan. Tukar `startPage` dalam `lunascape-docs.json` terlebih dahulu.

## Topik berkaitan

- [Menukar susunan dokumen](reorder.md)
- [Menggunakan INDEX](../02-reading/index-panel.md)
