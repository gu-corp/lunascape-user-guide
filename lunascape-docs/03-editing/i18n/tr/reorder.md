# Belge sıralamasını değiştirme

INDEX içinde görünen sıra, sürükle bırak ile veya klavyeden değiştirilebilir. Değiştirilen sıra, belgenin front matter bölümüne `navigation.order` olarak kaydedilir.

## Sürükle bırak ile sıralama

1. INDEX içinde bir belgeyi veya klasörü sürükleyin.
2. Aynı düzeydeki bir ögenin önüne ya da arkasına veya bir klasörün üzerine bırakın.
   Aynı düzey içinde sıra değişir. Başka bir klasörün üzerine bırakıldığında, öge o klasöre taşınır.

## Klavye veya menü ile sıralama

- INDEX içindeki bir ögeye odaklanın ve `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓` tuşlarına basın.
- Öge menüsünden [Bir yukarı taşı] / [Bir aşağı taşı] seçeneğini seçin.

## Kaydedilenler

- Aynı düzeyde sıralama yapıldığında, asıl belgenin front matter bölümündeki `navigation.order` güncellenir. Klasörlerde bu bilgi, klasörün `README.md` dosyasına yazılır. `README.md` dosyası bulunmayan klasörlerde, yalnızca front matter içeren bir `README.md` oluşturulur.
- Başka bir klasöre taşındığında, asıl belge ve karşılık gelen çevirileri birlikte taşınır. Taşımadan önce, göreli bağlantılara olan etkiyle ilgili bir onay görüntülenir.
- Git'te hazırlama (staging) veya işleme (commit) yapılmaz.

> **Not**
>
> - Süzme sırasında, belge düzenlenirken ve güvenilmeyen çalışma alanlarında sıralama yapılamaz.
> - "INDEX güncellendi" iletisi göründüğünde, başka bir değişiklik yeni uygulanmış demektir. İşlemi yeniden yapın.
> - Başlangıç sayfası başka bir klasöre taşınamaz.

> **İpucu**
>
> `navigation.order` değerlerini 100, 200, 300 gibi 100'er artışlarla verirseniz, sonradan araya belge eklemek kolaylaşır. Ayrıntılar için bkz. [Gezinme bilgilerini ayarlama](../04-document-tools/navigation-metadata.md).

## İlgili konular

- [Belge ve klasör oluşturma ve düzenleme](organize.md)
- [Gezinme bilgilerini ayarlama](../04-document-tools/navigation-metadata.md)
