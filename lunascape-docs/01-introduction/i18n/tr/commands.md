# Komut listesi

Komut Paleti'ne (`⇧⌘P` / `Ctrl+Shift+P`) "Lunascape Docs" yazdığınızda aşağıdaki komutları çalıştırabilirsiniz.

| Komut | İşlevi |
|---|---|
| Lunascape Docs: Şartname görüntüleyicisini aç | En yakın belge kökünü görüntüleyicide açar. Okuma, düzenleme, denetim ve çeviri bu ekranda yapılır |
| Lunascape Docs: Şartname görüntüleyicisinde aç | Düzenleyicide açık olan Markdown dosyasını görüntüleyicide gösterir |
| Lunascape Docs: Şablondan belge oluştur | Belge klasörü bulunmayan bir projede ilk belge takımını oluşturur |
| Lunascape Docs: Belge kökünü doğrula | Belge kökünün tamamını docs-lint ile denetler, sonuçları Belge Araçları'nda ve "Sorunlar" panelinde gösterir |
| Lunascape Docs: Yardımı aç | Bu yardım kılavuzunu açar |

## Gezgin üzerinden işlemler

Gezgin'de bir `.md`, `.markdown` veya `.mdx` dosyasına sağ tıkladığınızda [Lunascape Docs: Şartname görüntüleyicisinde aç] seçeneğini seçebilirsiniz.

> **İpucu**
>
> Markdown dosyalarını normal şekilde açtığınızda da Lunascape Docs ile göstermek için çalışma alanı ayarlarına bir düzenleyici ilişkilendirmesi ekleyin.
>
> ```json
> {
>   "workbench.editorAssociations": {
>     "*.md": "lunascapeDocEditor.markdownPortal"
>   }
> }
> ```

## Adım adım kılavuz

VS Code'daki [Yardım] menüsü → "Hoş Geldiniz" bölümünde bulunan "Lunascape Docs'u kullanmaya başlayın" adlı adım adım kılavuzla ilk işlemleri sırayla deneyebilirsiniz.

## İlgili konular

- [Temel işlemler](../02-reading/README.md)
- [Klavye işlemleri listesi](../08-reference/keyboard.md)
