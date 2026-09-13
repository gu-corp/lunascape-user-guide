# Menyerahkan kerja kepada AI

Lunascape Docs tidak memanggil model bahasa. Ia menyediakan **konteks, alat dan semakan**, dan menyerahkan kerja menterjemah, menyemak dan mengarang kepada AI yang anda gunakan.

## Cara ia difikirkan

| Yang disediakan oleh produk | Kandungan |
|---|---|
| Konteks | Konvensyen dokumentasi (tempat versi terjemahan disimpan, front matter, piawaian dokumen, glosari) dan kedudukan dokumen sasaran |
| Alat kerja | Lejar bagi terjemahan yang belum diterjemah dan perlu dikemas kini, membaca dan menulis dokumen, penciptaan daripada templat |
| Semakan selepas kerja | Pengesahan oleh docs-lint, serta beza liputan dan kesegaran |

Teks arahan tidak mengandungi isi dokumen. AI membaca fail itu sendiri, menulisnya sendiri, dan mengesahkannya sendiri.

## Menyerahkan kerja

1. Tekan [Alat Dokumen] pada bar alat, kemudian buka tab [AI].
2. Pilih kerja yang hendak diserahkan daripada [Kerja].
3. Isikan perkara yang diperlukan (bahasa sasaran, subjek).
4. Tekan [Serahkan kerja ini].
   Terminal VS Code akan terbuka, dan AI yang anda pilih menerima arahan itu lalu memulakan kerja.

> **Petua**
>
> Sesi Claude Code disertai alat kerja (pelayan MCP `lunascape-docs`). Sesi itu boleh mendapatkan senarai belum diterjemah dan perlu dikemas kini, menjalankan docs-lint, dan merekodkan kesegaran selepas terjemahan dengan sendirinya.

## Menyemak hasilnya

| Bentuk pembekal | Tempat hasilnya mendarat |
|---|---|
| Jenis sesi (Claude Code, Codex) | Menulis terus ke pokok kerja. **Sila semak dalam beza Git** |
| Jenis API (model bahasa VS Code, Anthropic, serasi OpenAI) | Mengembalikan cadangan satu dokumen pada satu masa. Semak dengan [Buka beza], kemudian tulis dengan [Simpan] |

### Menyemak cadangan jenis API

Apabila dijalankan dengan jenis API, cadangan akan sampai ke tab [AI].

1. Tekan [Buka beza] dan bandingkan dengan kandungan semasa.
2. Jika ia memuaskan, tekan [Simpan]. Bagi terjemahan, kesegarannya turut direkodkan. Jika hendak membatalkannya, tekan [Buang].
   Untuk menghentikan penjanaan di pertengahan, tekan [Henti].

> **Nota**
>
> - Lunascape Docs tidak sekali-kali melakukan pementasan atau komit Git. Sentiasa semak perubahan dalam beza.
> - Kerja tidak boleh diserahkan dalam ruang kerja yang tidak dipercayai, atau semasa memaparkan folder sementara di luar akar dokumentasi.

## Topik berkaitan

- [Kerja yang boleh diserahkan](tasks.md)
- [Tetapan AI](settings.md)
- [Lejar dan rekodnya](ledger.md)
