# Mengubah aturan pemeriksaan

Anda dapat mengubah tingkat pemberitahuan (kesalahan, peringatan, informasi) setiap butir pemeriksaan, atau menonaktifkannya. Perubahan disimpan ke `docs-lint.config.json` di root dokumentasi dan dibagikan dengan tim.

## Mengubah tingkat pemberitahuan

1. Tekan [Alat Dokumen] pada bilah alat, lalu buka tab [Pemeriksaan].
2. Tekan [Tinjau dan ubah aturan].
   Daftar butir pemeriksaan terbuka di dalam kartu yang sama. Setiap butir menampilkan tujuannya dan asal pengaturannya saat ini (Project, Profile, Pack, atau Default).
3. Pilih tingkat pemberitahuan untuk butir yang ingin Anda ubah.
4. Tekan [Simpan dan periksa ulang].
   Pengaturan disimpan dan seluruh root dokumentasi diperiksa ulang dengan pengaturan yang baru.

| Pilihan | Arti |
|---|---|
| [Pengaturan standar (…)] | Menghapus penimpaan dan mengembalikan ke pengaturan standar yang ditentukan berdasarkan profil, Standard Pack, lalu nilai bawaan |
| [Nonaktif] | Tidak memeriksa butir ini |
| [Informasi] / [Peringatan] / [Kesalahan] | Melaporkan pada tingkat pemberitahuan ini |

> **Catatan**
>
> - Penyimpanan memerlukan ruang kerja tepercaya.
> - Yang disimpan hanyalah tingkat pemberitahuan setiap butir. Opsi masing-masing butir tetap dipertahankan. Standard Pack dan profil itu sendiri tidak diubah dari layar ini.
> - Jika `docs-lint.config.json` diubah dari luar tepat sebelum penyimpanan, penyimpanan dibatalkan. Muat keadaan terbaru, lalu ulangi.
> - Jika `docs-lint.config.json` belum ada, berkas itu dibuat saat Anda menyimpan.

## Mengedit berkas pengaturan secara langsung

- Menekan [Buka pengaturan lengkap] akan membuka `docs-lint.config.json` di VS Code.
- Buka [Asal aturan dan pengaturan dokumen], lalu tekan [Edit pengaturan dokumen] untuk membuka `lunascape-docs.json` di VS Code. Standard Pack dan profil dipilih di sana.

Kedua berkas tersebut mendapat pelengkapan masukan dan penjelasan dari JSON Schema yang disertakan dalam ekstensi.

## Standard Pack dan profil

Standard Pack adalah standar dokumentasi yang merangkum jenis dokumen yang diperlukan, susunan bab, peristilahan, dan templat. Pilih dengan `documentStandards` di `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Pack bawaan `builtin:gu-corp-software` menyediakan profil `base`, `web-application`, `api-service`, `regulated-financial-product`, dan `smart-contract`.

## Topik terkait

- [Memeriksa dokumen](check.md)
- [Pengaturan proyek](project-configuration.md)
