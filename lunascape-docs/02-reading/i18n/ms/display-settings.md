# Menukar tetapan paparan

Melalui [Tetapan paparan] (gear) pada bar alat, setiap pengguna boleh menukar rupa INDEX dan paparan butang edit.

1. Tekan [Tetapan paparan] pada bar alat.
2. Tukar item yang ingin diubah. Perubahan berkuat kuasa serta-merta.
3. Tekan [Tetapan paparan] sekali lagi, atau tekan di luar panel, untuk menutupnya.

## Item yang boleh ditetapkan

| Bahagian | Item | Fungsi |
|---|---|---|
| Bahasa dokumen | (keadaan semasa) | Memaparkan bahasa lalai projek dan bahasa yang sedang dipaparkan. [Tetapkan bahasa projek…] membuka tetapan bahasa projek |
| Kandungan | [Nama fail] | Memaparkan nama fail dan bukan nama dokumen |
| | [Ikon dokumen] | Memaparkan ikon pada item dokumen |
| | [Ikon folder] | Memaparkan ikon pada item folder |
| | [Bilangan item] | Memaparkan bilangan dokumen dalam folder |
| | [Panduan inden] | Memaparkan garis panduan yang menunjukkan hierarki |
| | [Sembunyikan jika hanya ada satu dokumen] | Dalam akar dokumentasi yang hanya mempunyai 1 dokumen, INDEX ditutup secara automatik pada kali pertama sahaja |
| | [Kuncupkan maklumat dokumen] | Menguncupkan jadual pengurusan di bahagian atas dokumen menjadi baris "Maklumat dokumen". Apabila dimatikan, jadual dipaparkan seadanya |
| | [Kepadatan paparan] | Memilih jarak baris INDEX daripada [Biasa] / [Padat] |
| | [Butang edit] | Memaparkan [Edit] di bahagian kanan bawah teks |
| Tindakan | [Kembali kepada lalai projek] | Memadamkan semua perubahan pengguna dan kembali kepada tetapan projek |
| | [Buka tetapan sambungan] | Membuka tetapan Lunascape Docs pada skrin tetapan VS Code |

> **Petua**
>
> - Tetapan paparan disimpan bagi setiap pengguna dan setiap akar dokumentasi, dan tidak ditulis ke dalam fail yang diurus oleh Git.
> - Tetapan diutamakan mengikut susunan "tetapan paparan pengguna → tetapan VS Code → `lunascape-docs.json` → lalai produk". Nilai lalai sepasukan ditentukan melalui `tree` dan `editor` dalam `lunascape-docs.json`.

## Menukar tema warna

Apabila anda menekan penukar tema (matahari/bulan) pada bar alat, paparan bertukar antara latar belakang putih dan tema warna VS Code. Tema ketika dibuka ditentukan oleh tetapan `lunascapeDocEditor.appearance` (`light` atau `auto`).

## Topik berkaitan

- [Menggunakan INDEX](index-panel.md)
- [Tetapan projek](../04-document-tools/project-configuration.md)
- [Senarai tetapan VS Code](../08-reference/settings.md)
