# Membaca dalam bahasa lain

Apabila sesuatu dokumen mempunyai terjemahan, anda boleh menukar bahasa daripada menu bahasa (glob) pada bar alat.

## Menukar bahasa

1. Tekan menu bahasa pada bar alat.
   Menu memaparkan bahasa halaman semasa dan asasnya (laluan terjemahan, pengesanan automatik, atau bahasa lalai projek).
2. Pilih bahasa yang anda mahu baca.
   Terjemahan dokumen yang sama akan dibuka. Pilihan itu diingat, dan dokumen yang anda buka seterusnya dipaparkan dalam bahasa tersebut jika terjemahannya wujud.

Senarai bahasa menunjukkan sama ada dokumen itu mempunyai terjemahan atau tidak.

| Paparan | Maksud |
|---|---|
| Ada terjemahan | Terjemahan wujud dan boleh dibuka |
| Tiada terjemahan | Bahasa ini disokong oleh projek, tetapi dokumen ini belum mempunyai terjemahan |
| Perlu dikemas kini | Terjemahan wujud, tetapi dokumen asal telah berubah selepas diterjemahkan |

> **Perhatian**
>
> - Memilih bahasa hanya membuka terjemahan yang sedia ada. Ia tidak menjana terjemahan dan tidak mencipta fail. Untuk membuat terjemahan, gunakan [Cipta atau urus terjemahan…] dalam menu yang sama.
> - Apabila bahasa halaman semasa didapati berbeza daripada bahasa lalai projek, satu amaran dipaparkan. Tetapan tidak akan ditulis semula.

## Bahasa yang dipaparkan pada mulanya

Apabila anda membuka dokumen, bahasa paparan pertama ditentukan mengikut susunan berikut.

1. Bahasa yang anda pilih sendiri sebelum ini dalam akar dokumentasi ini. Pilihan itu disimpan (memilih bahasa lalai juga disimpan sebagai satu pilihan).
2. Bahasa paparan VS Code (dalam versi pelayar Web, tetapan bahasa pelayar). Bahasa sokongan yang sepadan dipilih secara automatik. Bahasa berserta wilayah (seperti `en-US`) turut sepadan dengan bahasa asasnya (`en`).
3. Bahasa sandaran projek (`fallbackLocale` dalam `lunascape-docs.json`).
4. Bahasa lalai projek.

> **Petua**
>
> - Apabila bahasa dipilih secara automatik, bahasa semasa dalam menu bahasa dipaparkan dengan tanda "Dipilih automatik". Letakkan penuding pada lencana itu untuk melihat sebabnya.
> - `fallbackLocale` ialah bahasa yang ditunjukkan kepada pembaca yang bahasa persekitarannya tidak sepadan dengan mana-mana bahasa sokongan. Dalam projek yang kanoniknya bahasa Jepun dan mempunyai versi bahasa Inggeris, menetapkan `"en"` akan membuka versi bahasa Inggeris kepada pembaca dalam persekitaran bahasa Sepanyol, contohnya. Jika tidak ditetapkan, bahasa lalai digunakan.

## Tempat terjemahan disimpan

Dokumen dalam bahasa lalai kekal di tempatnya, manakala terjemahan diletakkan dalam **`i18n/<bahasa>/` di dalam folder yang sama**, dengan nama fail yang sama.

```text
docs/
  README.md                  ← bahasa lalai (contoh: bahasa Jepun)
  i18n/en/README.md          ← versi bahasa Inggerisnya
  guide/
    setup.md
    i18n/en/setup.md         ← versi bahasa Inggerisnya
```

> **Perhatian**
>
> - Membina semula struktur folder di bawah `i18n/` (`i18n/en/guide/setup.md`) tidak dikenali. Folder `i18n/` mesti sentiasa berada dalam folder yang sama dengan dokumen tersebut.
> - Satu tempat itu sahaja yang digunakan untuk mencari terjemahan. Meletakkan terjemahan dokumen yang sama dalam `i18n/` folder induk tidak menimbulkan persaingan "mana satu diutamakan": salinan di sebelah induk itu hanya menjadi fail terpencil yang tidak muncul dalam menu bahasa mahupun dalam lejar (dan tidak dipadamkan secara automatik). Jangan letakkan terjemahan yang sama di dua tempat.

## Jika membaca dalam versi pelayar Web

Dalam versi pelayar Web, bahasa boleh ditukar dengan cara yang sama apabila terjemahan wujud. Jika anda mahu membaca dalam bahasa yang tiada terjemahan, anda boleh menggunakan fungsi terjemahan halaman pelayar. Kod, rumus matematik dan rajah dikecualikan daripada terjemahan tersebut.

## Topik berkaitan

- [Menyerahkan kerja kepada AI](../05-ai/README.md)
- [Kerja yang boleh diserahkan](../05-ai/tasks.md)
- [Menukar tetapan paparan](../02-reading/display-settings.md)
