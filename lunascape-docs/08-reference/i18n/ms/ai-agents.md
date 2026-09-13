# Penggunaan daripada AI

Sambungan ini mendaftarkan Language Model Tool baca sahaja `lunascape_getDocsSpecification` pada VS Code. Apabila ejen VS Code yang serasi ditanya tentang fungsi, tetapan atau konvensyen dokumen Lunascape Docs, ejen tersebut boleh mendapatkan kandungan bantuan ini (spesifikasi umum) melalui alat ini.

## Cara penggunaan

Bertanya dalam sembang VS Code dengan menyertakan `#lunascapeDocs`, atau terus bertanya tentang tetapan atau struktur dokumen Lunascape Docs.

```text
#lunascapeDocs Bagaimanakah cara mengaktifkan terjemahan bahasa Inggeris dalam lunascape-docs.json?
```

## Argumen alat

| Argumen | Kandungan |
|---|---|
| `topic` | Bab yang hendak diambil: `all`, `usage` (Operasi asas), `structure` (Akar dokumentasi dan konvensyen fail), `editing` (Menyunting dokumen), `configuration` (Tetapan projek), `security` (Keselamatan dan sempadan penyimpanan), `ai` (Penggunaan daripada AI) |
| `locale` | Bahasa bantuan (teg bahasa bantuan yang disertakan, seperti `ja` atau `en`). Jika ditinggalkan, bahasa paparan VS Code akan digunakan; jika tiada, bantuan bahasa Jepun dikembalikan |

> **Perhatian**
>
> - Alat ini tidak menghantar kandungan dokumen ke luar.
> - Alat ini tidak mengembalikan nama ruang kerja atau laluan tempatan.
> - Alat ini tidak mengubah fail.
> - Ia boleh digunakan daripada ejen VS Code yang serasi walaupun tanpa `AGENTS.md`. Ia tidak dikongsi secara automatik dengan klien AI lain yang tidak menggunakan API alat sambungan ini.

## Topik berkaitan

- [Memaparkan bantuan](../02-reading/help.md)
- [Keselamatan dan sempadan penyimpanan](security.md)
