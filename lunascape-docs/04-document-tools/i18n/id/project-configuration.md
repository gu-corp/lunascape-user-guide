# Pengaturan proyek

`lunascape-docs.json` yang berada tepat di bawah root dokumentasi adalah pengaturan root dokumentasi yang dibagikan dalam tim. Berkas ini dikelola dengan Git.

## Membuat atau mengedit berkas pengaturan

- Tekan [Alat Dokumen] pada bilah alat → tab [Pemeriksaan] → [Asal aturan dan pengaturan dokumen] → [Edit pengaturan dokumen], dan berkas akan terbuka di VS Code. Jika berkas belum ada, berkas awal dibuat pada saat itu.
- Nama berkas `lunascape-docs.json` otomatis dikaitkan dengan JSON Schema bawaan, sehingga pelengkapan otomatis dan penjelasan setiap item ditampilkan. Penulisan `$schema` tidak diperlukan.

## Contoh pengaturan

```json
{
  "id": "product-docs",
  "title": "Dokumentasi produk",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Penjelasan setiap item

| Item | Isi | Bawaan |
|---|---|---|
| `id` | Kunci untuk menyimpan pengaturan tampilan tiap pengguna. Berikan ID tetap bila Anda ingin pengaturan tetap terbawa meski folder dipindahkan | Jalur folder |
| `title` | Nama yang ditampilkan di ujung kiri bilah alat dan pada daftar root dokumentasi. Nama ini tidak berubah meski bahasa tampilan diganti | Judul README/index pada root; jika tidak ada, nama folder |
| `indexTitle` | Judul INDEX | `INDEX` |
| `startPage` | Dokumen yang pertama dibuka (jalur relatif dari root dokumentasi) | `README.md` |
| `appearance` | Skema warna. `light` (selalu terang) atau `auto` (mengikuti tema VS Code) | `light` |
| `defaultLocale` | Bahasa bawaan (bahasa dokumen kanonik). Ditentukan dengan tag bahasa BCP 47 (`ja`, `en`, `zh-Hant`, dan lain-lain). Bahasa ini menjadi sumber terjemahan | Tidak disetel (diperkirakan dari isi teks untuk tampilan) |
| `fallbackLocale` | Bahasa yang pertama ditampilkan kepada pembaca yang bahasa lingkungan bacanya tidak cocok dengan satu pun bahasa yang didukung. Tentukan bahasa yang tercakup dalam `locales` | Tidak disetel (memakai `defaultLocale`) |
| `locales` | Daftar bahasa yang didukung. Sertakan `defaultLocale`. Daftar ini menjadi menu bahasa dan kandidat tujuan terjemahan | Hanya `defaultLocale` |
| `ignoredDirectories` | Nama folder yang dikecualikan dari INDEX, pencarian, dan pemeriksaan. Jika ditentukan, nilai bawaan digantikan | `["99-archive"]` |
| `tree` | Nilai bawaan tampilan INDEX. Pengguna dapat menimpanya lewat pengaturan tampilan | Seperti pada contoh di atas |
| `editor.defaultMode` | Tampilan pengeditan selama pengguna belum menggantinya. `visual` atau `source` | `visual` |
| `editor.showEditButton` | Menentukan apakah [Edit] di kanan bawah isi dokumen ditampilkan | `true` |
| `documentStandards.pack` | Standard Pack yang dipakai untuk pemeriksaan dokumen dan templat. `builtin:<nama>`, atau jalur relatif dari root dokumentasi | Tidak ada |
| `documentStandards.profile` | Nama profil yang didefinisikan oleh Pack | Tidak ada |
| `translation.enabled` | Mengaktifkan pembuatan usulan terjemahan dan terjemahan sekaligus | `true` |
| `translation.contextFiles` | Markdown kanonik (jalur relatif dari root dokumentasi) yang diberikan sebagai rujukan istilah dan gaya bahasa saat menerjemahkan | `[]` |
| `translation.maxContextCharacters` | Batas atas jumlah karakter seluruh dokumen rujukan (maksimum 1048576) | `49152` |
| `description` | Penjelasan satu baris tentang kumpulan dokumen. Ditampilkan pada kartu di halaman utama repositori. Seperti `title`, dapat ditulis sebagai teks atau objek per bahasa | Tidak ada |

## Memberi tahu letak dokumen di dalam repositori

Pada `lunascape-docs.json` yang diletakkan tepat di bawah repositori, Anda dapat menulis **peta repositori**, bukan pengaturan folder tersebut. Jika salah satu dari tiga item berikut ditulis, berkas itu menjadi peta, dan folder itu sendiri tidak menjadi root dokumentasi.

| Item | Isi | Bawaan |
|---|---|---|
| `defaultFolder` | Folder tempat dokumen berada (jalur relatif dari folder teratas). Folder yang ditunjuk tidak memerlukan berkas pengaturan | Tidak ada (memakai `docs`) |
| `roots` | Daftar kumpulan dokumen bila jumlahnya lebih dari satu (jalur relatif dari folder teratas, sesuai urutan tampilan). Dalam hal ini, folder teratas menjadi halaman utama | Tidak ada |
| `excludes` | Folder yang dikecualikan dari penemuan root dokumentasi (jalur relatif dari folder teratas). Ditambahkan pada pengecualian bawaan seperti `node_modules` | `[]` |
| `home.cards` | Menentukan apakah kartu kumpulan dokumen ditampilkan di bawah README halaman utama. Setel `false` bila Anda menulis sendiri tautannya di README | `true` |

Root dokumentasi ditentukan dengan urutan berikut. Yang pertama ditemukan dari atas akan dipakai.

1. Folder yang ditentukan lewat pengaturan atau perintah
2. Sasaran yang ditunjuk `defaultFolder` atau `roots` pada `lunascape-docs.json` di folder teratas
3. Folder yang memiliki `lunascape-docs.json` (bila ada dua atau lebih di bawah induk yang sama, induk itu menjadi halaman utama)
4. Folder `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. Folder teratas repositori itu sendiri

> **Tip**
>
> Jika tidak ada yang ditulis, nomor 4 yang berlaku, sehingga repositori biasa dengan satu `docs/` tetap seperti sebelumnya. Tulis `defaultFolder` hanya bila Anda ingin nama foldernya `manual`.

### Contoh peta

```json
{
  "title": "Bantuan Lunascape",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Urutan prioritas pengaturan

Item yang berkaitan dengan tampilan diprioritaskan dengan urutan berikut.

1. Pengaturan tampilan pengguna (panel [Pengaturan tampilan])
2. Pengaturan VS Code (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Nilai bawaan produk

Hanya bahasa (`defaultLocale`, `fallbackLocale`, `locales`) yang merupakan pengecualian: `lunascape-docs.json` adalah acuan utamanya. Bahasa proyek tidak dapat ditimpa melalui pengaturan pribadi VS Code.

> **Catatan**
>
> Standard Pack juga dapat ditentukan sebagai `standard` di `docs-lint.config.json`. Bila keduanya ada, `docs-lint.config.json` yang diprioritaskan.

## Topik terkait

- [Mengubah aturan pemeriksaan](rules.md)
- [Mengubah pengaturan tampilan](../02-reading/display-settings.md)
- [Daftar pengaturan VS Code](../08-reference/settings.md)
