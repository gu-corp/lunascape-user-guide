# Tugas yang boleh diserahkan

Pilih daripada [Tugas] dalam tab [AI]. Setiap tugas mengubah arahan yang diserahkan dan semakan yang dijalankan selepasnya.

| Tugas | Kandungan | Keperluan | Jenis API |
|---|---|---|---|
| Terjemah halaman ini | Menterjemah dokumen yang sedang dipaparkan ke bahasa yang dipilih | Dokumen sasaran dibuka, bahasa sasaran | ○ |
| Terjemah sekali gus yang belum diterjemah | Menterjemah dokumen yang belum diterjemah dan yang perlu dikemas kini bagi bahasa yang dipilih, satu demi satu | Bahasa sasaran | Jenis sesi sahaja |
| Baca pruf halaman ini | Menyemak dan membetulkan istilah, gaya bahasa, dan susunan bab yang dikehendaki oleh standard dokumen | Dokumen sasaran dibuka | ○ |
| Cipta dokumen baharu | Mencipta dokumen baharu mengikut standard dokumen dan templat | Subjek (boleh diabaikan) | Jenis sesi sahaja |

## Apa yang terkandung dalam arahan

| Bil. | Kandungan |
|---|---|
| 1 | Lokasi akar dokumentasi. Arahan diberi supaya tiada apa-apa di luarnya diubah |
| 2 | Bahasa lalai (dokumen kanonik), dan tempat versi terjemahan disimpan (folder `i18n/<bahasa>/` dalam folder yang sama dengan dokumen) |
| 3 | `navigation.order` hanya dimiliki oleh dokumen kanonik, dan versi terjemahan hanya boleh menindih `navigation.title` sahaja |
| 4 | ID keperluan, pautan, kod, Mermaid, TeX dan struktur front matter tidak boleh diubah |
| 5 | Standard dokumen dan glosari (`terminology` dalam `docs-lint.config.json`) |
| 6 | Selepas selesai, jalankan semakan dokumen, laporkan fail yang diubah, dan jangan lakukan sebarang operasi Git |

> **Petua**
>
> Sasaran bagi "Terjemah sekali gus yang belum diterjemah" diambil daripada lejar, sehingga 200 dokumen setiap kali. Jalankannya berulang kali jika dokumennya banyak.

## Perkara berkaitan

- [Menyerahkan kerja kepada AI](README.md)
- [Lejar dan rekod](ledger.md)
