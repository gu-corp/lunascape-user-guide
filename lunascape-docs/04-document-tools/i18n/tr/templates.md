# Şablondan belge oluşturma

Belge Araçları'nın [Oluştur] sekmesinde bir şablon seçip içeriği önizleyerek yeni bir belge oluşturabilirsiniz.

1. Araç çubuğunda [Belge Araçları] düğmesine basın ve [Oluştur] sekmesini açın.
2. [Şablondan oluştur] düğmesine basın ve bir şablon seçin.
3. Giriş alanlarını (başlık, özet vb.) doldurun. Zorunlu alanlarda "Zorunlu" yazar.
4. Kayıt yerini, belge köküne göre göreli yol olarak girin (örneğin `03-design/api.md`).
5. [Önizleme] düğmesine basın ve oluşturulacak Markdown içeriğini gözden geçirin.
6. [Bu içerikle oluştur] düğmesine basın.
   Belge oluşturulur ve görüntüleyicide açılır. Ardından belge kökünün tamamı yeniden denetlenir.

## Seçilebilecek şablonlar

| Şablon | İçerik |
|---|---|
| Tek sayfalık belge | Kısa bir şartnameyi, notları veya tek başına bir açıklama belgesini tek dosyada oluşturur |
| Şartname · kılavuz · yardım | Şartname, kılavuz ve yardım için kullanılabilecek genel bir bölüm düzeniyle tek dosya oluşturur |
| Standard Pack şablonları | `lunascape-docs.json` içinde Standard Pack seçiliyse, o profilde kullanılabilen belge türleri (gereksinim belgesi, tasarım belgesi vb.) eklenir |

> **Not**
>
> - Oluşturma için güvenilen çalışma alanı gerekir.
> - Var olan dosyaların üzerine yazılmaz. Kayıt yerinde aynı adlı bir belge varsa oluşturma yapılamaz.
> - Kayıt yerinin `.md` veya `.mdx` uzantısı olmalıdır. `i18n` altında (çevirilerin bulunduğu yerde) belge oluşturulamaz.
> - Girişleri değiştirdikten sonra, oluşturmadan önce yeniden [Önizleme] düğmesine basın.

> **İpucu**
>
> Henüz belge klasörü olmayan projelerde, komut paletindeki "Lunascape Docs: Şablondan belge oluştur" komutuyla ilk takımı oluşturabilirsiniz. [İlk belgelerinizi oluşturma](../01-introduction/first-documents.md) konusuna bakın.

## İlgili konular

- [Belge Araçları'nı kullanma](README.md)
- [Denetim kurallarını değiştirme](rules.md)
