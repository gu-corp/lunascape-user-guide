# Menukar susunan dokumen

Susunan yang dipaparkan dalam INDEX boleh ditukar dengan seret dan lepas atau melalui papan kekunci. Susunan yang ditukar disimpan dalam front matter dokumen sebagai `navigation.order`.

## Menyusun semula dengan seret dan lepas

1. Seret dokumen atau folder dalam INDEX.
2. Lepaskannya di hadapan atau di belakang item pada aras yang sama, atau di atas sesebuah folder.
   Dalam aras yang sama, susunannya berubah. Jika dilepaskan pada folder lain, item itu berpindah ke folder tersebut.

## Menyusun semula dengan papan kekunci atau menu

- Letakkan fokus pada item INDEX, kemudian tekan `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Pilih [Alih ke atas satu] / [Alih ke bawah satu] dalam menu item.

## Kandungan yang disimpan

- Apabila item disusun semula dalam aras yang sama, `navigation.order` dalam front matter dokumen kanonik dikemas kini. Bagi folder, nilai itu ditulis ke dalam `README.md` folder berkenaan. Jika folder itu tiada `README.md`, satu `README.md` yang mengandungi front matter sahaja akan dicipta.
- Apabila item dipindahkan ke folder lain, dokumen kanonik dan versi terjemahannya dipindahkan bersama-sama. Sebelum pemindahan, pengesahan tentang kesannya terhadap pautan relatif akan dipaparkan.
- Staging dan komit Git tidak dilakukan.

> **Nota**
>
> - Penyusunan semula tidak boleh dilakukan semasa menapis, semasa menyunting dokumen, dan dalam ruang kerja yang tidak dipercayai.
> - Apabila "INDEX telah dikemas kini" dipaparkan, ini bermakna perubahan lain baru sahaja digunakan. Lakukan operasi itu sekali lagi.
> - Halaman mula tidak boleh dipindahkan ke folder lain.

> **Petua**
>
> Jika `navigation.order` diberikan dalam selang 100 seperti 100, 200, 300, dokumen lain mudah disisipkan di antaranya kemudian. Untuk maklumat lanjut, lihat [Menetapkan metadata navigasi](../04-document-tools/navigation-metadata.md).

## Topik berkaitan

- [Mencipta dan menyusun dokumen dan folder](organize.md)
- [Menetapkan metadata navigasi](../04-document-tools/navigation-metadata.md)
