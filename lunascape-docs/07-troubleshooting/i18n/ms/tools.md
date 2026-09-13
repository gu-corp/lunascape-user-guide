# Semakan, penciptaan atau terjemahan tidak berjaya

## Semakan

### "docs-lint tidak boleh digunakan" dipaparkan

- Persekitaran pelaksanaan docs-lint tiada dalam sambungan, atau terdapat masalah pada tetapan. Pasang semula sambungan.
- "Untuk memuatkan Pack tempatan dan tetapan dengan selamat, percayai ruang kerja ini dalam VS Code": ruang kerja dipercayai diperlukan untuk menggunakan Standard Pack tempatan.

### Keputusan kekal pada "perlu pengesahan semula"

Apabila dokumen atau tetapan diubah, keputusan sebelumnya menjadi tidak sah. Tekan [Semak akar dokumentasi] sekali lagi. Perubahan yang belum disimpan tidak disertakan.

### Menekan penemuan tidak membuka apa-apa

Item "Seluruh akar dokumentasi" tidak terikat pada dokumen tertentu, jadi tidak mempunyai kedudukan. Ikut kandungan penemuan itu dan semak dokumen yang berkenaan.

### Peraturan tidak boleh disimpan

- Ruang kerja dipercayai diperlukan.
- "Tetapan Lint telah diubah oleh operasi lain": `docs-lint.config.json` telah diubah dari luar. Muatkan keadaan terkini, kemudian cuba lagi.
- Fail tetapan yang merupakan pautan simbolik, atau yang berada di luar akar dokumentasi, tidak boleh disunting.

## Penciptaan daripada templat

- "Pratonton templat telah tamat tempoh" / "Kandungan input telah berubah": tekan [Pratonton] sekali lagi sebelum mencipta.
- "Dokumen di destinasi simpanan sudah wujud": fail sedia ada tidak ditulis ganti. Tentukan destinasi simpanan yang lain.
- Destinasi simpanan memerlukan laluan relatif dari akar dokumentasi dan sambungan fail `.md` / `.mdx`. Dokumen tidak boleh dicipta di bawah `i18n`.
- "Percayai ruang kerja untuk mencipta dokumen": percayai ruang kerja itu dalam VS Code.

<!-- ai-only:start -->
## Terjemahan

### Butang terjemahan tidak boleh ditekan

- "Terjemahan AI tidak diaktifkan untuk akar dokumentasi ini": tetapkan `translation.enabled` kepada `true` dalam `lunascape-docs.json`.
- "Bahasa lalai projek belum ditetapkan": simpan bahasa lalai melalui [Menukar tetapan paparan](../02-reading/display-settings.md).
- "Tambahkan bahasa sasaran ke dalam bahasa yang disokong": tambah bahasa sasaran terjemahan ke dalam `locales`.
- "Dokumen kanonik untuk diterjemah tidak dijumpai": halaman terjemahan sedang dibuka. Tukar ke halaman bahasa lalai.
- Terjemahan pukal tidak boleh digunakan dalam paparan folder sementara. Letakkan `lunascape-docs.json` dalam folder itu untuk menjadikannya akar dokumentasi.

### Cadangan terjemahan ditolak atau perlu dijana semula

- "Dokumen kanonik telah berubah. Jana semula cadangan terjemahan": dokumen kanonik atau sasaran terjemahan berubah selepas cadangan itu dibuat. Terjemah sekali lagi.
- Jika respons model bahasa kehilangan pengecam atau kod yang perlu dilindungi, respons itu tidak diterima. Kandungan respons boleh disemak dalam panel output "Lunascape Docs Terjemahan".
- "Terjemahan pukal terhad kepada 1000 dokumen setiap kali": bahagikan skop mengikut folder atau pilihan yang dinyatakan.
<!-- ai-only:end -->

## Topik berkaitan

- [Menyemak dokumen](../04-document-tools/check.md)
- [Mencipta dokumen daripada templat](../04-document-tools/templates.md)
- [Menyerahkan kerja kepada AI](../05-ai/README.md)
