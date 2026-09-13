# Belge ve klasör oluşturma ve düzenleme

INDEX öğe menüsünden belge ve klasör oluşturabilir, çoğaltabilir, adlarını değiştirebilir ve silebilirsiniz. Giriş, görüntüleyici içindeki küçük bir iletişim kutusunda yapılır ve okumanızı kesintiye uğratmaz.

> **Not**
>
> Bu işlemler yalnızca çalışma alanı VS Code'da güvenilen çalışma alanı olarak işaretlendiğinde kullanılabilir. Bir belge düzenlenirken, başka bir işlem sürerken veya hedefte kaydedilmemiş değişiklikler varken çalıştırılamaz.

## Belge veya klasör oluşturma

1. Oluşturulacağı klasörün öğe menüsünü ([⋯] veya sağ tıklama) açın.
   Doğrudan belge kökünün altında oluşturmak için INDEX başlığının sağ ucundaki [⋯] düğmesini kullanın ya da INDEX'in boş bir bölümüne sağ tıklayın.
2. [Yeni belge] veya [Yeni klasör] seçeneğini seçin.
3. Bir ad girin ve [Oluştur] düğmesine basın.
   Belge adının bir Markdown uzantısı olması gerekir (`.md`, `.markdown`, `.mdx` gibi).

Yeni belgeler, varsayılan dildeki belge (asıl belge) olarak oluşturulur.

## Belge çoğaltma

1. Belgenin öğe menüsünü açın ve [Çoğalt] seçeneğini seçin.
2. Yeni bir ad girin ve [Oluştur] düğmesine basın.

Yalnızca asıl belge çoğaltılır; çevirileri çoğaltılmaz.

## Başlığı değiştirme

Belgenin başlığını (H1) değiştirir. Dosya adı değişmez.

1. Bir belgenin veya klasörün öğe menüsünü açın ve [Başlığı değiştir] seçeneğini seçin.
2. Yeni başlığı tek satır olarak girin ve [Değiştir] düğmesine basın.

Klasörlerde, o klasörün `README.md` dosyasının başlığı değiştirilir. Görüntülenen dil bir çeviriyse, o dildeki belgenin başlığı değişir.

## Belge adını değiştirme

Araç çubuğunda görünen belge adını (belge kökünün adını) değiştirir.

1. Araç çubuğundaki belge adına sağ tıklayın. INDEX başlığının sağ ucundaki [⋯] düğmesi de aynı menüyü açar.
2. [Belge adını değiştir] seçeneğini seçin ve yeni bir ad girin.

Ayarlanmadığı sürece klasör adı olduğu gibi gösterilir.

Belirlediğiniz ad, **belge adını o anda hangi yer sağlıyorsa oraya** yazılır; böylece gördüğünüz bir başlık hiçbir zaman yok sayılmaz.

| Geçerli durum | Yazılacağı yer |
|---|---|
| `lunascape-docs.json` bir ad içeriyor | `lunascape-docs.json` güncellenir |
| Ad yok, ancak belge kökünde bir README var | README'nin başlığı (H1) yeniden yazılır |
| Hiçbiri yok | `lunascape-docs.json` oluşturulur ve ad oraya kaydedilir |

Hangisine yazıldığı, değişiklikten sonra görünen iletide belirtilir.

> **İpucu**
>
> Belge adı şu sırayla belirlenir: `lunascape-docs.json` içindeki ad, ardından belge kökündeki README'nin başlığı, ardından klasör adı.

## Dosya veya klasör adını değiştirme

1. Öğe menüsünü açın ve [Dosya adını değiştir] veya [Klasör adını değiştir] seçeneğini seçin.
2. Yeni adı girin ve [Değiştir] düğmesine basın.

İlgili çeviriler (`i18n/<dil>/` altındaki aynı yol) de birlikte yeniden adlandırılır.

## Silme

1. Öğe menüsünü açın ve [Çöp kutusuna taşı] seçeneğini seçin.
2. Onay iletisinin içeriğini denetleyin ve taşımayı onaylayın.

Hedef, işletim sisteminin çöp kutusuna taşınır; gerekirse geri yüklenebilir. Çeviriler silinmez, oldukları yerde kalır.

## Kullanılamayan adlar

- `.` ile başlayan adlar (INDEX'te görünmezler)
- `i18n` (çeviri dosyaları için ayrılmıştır)
- Windows'ta ayrılmış adlar (`CON`, `PRN` gibi)
- Nokta veya boşlukla biten adlar
- Denetim karakterleri ya da dosya adlarında kullanılamayan karakterler içeren adlar
- Aynı klasörde zaten bulunan adlar (yalnızca büyük/küçük harfle ayrılan adlar dâhil)

> **Not**
>
> Başlangıç sayfasının (genellikle kökteki `README.md`) adı değiştirilemez veya taşınamaz. Önce `lunascape-docs.json` içindeki `startPage` değerini değiştirin.

## İlgili konular

- [Belge sıralamasını değiştirme](reorder.md)
- [INDEX kullanımı](../02-reading/index-panel.md)
