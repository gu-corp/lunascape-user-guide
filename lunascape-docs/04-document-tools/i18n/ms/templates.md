# Mencipta dokumen daripada templat

Dalam tab [Cipta] pada Alat Dokumen, anda boleh memilih templat, membuat pratonton kandungannya, kemudian mencipta dokumen baharu.

1. Tekan [Alat Dokumen] pada bar alat, kemudian buka tab [Cipta].
2. Tekan [Cipta daripada templat], kemudian pilih satu templat.
3. Isikan medan input (tajuk, ringkasan dan sebagainya). Medan yang wajib diisi ditandakan dengan "Wajib".
4. Masukkan destinasi simpanan sebagai laluan relatif daripada akar dokumentasi (contohnya `03-design/api.md`).
5. Tekan [Pratonton], kemudian semak Markdown yang dijana.
6. Tekan [Cipta ini].
   Dokumen dicipta dan dipaparkan dalam pemapar. Seterusnya, semakan ke atas keseluruhan akar dokumentasi dijalankan.

## Templat yang boleh dipilih

| Templat | Kandungan |
|---|---|
| Dokumen satu halaman | Mencipta spesifikasi ringkas, nota atau dokumen penerangan tunggal dalam satu fail |
| Spesifikasi, manual, bantuan | Mencipta satu fail dengan susunan bab umum yang sesuai untuk spesifikasi, manual atau bantuan |
| Templat Standard Pack | Apabila Standard Pack dipilih dalam `lunascape-docs.json`, jenis dokumen yang boleh digunakan dengan profil tersebut (dokumen keperluan, dokumen reka bentuk dan sebagainya) turut ditambah |

> **Nota**
>
> - Ruang kerja dipercayai diperlukan untuk mencipta dokumen.
> - Fail sedia ada tidak ditulis ganti. Dokumen tidak dapat dicipta jika sudah ada dokumen dengan nama yang sama di destinasi simpanan.
> - Destinasi simpanan memerlukan sambungan `.md` atau `.mdx`. Dokumen tidak boleh dicipta di bawah `i18n` (lokasi versi terjemahan).
> - Selepas mengubah input, tekan [Pratonton] sekali lagi sebelum mencipta dokumen.

> **Petua**
>
> Dalam projek yang belum mempunyai folder dokumen, anda boleh mencipta set pertama dengan "Lunascape Docs: Cipta dokumentasi daripada templat" dalam Palet Perintah. Rujuk [Mencipta dokumen pertama anda](../01-introduction/first-documents.md).

## Topik berkaitan

- [Menggunakan Alat Dokumen](README.md)
- [Menukar peraturan semakan](rules.md)
