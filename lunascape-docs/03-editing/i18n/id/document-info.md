# Menampilkan informasi dokumen

"Tabel kendali dokumen" yang diletakkan di awal dokumen (tabel berisi ID dokumen, versi, tanggal pembaruan, status, dan sebagainya) ditampilkan saat membaca sebagai satu baris ringkas "Informasi dokumen". Markdown-nya sendiri tetap berupa tabel biasa, sehingga tetap terbaca di GitHub.

## Syarat agar ditampilkan

Letakkan tabel dua kolom seperti berikut tepat setelah judul (H1).

```markdown
# Dokumen definisi kebutuhan fungsional

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Syaratnya adalah adanya baris "文書ID" dan beberapa butir kendali dokumen.
- Tabel yang diletakkan di bawah judul `## 文書管理` atau `## Document information` juga termasuk.
- Tabel yang berada di tengah isi teks, serta tabel "butir/isi" pada umumnya, tidak diubah.

## Cara penampilannya

- Saat membaca, hanya "status" dan "tanggal pembaruan" yang ditampilkan dalam huruf kecil.
- Tekan barisnya untuk menampilkan seluruh butir.
- Saat dicetak, seluruh butir ditampilkan.
- Pada layar penyuntingan, tabel tampil sebagai tabel biasa dan dapat langsung disunting.

> **Petunjuk**
>
> Jika Anda ingin tabel selalu ditampilkan tanpa diciutkan, nonaktifkan [Ciutkan detail dokumen] pada [Pengaturan tampilan].

## Topik terkait

- [Menyunting dokumen](README.md)
- [Mengubah pengaturan tampilan](../02-reading/display-settings.md)
