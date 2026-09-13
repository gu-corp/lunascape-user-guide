# Taslak kaydetme

Web sürümünde bir belgeyi düzenlediğinizde, değişiklikler depoya yazılmaz; tarayıcının içinde “taslak” olarak saklanır.

## Taslak oluşturma

1. Bir belgeyi açın ve sağ alttaki [Düzenle] düğmesine basın.
2. Düzenleyip [Kaydet] düğmesine basın.
   “Taslak olarak kaydedildi” iletisi görünür ve değişiklik tarayıcıda saklanır.

- Taslağı olan belgeler INDEX içinde bir rozetle işaretlenir. Metnin üstünde “Bu belge, bu cihazdaki bir taslaktır (yayımlanmadı)” yazısı görünür.
- Araç çubuğundaki [Taslaklar] düğmesi taslak sayısını gösterir; düğmeye basıldığında taslak listesi açılır.

## Taslağı atma

- Tek bir belgenin taslağını atmak için metnin üstündeki [Taslağı at] düğmesine basın.
- Tümünü atmak için taslak listesini kullanın.

## Depoya yansıtma

Taslakları pull request olarak gönderen “Yayımlama isteği” uygulanmıştır, ancak genel görüntüleyicide etkin değildir. Depoya yansıtmak için VS Code sürümünde ya da elinizdeki kopyada düzenleme yapın.

> **Not**
>
> - Taslaklar tarayıcıda (IndexedDB) saklanır. Başka bir tarayıcıya veya başka bir cihaza aktarılmaz. Tarayıcının site verilerini silerseniz taslaklar da silinir.
> - Taslağı oluşturduktan sonra depodaki belge güncellenirse “Üst kaynak güncellendi” yazısı görünür. İçeriği gözden geçirip taslağı atmaya mı yoksa olduğu gibi kullanmaya mı karar verin.
> - [Belgeleri aç] ile açtığınız yerel bir klasörü düzenlediğinizde, tarayıcı destekliyorsa değişiklikler doğrudan dosyaya kaydedilir. Desteklemeyen tarayıcılarda yalnızca o oturum boyunca saklanır.

## İlgili konular

- [Web sürümüyle neler yapabilirsiniz](README.md)
- [Belgeyi düzenleme](../03-editing/README.md)
