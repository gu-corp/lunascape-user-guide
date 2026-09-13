# Görselleri boyutlandırma

Belgeye eklediğiniz görseller, metnin genişliğine ve ekranın yüksekliğine otomatik olarak sığar. Belirli bir boyutta göstermek istediğiniz görseller için genişlik belirleyebilirsiniz.

## Otomatik boyutlandırma nasıl çalışır

- Sıradan bir Markdown görseli (`![açıklama](./images/screen.png)`), metin genişliğine sığacak şekilde küçültülür. Özgün boyutundan daha büyük olacak şekilde asla büyütülmez.
- Uzun bir ekran görüntüsü, ekran yüksekliğinin %72'si veya 720px'den hangisi küçükse ona sığdırılır.

## Genişliği düzenleyicide belirleme

1. [Düzenle] düğmesine basın ve görseli görsel görünümde seçin.
2. Araç çubuğundaki [Görsel boyutu] menüsünden bir genişlik seçin.
3. [Kaydet] düğmesine basın.

| Seçenek | Genişlik |
|---|---|
| [Otomatik] | Belirtilmez (otomatik boyutlandırma) |
| [Küçük (360px)] | 360px |
| [Orta (560px)] | 560px |
| [Büyük (760px)] | 760px |
| [Metin genişliği (920px)] | 920px |
| [Özel…] | 16 ile 4096px arasında herhangi bir tam sayı |

## Genişliği Markdown ile belirleme

HTML `img` etiketine sayısal bir `width` verin. Bu yazım biçimi GitHub'da ve MDX'te de aynı şekilde görsel olarak görüntülenir.

```html
<img src="./images/screen.png" alt="Ayarlar ekranı" width="360" />
```

> **Not**
>
> - `width` yalnızca bir sayı alır; `px` veya `%` eklenmez. Metin genişliğinden büyük bir değer belirtseniz bile görüntülenirken metin genişliğine sığdırılır.
> - Görsel yolları belgeye göre görecelidir. Belge kökünün dışındaki görseller gösterilmez.

## İlgili konular

- [Belge düzenleme](README.md)
- [Diyagramlar, matematik veya görseller görüntülenmiyor](../07-troubleshooting/rendering.md)
