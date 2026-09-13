# Pemeriksaan, pembuatan, atau terjemahan tidak berjalan dengan baik

## Pemeriksaan

### Muncul "docs-lint tidak tersedia"

- Lingkungan eksekusi docs-lint tidak disertakan dalam ekstensi, atau ada masalah pada pengaturan. Pasang ulang ekstensi.
- "Untuk memuat Pack lokal dan pengaturan dengan aman, percayai ruang kerja ini di VS Code": untuk memakai Standard Pack lokal, diperlukan ruang kerja tepercaya.

### Hasil tetap "perlu divalidasi ulang"

Jika dokumen atau pengaturan diubah, hasil sebelumnya menjadi tidak berlaku. Tekan [Periksa root dokumentasi] sekali lagi. Perubahan yang belum disimpan tidak ikut diperhitungkan.

### Temuan tidak terbuka saat ditekan

Butir "seluruh root dokumentasi" tidak terkait dengan dokumen tertentu sehingga tidak memiliki posisi. Periksa dokumen yang bersangkutan sesuai isi temuan.

### Aturan tidak dapat disimpan

- Diperlukan ruang kerja tepercaya.
- "Pengaturan Lint diubah oleh operasi lain": `docs-lint.config.json` diubah dari luar. Muat keadaan terbaru, lalu ulangi.
- Berkas pengaturan yang berupa tautan simbolik atau yang berada di luar root dokumentasi tidak dapat disunting.

## Pembuatan dari templat

- "Pratinjau templat sudah kedaluwarsa" atau "Isi masukan telah berubah": tekan [Pratinjau] sekali lagi, lalu buat dokumennya.
- "Dokumen pada tujuan penyimpanan sudah ada": berkas yang sudah ada tidak ditimpa. Tentukan tujuan penyimpanan lain.
- Tujuan penyimpanan memerlukan jalur relatif dari root dokumentasi serta ekstensi `.md` / `.mdx`. Dokumen tidak dapat dibuat di bawah `i18n`.
- "Percayai ruang kerja untuk membuat dokumen": percayai ruang kerja tersebut di VS Code.

<!-- ai-only:start -->
## Terjemahan

### Tombol terjemahan tidak dapat ditekan

- "Terjemahan AI tidak diaktifkan pada root dokumentasi ini": setel `translation.enabled` pada `lunascape-docs.json` menjadi `true`.
- "Bahasa bawaan proyek belum ditetapkan": simpan bahasa bawaan melalui [Mengubah pengaturan tampilan](../02-reading/display-settings.md).
- "Tambahkan bahasa tujuan ke bahasa yang didukung": tambahkan bahasa tujuan terjemahan ke `locales`.
- "Dokumen kanonik untuk diterjemahkan tidak ditemukan": yang terbuka adalah halaman versi terjemahan. Beralihlah ke halaman dalam bahasa bawaan.
- Terjemahan sekaligus tidak dapat dipakai saat folder ditampilkan secara sementara. Letakkan `lunascape-docs.json` pada folder itu agar menjadi root dokumentasi.

### Usulan terjemahan ditolak atau diminta dibuat ulang

- "Dokumen kanonik telah berubah. Buat ulang usulan terjemahan": setelah usulan dibuat, dokumen kanonik atau bahasa tujuan berubah. Terjemahkan sekali lagi.
- Jika respons model bahasa kehilangan pengenal atau kode yang harus dilindungi, respons tersebut tidak diterima. Isi respons dapat diperiksa pada panel keluaran "Lunascape Docs Terjemahan".
- "Terjemahan sekaligus dibatasi 1000 dokumen per sekali jalan": bagi cakupannya per folder atau dengan memilih dokumen secara eksplisit.
<!-- ai-only:end -->

## Topik terkait

- [Memeriksa dokumen](../04-document-tools/check.md)
- [Membuat dokumen dari templat](../04-document-tools/templates.md)
- [Menyerahkan pekerjaan kepada AI](../05-ai/README.md)
