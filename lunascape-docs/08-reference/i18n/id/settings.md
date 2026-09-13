# Daftar pengaturan VS Code

Cari "Lunascape Docs" di pengaturan VS Code (`⌘,` / `Ctrl+,`) untuk mengubah item berikut. Semuanya adalah pengaturan per pengguna dan tidak disimpan ke dalam dokumen proyek.

## Root dokumentasi

| Pengaturan | Nilai | Bawaan | Fungsi |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` memilih secara otomatis root dokumentasi yang terdekat dengan berkas Markdown yang dibuka, dan membuka folder induknya untuk sementara bila berkas itu tidak termasuk root mana pun. `fixed` selalu membuka root dokumentasi pada `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Larik string | `["docs"]` | Nama folder yang ditemukan otomatis sebagai root dokumentasi pada mode `auto`. Folder yang memiliki `lunascape-docs.json` ditemukan tanpa memandang namanya. Bila `lunascape-docs.json` di bawah repositori memuat `defaultFolder` atau `roots`, yang itulah yang diutamakan |
| `lunascapeDocEditor.root` | Path | `docs` | Root dokumentasi relatif terhadap ruang kerja, untuk mode `fixed` atau saat dibuka melalui perintah |
| `lunascapeDocEditor.startPage` | Path | `README.md` | Halaman awal relatif terhadap root dokumentasi |
| `lunascapeDocEditor.title` | String | `Lunascape Docs` | Menimpa judul tab dokumen. Tidak memengaruhi nama pilihan root dokumentasi |
| `lunascapeDocEditor.ignoredDirectories` | Larik string | `["99-archive"]` | Nama folder yang dikecualikan dari INDEX |

## Tampilan

| Pengaturan | Nilai | Bawaan | Fungsi |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` memakai latar putih, `auto` mengikuti skema warna VS Code |
| `lunascapeDocEditor.locale` | Tag bahasa | Tidak ada | Bahasa dokumen pribadi Anda, yang diutamakan bila tersedia. Tidak mengubah bahasa kanonik proyek |
| `lunascapeDocEditor.documentMetadata.compact` | Boolean | `true` | Melipat tabel pengelolaan dokumen tepat setelah H1 menjadi baris "Informasi dokumen" |
| `lunascapeDocEditor.tree.showFileNames` | Boolean | `false` | Menampilkan nama berkas alih-alih nama dokumen di INDEX |
| `lunascapeDocEditor.tree.showDocumentIcons` | Boolean | `false` | Menampilkan ikon dokumen di INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | Boolean | `false` | Menampilkan ikon folder di INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | Boolean | `false` | Menampilkan jumlah item tepat di bawah setiap folder pada INDEX |
| `lunascapeDocEditor.tree.showGuides` | Boolean | `true` | Menampilkan garis panduan tingkatan di INDEX |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Jarak antarbaris INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Boolean | `true` | Menutup INDEX sekali saja bila dokumen hanya ada satu |

## Pengeditan

| Pengaturan | Nilai | Bawaan | Fungsi |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Tampilan pengeditan selama Anda belum menggantinya. Tampilan yang terakhir dipakai lebih diutamakan |
| `lunascapeDocEditor.editor.showEditButton` | Boolean | `true` | Menampilkan [Edit] di kanan bawah isi dokumen |

## Diagram

| Pengaturan | Nilai | Bawaan | Fungsi |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Runtime penggambaran TikZ. `bundled` memakai runtime tersertakan yang telah disetujui (tidak disertakan pada versi distribusi saat ini), `workspace` memakai `node-tikzjax` 1.0.5 tepat di bawah ruang kerja tepercaya (khusus pengembangan dan evaluasi), `disabled` tidak menggambar apa pun |

## Pengaturan yang tidak disarankan

| Pengaturan | Gunakan sebagai gantinya |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` pada `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` pada `lunascape-docs.json` |

Pengaturan pribadi tidak dapat menimpa bahasa proyek.

## Topik terkait

- [Mengubah pengaturan tampilan](../02-reading/display-settings.md)
- [Konfigurasi proyek](../04-document-tools/project-configuration.md)
