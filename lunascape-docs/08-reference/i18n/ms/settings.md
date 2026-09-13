# Tetapan VS Code

Cari "Lunascape Docs" dalam tetapan VS Code (`⌘,` / `Ctrl+,`) untuk menukar perkara berikut. Kesemuanya ialah tetapan bagi setiap pengguna dan tidak pernah disimpan ke dalam dokumen projek.

## Akar dokumentasi

| Tetapan | Nilai | Lalai | Fungsi |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` memilih secara automatik akar dokumentasi yang paling hampir dengan fail Markdown yang dibuka, dan membuka folder induknya buat sementara jika fail itu tidak tergolong dalam mana-mana akar. `fixed` sentiasa membuka akar dokumentasi dalam `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Tatasusunan rentetan | `["docs"]` | Nama folder yang ditemui secara automatik sebagai akar dokumentasi dalam mod `auto`. Folder yang mempunyai `lunascape-docs.json` ditemui tanpa mengira namanya. Apabila terdapat `defaultFolder` atau `roots` dalam `lunascape-docs.json` di bawah repositori, tetapan itu diutamakan |
| `lunascapeDocEditor.root` | Laluan | `docs` | Akar dokumentasi relatif kepada ruang kerja, bagi mod `fixed` atau ketika dibuka melalui perintah |
| `lunascapeDocEditor.startPage` | Laluan | `README.md` | Halaman permulaan relatif kepada akar dokumentasi |
| `lunascapeDocEditor.title` | Rentetan | `Lunascape Docs` | Menulis ganti tajuk tab dokumen. Ia tidak mempengaruhi nama pemilihan akar dokumentasi |
| `lunascapeDocEditor.ignoredDirectories` | Tatasusunan rentetan | `["99-archive"]` | Nama folder yang dikecualikan daripada INDEX |

## Paparan

| Tetapan | Nilai | Lalai | Fungsi |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` menggunakan latar belakang putih; `auto` mengikut skema warna VS Code |
| `lunascapeDocEditor.locale` | Tag bahasa | Tiada | Bahasa dokumen peribadi anda yang diutamakan apabila tersedia. Ia tidak menukar bahasa kanonik projek |
| `lunascapeDocEditor.documentMetadata.compact` | Boolean | `true` | Melipat jadual pengurusan dokumen selepas H1 menjadi baris "Maklumat dokumen" |
| `lunascapeDocEditor.tree.showFileNames` | Boolean | `false` | Memaparkan nama fail dan bukan nama dokumen dalam INDEX |
| `lunascapeDocEditor.tree.showDocumentIcons` | Boolean | `false` | Memaparkan ikon dokumen dalam INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | Boolean | `false` | Memaparkan ikon folder dalam INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | Boolean | `false` | Memaparkan bilangan item di bawah setiap folder dalam INDEX |
| `lunascapeDocEditor.tree.showGuides` | Boolean | `true` | Memaparkan garis panduan hierarki dalam INDEX |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Jarak baris INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Boolean | `true` | Menutup INDEX sekali sahaja apabila hanya ada satu dokumen |

## Penyuntingan

| Tetapan | Nilai | Lalai | Fungsi |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Paparan penyuntingan sebelum anda menukarnya. Paparan yang terakhir digunakan diutamakan |
| `lunascapeDocEditor.editor.showEditButton` | Boolean | `true` | Memaparkan [Edit] di bahagian kanan bawah teks dokumen |

## Rajah

| Tetapan | Nilai | Lalai | Fungsi |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Masa jalan pelukisan TikZ. `bundled` menggunakan masa jalan diluluskan yang disertakan (tidak disertakan dalam binaan edaran semasa), `workspace` menggunakan `node-tikzjax` 1.0.5 di bawah ruang kerja dipercayai (untuk pembangunan dan penilaian sahaja), `disabled` tidak melukis apa-apa |

## Tetapan yang tidak disarankan

| Tetapan | Gunakan sebagai ganti |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` dalam `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` dalam `lunascape-docs.json` |

Tetapan peribadi tidak boleh menulis ganti bahasa projek.

## Topik berkaitan

- [Menukar tetapan paparan](../02-reading/display-settings.md)
- [Konfigurasi projek](../04-document-tools/project-configuration.md)
