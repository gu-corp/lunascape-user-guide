# Temel işlemler

Belgeleri açmaktan okumak istediğiniz sayfaya ulaşmaya kadarki temel işlemler.

## Belgeleri açma

1. VS Code'da depoyu açın.
2. Komut paletinde (`⇧⌘P` / `Ctrl+Shift+P`) “Lunascape Docs: Şartname görüntüleyicisini aç” komutunu çalıştırın.
   En yakın belge kökü (varsayılan olarak `docs` klasörü) bulunur ve başlangıç sayfası görüntülenir.

> **İpucu**
>
> - Gezgin'de bir Markdown dosyasına sağ tıklayıp [Lunascape Docs: Şartname görüntüleyicisinde aç] seçeneğini seçerseniz o dosyadan başlayabilirsiniz.
> - Herhangi bir belge köküne ait olmayan bir Markdown dosyasını açtığınızda, dosyanın bulunduğu klasör geçici bir belge kökü olarak görüntülenir.

## Sayfalar arasında gezinme

| İşlem | Yöntem |
|---|---|
| İçindekilerden açma | Soldaki INDEX'te belge adına basın |
| Bağlantı izleme | Metindeki bağlantıya basın. Aynı ekranda açılır |
| Geçmişte gezinme | Araç çubuğundaki [Geri] ve [İleri] düğmeleri ya da `Alt`+`←` / `Alt`+`→` |
| Başlangıç sayfasına dönme | Araç çubuğundaki [Şartname başlangıcı] |
| Bir üst düzeye çıkma | Araç çubuğundaki [Üst INDEX] ya da içerik haritasındaki bir öğe |
| Sayfa içinde gezinme | Sağdaki “Bu sayfada” bölümünde bir başlığa basın |

## Belge arama

INDEX'in üstündeki [Belgeleri filtrele] alanına bir sözcük yazdığınızda yalnızca adı eşleşen belgeler görüntülenir. Yazdığınızı sildiğinizde liste eski durumuna döner.

## İçeriği güncel duruma getirme

Markdown dosyasını VS Code'un düzenleyicisinde kaydettiğinizde görünüm otomatik olarak güncellenir. Dosyaları dış bir araçla değiştirdiğinizde araç çubuğundaki [Yeniden yükle] düğmesine basın.

> **Not**
>
> - Metindeki dış bağlantılar (`https://` gibi) varsayılan tarayıcıda açılır. Belge kökünün dışındaki dosyalara giden bağlantılar açılmaz.
> - Görüntülediğiniz belgeler cihazınızda işlenir. Belgeler, okunmak için dışarıya gönderilmez.

## İlgili konular

- [INDEX'i kullanma](index-panel.md)
- [Belge kökünü değiştirme](roots.md)
- [Belge düzenleme](../03-editing/README.md)
