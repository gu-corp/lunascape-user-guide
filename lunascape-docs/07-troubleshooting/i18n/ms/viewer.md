# Dokumen tidak dipaparkan

## "開けるMarkdownまたはdocsフォルダが見つかりません" (Tiada Markdown atau folder docs yang boleh dibuka) dipaparkan

- Ruang kerja tidak mempunyai folder `docs`, atau menggunakan nama selain `docs`.
  - Letakkan `lunascape-docs.json` di dalam folder itu, maka folder tersebut dikenali sebagai akar dokumentasi tanpa mengira namanya.
  - Atau, tambahkan nama folder itu pada tetapan `lunascapeDocEditor.rootDirectoryNames`.
- Jika belum ada dokumen, ciptanya dengan "Lunascape Docs: テンプレートからドキュメントを作成" (Cipta dokumentasi daripada templat).
- Anda juga boleh membuka fail Markdown dalam editor, kemudian menjalankan "Lunascape Docs: 仕様書ビューアーで開く" (Buka dalam Pemapar Spesifikasi).

## Dokumen tidak dipaparkan dalam INDEX

- Pastikan sambungan failnya ialah `.md`, `.markdown` atau `.mdx`.
- Folder berikut tidak dipaparkan: folder yang bermula dengan `.`, `node_modules`, dan folder yang disenaraikan dalam `ignoredDirectories` (lalainya `99-archive`).
- Versi terjemahan di bawah `i18n/` tidak disenaraikan secara berasingan dalam INDEX. Tukar kepadanya melalui menu bahasa.
- Jika fail yang baru ditambah tidak dipaparkan, tekan [Muat semula].
- Anda mungkin sedang melihat akar dokumentasi yang lain. Semak nama akar dokumentasi di hujung kiri bar alat.

## Menekan folder tidak memaparkan apa-apa

`README.md` folder itu ialah "penghurai khusus tetapan" yang hanya mempunyai front matter tanpa isi. Buka folder itu dalam INDEX dan pilih dokumen di dalamnya.

## Akar dokumentasi yang tidak dikehendaki dibuka

- Jika tetapan `lunascapeDocEditor.rootMode` ialah `fixed`, `lunascapeDocEditor.root` sentiasa dibuka.
- Dengan `auto`, akar dokumentasi yang paling hampir dengan fail Markdown yang dibuka akan dipilih. Tukar melalui menu lungsur di hujung kiri bar alat.

## Nama akar dokumentasi berbeza daripada yang dijangka

Nama ditentukan mengikut turutan: `title` dalam `lunascape-docs.json` → `navigation.title` dalam `README.md` akar → H1 fail itu → `index.md` → nama folder. Tetapkan `title` jika anda mahu menetapkannya.

## INDEX hilang

- Dalam akar dokumentasi yang hanya mempunyai satu dokumen, INDEX ditutup secara automatik pada kali pertama sahaja. Bukanya semula dengan ikon paparan lajur pada bar alat. Anda boleh mematikannya dengan [Sembunyikan jika hanya ada satu dokumen] dalam [Tetapan paparan].
- Apabila skrin sempit, bukanya melalui [Buka INDEX] (tiga garis) di sebelah kiri [Kembali].

## Pautan tidak terbuka apabila ditekan

- "リンク先が見つかりません" (Sasaran pautan tidak dijumpai): fail sasaran tidak wujud. Anda boleh menyemak pautan dalaman dengan [Semakan] dalam Alat Dokumen.
- "安全でない、または未対応のリンクを開きませんでした" (Pautan yang tidak selamat atau tidak disokong tidak dibuka): pautan ke luar akar dokumentasi, atau ke skema selain `https://` dan `mailto:`, tidak akan dibuka.

## Bahasa yang dipaparkan berbeza daripada yang dikehendaki

- Semak bahasa halaman yang sedang dipaparkan dan asas penentuannya dalam menu bahasa.
- Bahasa paparan yang dipilih sebelum ini diingati. Pilih semula bahasa lalai dalam menu bahasa.
- Jika tetapan peribadi `lunascapeDocEditor.locale` ditetapkan, versi terjemahan bahasa tersebut diutamakan.

## Perkara berkaitan

- [Menukar akar dokumentasi](../02-reading/roots.md)
- [Akar dokumentasi dan konvensi fail](../04-document-tools/structure.md)
