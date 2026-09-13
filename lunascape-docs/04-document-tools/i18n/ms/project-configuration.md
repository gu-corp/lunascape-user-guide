# Tetapan projek

`lunascape-docs.json` yang terletak terus di bawah akar dokumentasi ialah tetapan akar dokumentasi yang dikongsi oleh pasukan. Fail ini diurus dengan Git.

## Membuat atau mengedit fail tetapan

- Tekan [Alat Dokumen] pada bar alat → tab [Semakan] → [Sumber peraturan dan tetapan dokumen] → [Edit tetapan dokumen], dan fail itu akan dibuka dalam VS Code. Jika fail belum ada, fail awal akan dibuat pada ketika itu.
- Nama fail `lunascape-docs.json` dikaitkan secara automatik dengan JSON Schema yang disertakan, jadi pelengkapan input dan keterangan bagi setiap item akan dipaparkan. Catatan `$schema` tidak diperlukan.

## Contoh tetapan

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

## Keterangan item

| Item | Kandungan | Lalai |
|---|---|---|
| `id` | Kunci untuk menyimpan tetapan paparan bagi setiap pengguna. Berikan ID yang tetap apabila anda mahu tetapan kekal walaupun folder dipindahkan | Laluan folder |
| `title` | Nama yang dipaparkan di hujung kiri bar alat dan dalam senarai akar dokumentasi. Nama ini tidak berubah walaupun bahasa paparan ditukar | Tajuk README/index akar, jika tiada, nama folder |
| `indexTitle` | Tajuk INDEX | `INDEX` |
| `startPage` | Dokumen yang dibuka pertama (laluan relatif dari akar dokumentasi) | `README.md` |
| `appearance` | Skema warna: `light` (sentiasa cerah) atau `auto` (mengikut tema VS Code) | `light` |
| `defaultLocale` | Bahasa lalai (bahasa dokumen kanonik). Dinyatakan dengan tag bahasa BCP 47 (`ja`, `en`, `zh-Hant` dan sebagainya). Ia menjadi sumber terjemahan | Tidak ditetapkan (dianggarkan daripada teks untuk paparan) |
| `fallbackLocale` | Bahasa yang mula-mula ditunjukkan kepada pembaca yang bahasa persekitarannya tidak sepadan dengan mana-mana bahasa yang disokong. Nyatakan bahasa yang terkandung dalam `locales` | Tidak ditetapkan (`defaultLocale` digunakan) |
| `locales` | Senarai bahasa yang disokong. Sertakan `defaultLocale`. Ia menjadi menu bahasa dan calon sasaran terjemahan | `defaultLocale` sahaja |
| `ignoredDirectories` | Nama folder yang dikecualikan daripada INDEX, carian dan semakan. Jika dinyatakan, ia menggantikan nilai lalai | `["99-archive"]` |
| `tree` | Nilai lalai bagi paparan INDEX. Pengguna boleh menggantikannya melalui tetapan paparan | Seperti contoh di atas |
| `editor.defaultMode` | Paparan penyuntingan semasa pengguna belum menukarnya: `visual` atau `source` | `visual` |
| `editor.showEditButton` | Sama ada [Edit] dipaparkan di bahagian kanan bawah dokumen | `true` |
| `documentStandards.pack` | Standard Pack yang digunakan untuk semakan dokumen dan templat: `builtin:<nama>`, atau laluan relatif dari akar dokumentasi | Tiada |
| `documentStandards.profile` | Nama profil yang ditakrifkan oleh Pack | Tiada |
| `translation.enabled` | Mengaktifkan pembuatan cadangan terjemahan dan terjemahan pukal | `true` |
| `translation.contextFiles` | Markdown kanonik (laluan relatif dari akar dokumentasi) yang diserahkan semasa terjemahan sebagai rujukan istilah dan gaya bahasa | `[]` |
| `translation.maxContextCharacters` | Had atas jumlah bilangan aksara dokumen rujukan (maksimum 1048576) | `49152` |
| `description` | Keterangan satu baris tentang set dokumen. Dipaparkan pada kad di halaman utama repositori. Sama seperti `title`, boleh ditulis sebagai rentetan atau objek mengikut bahasa | Tiada |

## Memberitahu di mana dokumen berada dalam repositori

`lunascape-docs.json` yang diletakkan terus di bawah repositori boleh memuatkan **peta repositori**, bukan tetapan folder itu sendiri. Jika salah satu daripada tiga item berikut ditulis, ia menjadi peta, dan folder itu sendiri tidak menjadi akar dokumentasi.

| Item | Kandungan | Lalai |
|---|---|---|
| `defaultFolder` | Folder yang memuatkan dokumen (laluan relatif dari folder ini). Folder yang ditunjuk tidak memerlukan fail tetapan | Tiada (`docs` digunakan) |
| `roots` | Senarai set dokumen apabila terdapat beberapa set (laluan relatif dari folder ini, mengikut susunan paparan). Dalam kes ini, folder ini menjadi halaman utama | Tiada |
| `excludes` | Folder yang dikecualikan daripada penemuan akar dokumentasi (laluan relatif dari folder ini). Ditambah kepada pengecualian lalai seperti `node_modules` | `[]` |
| `home.cards` | Sama ada kad set dokumen dipaparkan di bawah README halaman utama. Tetapkan kepada `false` jika anda menulis pautan sendiri dalam README | `true` |

Akar dokumentasi ditentukan mengikut susunan berikut. Yang pertama ditemui daripada atas akan digunakan.

1. Folder yang dinyatakan melalui tetapan atau arahan
2. Sasaran yang ditunjuk oleh `defaultFolder` atau `roots` dalam `lunascape-docs.json` di bahagian atas
3. Folder yang mempunyai `lunascape-docs.json` (jika ada dua atau lebih di bawah induk yang sama, induk itu menjadi halaman utama)
4. Folder `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. Bahagian atas repositori itu sendiri

> **Petua**
>
> Jika tiada apa-apa ditulis, langkah 4 akan berfungsi, jadi repositori biasa yang mempunyai satu `docs/` berkelakuan seperti sebelum ini. Tulis `defaultFolder` hanya apabila anda mahu nama folder itu `manual`.

### Contoh peta

```json
{
  "title": "Bantuan Lunascape",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Keutamaan tetapan

Item yang berkaitan dengan paparan diutamakan mengikut susunan berikut.

1. Tetapan paparan pengguna (panel [Tetapan paparan])
2. Tetapan VS Code (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Nilai lalai produk

Hanya bahasa (`defaultLocale`, `fallbackLocale`, `locales`) yang menjadi pengecualian: `lunascape-docs.json` ialah sumber rasmi. Tetapan peribadi VS Code tidak boleh menggantikan bahasa projek.

> **Nota**
>
> Standard Pack juga boleh dinyatakan sebagai `standard` dalam `docs-lint.config.json`. Jika kedua-duanya ada, `docs-lint.config.json` diutamakan.

## Topik berkaitan

- [Menukar peraturan semakan](rules.md)
- [Menukar tetapan paparan](../02-reading/display-settings.md)
- [Senarai tetapan VS Code](../08-reference/settings.md)
