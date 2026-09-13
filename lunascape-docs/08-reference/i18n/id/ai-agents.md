# Penggunaan dari AI

Ekstensi ini mendaftarkan Language Model Tool baca-saja `lunascape_getDocsSpecification` ke VS Code. Ketika agen VS Code yang kompatibel ditanya tentang fitur, pengaturan, atau konvensi dokumen Lunascape Docs, agen tersebut dapat mengambil isi bantuan ini (spesifikasi umum) melalui alat tersebut.

## Cara penggunaan

Ajukan pertanyaan di obrolan VS Code dengan menambahkan `#lunascapeDocs`, atau tanyakan saja tentang pengaturan atau struktur dokumen Lunascape Docs.

```text
#lunascapeDocs Bagaimana cara mengaktifkan terjemahan bahasa Inggris di lunascape-docs.json?
```

## Argumen alat

| Argumen | Isi |
|---|---|
| `topic` | Bab yang diambil: `all`, `usage` (Operasi dasar), `structure` (Root dokumentasi dan konvensi berkas), `editing` (Menyunting dokumen), `configuration` (Konfigurasi proyek), `security` (Keamanan dan batas penyimpanan), `ai` (Penggunaan dari AI) |
| `locale` | Bahasa bantuan (tag bahasa bantuan bawaan, seperti `ja` atau `en`). Jika dihilangkan, bahasa tampilan VS Code digunakan, dan jika tidak ada, bantuan bahasa Jepang yang dikembalikan |

> **Catatan**
>
> - Alat ini tidak mengirimkan isi dokumen ke luar.
> - Alat ini tidak mengembalikan nama ruang kerja maupun jalur lokal.
> - Alat ini tidak mengubah berkas.
> - Alat ini dapat digunakan dari agen VS Code yang kompatibel meskipun tanpa `AGENTS.md`. Alat ini tidak dibagikan secara otomatis kepada klien AI lain yang tidak menggunakan API alat ekstensi ini.

## Topik terkait

- [Menampilkan bantuan](../02-reading/help.md)
- [Keamanan dan batas penyimpanan](security.md)
