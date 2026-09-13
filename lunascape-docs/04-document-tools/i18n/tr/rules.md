# Denetim kurallarını değiştirme

Her denetim öğesinin bildirim düzeyini (hata, uyarı, bilgi) değiştirebilir veya öğeyi kullanılmaz duruma getirebilirsiniz. Değişiklikler belge kökündeki `docs-lint.config.json` dosyasına kaydedilir ve ekiple paylaşılır.

## Bildirim düzeyini değiştirme

1. Araç çubuğundaki [Belge Araçları] düğmesine basın ve [Denetim] sekmesini açın.
2. [Kuralları gözden geçir ve değiştir] düğmesine basın.
   Denetim öğelerinin listesi aynı kartın içinde açılır. Her öğede amacı ve geçerli ayarın kaynağı (Project, Profile, Pack, Default) gösterilir.
3. Değiştirmek istediğiniz öğenin bildirim düzeyini seçin.
4. [Kaydet ve yeniden denetle] düğmesine basın.
   Ayar kaydedilir ve belge kökünün tamamı yeni ayarla yeniden denetlenir.

| Seçenek | Anlamı |
|---|---|
| [Standart ayar (…)] | Geçersiz kılmayı kaldırır; profil, Standard Pack ve varsayılan değer sırasıyla belirlenen standart ayara döner |
| [Kullanılmıyor] | Bu öğe denetlenmez |
| [Bilgi] / [Uyarı] / [Hata] | Bu bildirim düzeyiyle raporlanır |

> **Not**
>
> - Kaydetmek için güvenilen çalışma alanı gerekir.
> - Yalnızca her öğenin bildirim düzeyi kaydedilir. Öğelere ait seçenekler olduğu gibi korunur. Standard Pack ve profilin kendisi bu ekranda değiştirilmez.
> - Kaydetmeden hemen önce `docs-lint.config.json` dışarıdan değiştirilmişse kaydetme işlemi iptal edilir. En son durumu yükleyip yeniden deneyin.
> - `docs-lint.config.json` yoksa, kaydettiğinizde oluşturulur.

## Ayar dosyasını doğrudan düzenleme

- [Ayrıntılı ayarları aç] düğmesine bastığınızda `docs-lint.config.json` VS Code'da açılır.
- [Kuralların kaynağı ve belge ayarları] bölümünü açıp [Belge ayarlarını düzenle] düğmesine bastığınızda `lunascape-docs.json` VS Code'da açılır. Standard Pack ve profil buradan seçilir.

Her iki dosyada da, uzantıyla birlikte gelen JSON Schema sayesinde giriş tamamlama ve açıklamalar kullanılabilir.

## Standard Pack ve profiller

Standard Pack; gerekli belge türlerini, bölüm yapısını, terimleri ve şablonları bir araya getiren bir belge standardıdır. `lunascape-docs.json` dosyasındaki `documentStandards` ile seçilir.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Birlikte gelen `builtin:gu-corp-software` paketinde `base`, `web-application`, `api-service`, `regulated-financial-product` ve `smart-contract` profilleri bulunur.

## İlgili konular

- [Belgeleri denetleme](check.md)
- [Proje ayarları](project-configuration.md)
