# Mengatur informasi navigasi

Nama dan urutan yang ditampilkan di INDEX ditulis pada YAML front matter setiap dokumen. Tanpa itu pun dokumen tetap ditampilkan, dengan memakai judul (H1) dan urutan nama berkas.

## Nama dan urutan dokumen

Tulis seperti berikut di bagian awal dokumen.

```yaml
---
navigation:
  title: Memulai
  order: 200
---
```

| Item | Isi |
|---|---|
| `navigation.title` | Nama yang ditampilkan di INDEX. Jika dihilangkan, H1 yang dipakai; jika itu pun tidak ada, nama berkas |
| `navigation.order` | Bilangan bulat yang menentukan urutan. Diurutkan dari yang terkecil. Jika dihilangkan, berlaku urutan bawaan yang stabil (menurut nama berkas) |

> **Petunjuk**
>
> - Berilah `order` dengan kelipatan 100, seperti 100, 200, 300, agar nanti Anda dapat menyisipkan 150 di antaranya.
> - Nilai `order` yang tidak ditentukan, tidak sah, atau ganda tidak akan menyembunyikan dokumen.
> - Saat Anda mengubah urutan di INDEX, `navigation.order` ditulis secara otomatis. Anda tidak perlu menulisnya sendiri.

## Nama dan urutan folder

Nama dan urutan sebuah folder berada pada front matter `README.md` folder tersebut (atau `index.md` bila tidak ada). Halaman muka tidak harus memiliki isi.

```yaml
---
navigation:
  title: Perencanaan produk
  order: 100
---
```

Folder tanpa halaman muka ditampilkan dengan nama folder dan urutan bawaan. Bila perubahan judul atau pengubahan urutan di INDEX memerlukannya, sebuah `README.md` yang hanya berisi front matter akan dibuat. Membaca saja tidak pernah membuat berkas.

## Penanganan pada versi terjemahan

- Urutan, serta peran folder (halaman muka atau khusus pengaturan), hanya ditentukan oleh dokumen dalam bahasa bawaan.
- Versi terjemahan hanya dapat menimpa `navigation.title`. Bila dokumen kanonik memiliki isi, H1 versi terjemahan juga dipakai sebagai nama.
- Terjemahan yang berdiri sendiri tidak menambah halaman.

## Urutan dan pelipatan item anak

Pada halaman muka folder, tersedia `navigation.children.sort` dan `navigation.children.defaultCollapsed` untuk menentukan cara pengurutan item anak langsung serta keadaan terlipat pada awalnya. Pembacaan dan penyuntingannya di VS Code akan didukung kemudian.

## Topik terkait

- [Mengubah urutan dokumen](../03-editing/reorder.md)
- [Root dokumentasi dan konvensi berkas](structure.md)
