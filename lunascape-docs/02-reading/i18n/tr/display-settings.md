# Görünüm ayarlarını değiştirme

Araç çubuğundaki [Görünüm ayarları] (dişli) ile INDEX'in görünümünü ve düzenleme düğmesinin gösterilip gösterilmeyeceğini her kullanıcı kendine göre değiştirebilir.

1. Araç çubuğundaki [Görünüm ayarları] düğmesine basın.
2. Değiştirmek istediğiniz öğeleri açıp kapatın. Değişiklikler hemen uygulanır.
3. Kapatmak için [Görünüm ayarları] düğmesine yeniden basın veya panelin dışına tıklayın.

## Ayarlanabilen öğeler

| Bölüm | Öğe | İşlevi |
|---|---|---|
| Belge dili | (geçerli durum) | Projenin varsayılan dilini ve görüntülenmekte olan dili gösterir. [Proje dillerini ayarla…] ile projenin dil ayarlarını açar |
| İçerik | [Dosya adları] | Belge adı yerine dosya adını gösterir |
| | [Belge simgeleri] | Belge öğelerinde simge gösterir |
| | [Klasör simgeleri] | Klasör öğelerinde simge gösterir |
| | [Klasördeki öğe sayısı] | Klasörün içerdiği belge sayısını gösterir |
| | [Girinti kılavuzları] | Hiyerarşiyi gösteren kılavuz çizgilerini gösterir |
| | [Tek belge varsa otomatik olarak gizle] | Yalnızca bir belge bulunan belge kökünde INDEX'i yalnızca ilk açılışta otomatik olarak kapatır |
| | [Belge bilgilerini daralt] | Belgenin başındaki yönetim tablosunu "Belge bilgileri" satırına daraltır. Kapalıyken tablo olduğu gibi gösterilir |
| | [Görünüm yoğunluğu] | INDEX'in satır aralığını [Normal] / [Kompakt] arasından seçer |
| | [Düzenleme düğmesi] | Metnin sağ alt köşesindeki [Düzenle] düğmesini gösterir |
| İşlemler | [Proje varsayılanlarına dön] | Kullanıcının yaptığı tüm değişiklikleri siler ve projenin ayarlarına döner |
| | [Uzantı ayarlarını aç] | VS Code ayarlar ekranında Lunascape Docs ayarlarını açar |

> **İpucu**
>
> - Görünüm ayarları kullanıcı ve belge kökü başına saklanır; Git ile yönetilen dosyalara yazılmaz.
> - Ayarlar "kullanıcının görünüm ayarları → VS Code ayarları → `lunascape-docs.json` → ürün varsayılanları" sırasıyla önceliklendirilir. Ekip genelindeki varsayılan değerler `lunascape-docs.json` içindeki `tree` ve `editor` ile belirlenir.

## Renk düzenini değiştirme

Araç çubuğundaki tema değiştirme düğmesine (güneş/ay) bastığınızda beyaz arka plan ile VS Code renk düzeni arasında geçiş yapılır. Açılıştaki renk düzeni `lunascapeDocEditor.appearance` ayarıyla (`light` veya `auto`) belirlenir.

## İlgili konular

- [INDEX'i kullanma](index-panel.md)
- [Proje ayarları](../04-document-tools/project-configuration.md)
- [VS Code ayarları listesi](../08-reference/settings.md)
