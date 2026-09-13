# Belgeleri denetleme

docs-lint; başlık yapısını, kırık bağlantıları, eksik zorunlu belge ve bölümleri, terim tutarsızlıklarını ve gereksinim kimliklerinin tutarlılığını denetler. Denetim her zaman belge kökünün tamamını kapsar.

## Denetimi çalıştırma

1. Araç çubuğunda [Belge Araçları] düğmesine basın ve [Denetim] sekmesini açın.
2. [Belge kökünü denetle] düğmesine basın.
   Komut Paleti'nden "Lunascape Docs: Belge kökünü denetle" komutuyla da çalıştırabilirsiniz.
3. Bulgu listesini gözden geçirin.

## Sonuçları okuma

- Listenin üstündeki [Bu belge] / [Tümü] seçenekleriyle gösterilen kapsamı değiştirin. Denetimin kendi kapsamı her zaman belge kökünün tamamıdır.
- Bulguların dört düzeyi vardır: hata, uyarı, bilgi ve öneri. Araç çubuğundaki [Belge Araçları], hata ve uyarı sayısını gösterir.
- Bir bulguya bastığınızda, ilgili Markdown kaynağındaki konum VS Code düzenleyicisinde açılır.
- Belge kökünün tamamını ilgilendiren bulgular (örneğin eksik bir test belgesi) konum bilgisi olmadan "Belge kökünün tamamı" öğesi olarak görünür.
- Aynı bulgular VS Code'un Sorunlar panelinde de görünür.

## Denetlenen öğeler

[Kuralları gözden geçir ve değiştir] düğmesine bastığınızda etkin denetimlerin listesi ve her birinin amacı görüntülenir. Başlıca öğeler şunlardır:

| Öğe | İçerik |
|---|---|
| Başlık yapısı | Tek bir H1 var mı ve başlık düzeyleri arada atlanıyor mu |
| İç bağlantılar | Bağlantı hedefi belge var mı ve belge kökünün dışına çıkıyor mu |
| Kod bloğu dili | Kod bloklarında dil adı belirtilmiş mi |
| Gerekli klasörler ve belgeler | Standard Pack profilinin gerektirdiği klasör ve belgeler eksiksiz mi |
| Belgede gereken bölümler | Her belge türü için gereken bölümler var mı |
| Terim birliği | Kaçınılması gereken ifadeleri saptar ve tercih edilen terimlere yönlendirir |
| Gereksinim kimliği adlandırma ve yineleme | Gereksinim kimlikleri adlandırma kuralına uyuyor mu ve iki kez tanımlanmış mı |
| Gereksinim kimliği başvuru tutarlılığı | Tasarım, test ve durum tablolarının başvurduğu gereksinim kimlikleri gerçekten var mı |
| Gereksinim ve test eşleşmesi | Gereksinim kimliklerine test belgelerinden başvuruluyor mu |

Hangi öğelerin etkin olacağı, `lunascape-docs.json` içinde seçilen Standard Pack ile profile ve `docs-lint.config.json` dosyasına bağlıdır.

> **Not**
>
> - Bir belgeyi veya ayarı değiştirdiğinizde önceki sonuç "yeniden denetim gerekli" durumuna geçer. Hiçbir şey kendiliğinden geçmiş sayılmaz; [Belge kökünü denetle] düğmesine yeniden basın.
> - Kaydedilmemiş değişiklikler denetime yansımaz. Önce kaydedin.
> - Denetim, cihaz içinde belirlenimci biçimde çalışır. Yapay zekâ değerlendirmeleri ve çeviri sonuçları denetim sonuçlarına karışmaz.

## İlgili konular

- [Denetim kurallarını değiştirme](rules.md)
- [Proje yapılandırması](project-configuration.md)
- [Denetim, oluşturma veya çeviri başarısız oluyor](../07-troubleshooting/tools.md)
