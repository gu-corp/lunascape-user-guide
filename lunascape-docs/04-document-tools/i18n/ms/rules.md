# Menukar peraturan semakan

Anda boleh menukar tahap pemberitahuan (ralat, amaran, maklumat) bagi setiap item semakan, atau tidak menggunakannya. Perubahan disimpan dalam `docs-lint.config.json` di akar dokumentasi dan dikongsi dengan pasukan.

## Menukar tahap pemberitahuan

1. Tekan [Alat Dokumen] pada bar alat, kemudian buka tab [Semakan].
2. Tekan [Semak dan ubah peraturan].
   Senarai item semakan dikembangkan di dalam kad yang sama. Setiap item memaparkan tujuannya dan sumber tetapan semasa (Project, Profile, Pack, Default).
3. Pilih tahap pemberitahuan bagi item yang hendak diubah.
4. Tekan [Simpan dan semak semula].
   Tetapan disimpan dan keseluruhan akar dokumentasi disemak semula dengan tetapan baharu.

| Pilihan | Maksud |
|---|---|
| [Tetapan standard (…)] | Membuang tulis ganti dan kembali kepada tetapan standard yang ditentukan mengikut urutan profil, Standard Pack, kemudian nilai lalai |
| [Tidak digunakan] | Tidak menyemak item ini |
| [Maklumat] / [Amaran] / [Ralat] | Melaporkan pada tahap pemberitahuan ini |

> **Perhatian**
>
> - Penyimpanan memerlukan ruang kerja dipercayai.
> - Yang disimpan hanyalah tahap pemberitahuan bagi setiap item. Pilihan bagi setiap item dikekalkan seperti sedia ada. Standard Pack dan profil itu sendiri tidak diubah pada skrin ini.
> - Jika `docs-lint.config.json` diubah dari luar sejurus sebelum penyimpanan, penyimpanan dibatalkan. Muatkan keadaan terkini, kemudian cuba semula.
> - Jika `docs-lint.config.json` tiada, fail itu dicipta semasa anda menyimpan.

## Mengedit fail tetapan secara terus

- Tekan [Buka tetapan terperinci] untuk membuka `docs-lint.config.json` dalam VS Code.
- Buka [Sumber peraturan dan tetapan dokumen], kemudian tekan [Edit tetapan dokumen] untuk membuka `lunascape-docs.json` dalam VS Code. Standard Pack dan profil dipilih di sini.

Kedua-dua fail menyediakan pelengkapan input dan penerangan melalui JSON Schema yang disertakan bersama sambungan ini.

## Standard Pack dan profil

Standard Pack ialah piawaian dokumentasi yang menghimpunkan jenis dokumen yang diperlukan, susunan bab, istilah dan templat. Ia dipilih dengan `documentStandards` dalam `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Pack yang disertakan, `builtin:gu-corp-software`, mempunyai profil `base`, `web-application`, `api-service`, `regulated-financial-product` dan `smart-contract`.

## Topik berkaitan

- [Menyemak dokumen](check.md)
- [Tetapan projek](project-configuration.md)
