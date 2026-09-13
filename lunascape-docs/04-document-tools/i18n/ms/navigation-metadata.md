# Menetapkan maklumat navigasi

Nama dan susunan yang dipaparkan dalam INDEX ditulis dalam YAML front matter setiap dokumen. Tanpanya pun dokumen tetap dipaparkan, dengan menggunakan tajuk (H1) dan susunan nama fail.

## Nama dan susunan dokumen

Tulis yang berikut di bahagian atas dokumen.

```yaml
---
navigation:
  title: Permulaan
  order: 200
---
```

| Perkara | Kandungan |
|---|---|
| `navigation.title` | Nama yang dipaparkan dalam INDEX. Jika ditinggalkan, H1 digunakan; jika tiada juga, nama fail digunakan |
| `navigation.order` | Integer yang menentukan susunan. Disusun daripada nilai terkecil. Jika ditinggalkan, susunan lalai yang stabil (mengikut nama fail) digunakan |

> **Petua**
>
> - Berikan nilai `order` dalam selang 100, seperti 100, 200, 300, supaya anda boleh menyisipkan 150 di antaranya kemudian.
> - Nilai `order` yang tiada, tidak sah atau berulang tidak akan menyembunyikan dokumen.
> - Apabila anda menyusun semula dalam INDEX, `navigation.order` ditulis secara automatik. Anda tidak perlu menulisnya dengan tangan.

## Nama dan susunan folder

Nama dan susunan sesebuah folder dipegang oleh front matter `README.md` folder tersebut (atau `index.md` jika tiada README). Halaman muka depan tidak semestinya mempunyai kandungan badan.

```yaml
---
navigation:
  title: Perancangan produk
  order: 100
---
```

Folder tanpa halaman muka depan dipaparkan dengan nama folder dan susunan lalai. Apabila perubahan tajuk atau penyusunan semula dalam INDEX memerlukannya, `README.md` yang mengandungi front matter sahaja akan dicipta. Membaca sahaja tidak akan mencipta fail.

## Pengendalian dalam versi terjemahan

- Susunan, dan peranan folder (halaman muka depan atau khusus tetapan), ditentukan oleh dokumen bahasa lalai sahaja.
- Versi terjemahan hanya boleh menggantikan `navigation.title`. Apabila dokumen kanonik mempunyai kandungan badan, H1 versi terjemahan turut digunakan sebagai nama.
- Versi terjemahan sahaja tidak akan menambah halaman.

## Susunan dan pelipatan item anak

Dalam halaman muka depan folder, `navigation.children.sort` dan `navigation.children.defaultCollapsed` ditakrifkan untuk menentukan cara item anak di bawahnya disusun dan keadaan lipatan awalnya. Pembacaan dan penyuntingannya dalam VS Code akan disokong kemudian.

## Topik berkaitan

- [Menukar susunan dokumen](../03-editing/reorder.md)
- [Akar dokumentasi dan konvensi fail](structure.md)
