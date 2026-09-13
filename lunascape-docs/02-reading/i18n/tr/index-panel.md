# INDEX'i kullanma

Ekranın solundaki INDEX, belge kökündeki klasörlerin ve belgelerin ağacıdır.

## Filtreleme

1. INDEX'in üstündeki [Belgeleri filtrele] alanına bir sözcük yazın.
2. Yalnızca adı eşleşen belgeler görüntülenir. Yazdığınızı silerseniz eski durumuna döner.

> **Not**
>
> Filtreleme sırasında sürükle bırak ile sıralama yapılamaz.

## Klasörleri açma ve kapatma

- Klasör adının solundaki oka ya da kapak sayfası olmayan bir klasörün adına basarak klasörü açıp kapatabilirsiniz.
- Kapak sayfası (gövde metni olan bir `README.md` veya `index.md`) bulunan bir klasörde ada bastığınızda kapak sayfası açılır. Yalnızca açıp kapatmak için öğe menüsündeki [Klasörü aç] / [Klasörü kapat] seçeneklerini kullanın.
- Klasörlerin açık veya kapalı durumu her kullanıcı için ayrı olarak hatırlanır ve Git ile izlenen dosyalara yazılmaz.

## README ve klasör kapağı

`README.md`, ilgili klasörün içeriğini açıklayan dosyadır.

- README bulunan bir klasörde klasör adına bastığınızda o README görüntülenir.
- README bulunmayan bir klasörde, içindeki en üstteki belge görüntülenir.
- README'nin başlığı (H1), o klasörün INDEX'te görünen adı olur.

README zorunlu değildir. Sonradan eklemek için klasörün öğe menüsünden [README oluştur] seçeneğini seçin (yalnızca README'si olmayan klasörlerde görünür).

## INDEX'i gösterme / gizleme

- Araç çubuğundaki sütun denetimlerinin sol simgesi INDEX'i gösterir veya gizler. Sağdaki simge ise "Bu sayfada" bölümünü gösterir veya gizler.
- Ekran darken INDEX kapalı olarak başlar. [Geri] düğmesinin solunda görünen [INDEX'i aç] (üç çizgi) düğmesine bastığınızda INDEX, belgenin üzerine bindirilerek açılır. INDEX içindeki [×] ile, arka plana tıklayarak, `Esc` ile ya da başka bir belgeye geçerek kapatabilirsiniz. Bu geçici açma işlemi, geniş ekrandaki ayarı değiştirmez.
- Yalnızca tek bir belgenin görüntülendiği bir belge kökünde INDEX, yalnızca ilk açılışta kendiliğinden kapanır. Sütun simgesiyle yeniden açabilirsiniz. Bu davranışı [Görünüm ayarları] içindeki [Tek belge varsa otomatik olarak gizle] ile kapatabilirsiniz.

## Öğe menüsünü kullanma

INDEX'teki bir öğenin üzerine fareyle geldiğinizde görünen [⋯] düğmesiyle ya da öğeye sağ tıklayarak o öğenin menüsünü açın. Öğeler şu sırayla dizilir.

| Grup | Öğeler |
|---|---|
| Sık kullanılan işlemler | [Klasörü aç] / [Klasörü kapat], [INDEX'i aç] (klasörün kapak sayfasını açar), [Düzenle], [Başlığı değiştir], [VS Code'da aç], [Yolu kopyala] |
| Oluşturma ve düzenleme | [README oluştur] (yalnızca README'si olmayan klasörlerde), [Yeni belge], [Yeni klasör], [Çoğalt], [Dosya adını değiştir] / [Klasör adını değiştir], [Bir yukarı taşı], [Bir aşağı taşı] |
| Silme | [Çöp kutusuna taşı] |

- Doğrudan belge kökünün altında oluşturmak için INDEX başlığının sağ ucundaki [⋯] düğmesini kullanın ya da INDEX'in boş bir yerine sağ tıklayıp [Yeni belge] veya [Yeni klasör] seçeneğini seçin. Aynı menüde [Belge adını değiştir] ve belge kökünde README yoksa [README oluştur] seçenekleri de yer alır. Araç çubuğunda görünen belge adına sağ tıkladığınızda da aynı menü açılır.
- Menü içinde `↑` `↓` tuşlarıyla öğeler arasında gezinir, `Home` `End` tuşlarıyla ilk ve son öğeye gidersiniz. `Esc` ile kapattığınızda odak, menüyü açmadan önceki yerine döner.

> **Not**
>
> Oluşturma, düzenleme ve silme öğeleri yalnızca çalışma alanı VS Code'da güvenilen çalışma alanı olduğunda görünür. Bir belge düzenlenirken veya başka bir INDEX işlemi sürerken de kullanılamaz.

## Görünümü değiştirme

[Görünüm ayarları] üzerinden dosya adlarının gösterimini, belge ve klasör simgelerini, klasör içindeki öğe sayısını, hiyerarşi kılavuz çizgilerini ve görüntüleme yoğunluğunu değiştirebilirsiniz. Ayrıntılar için bkz. [Görünüm ayarlarını değiştirme](display-settings.md).

## İlgili konular

- [Belge ve klasör oluşturma ve düzenleme](../03-editing/organize.md)
- [Belgelerin sıralamasını değiştirme](../03-editing/reorder.md)
