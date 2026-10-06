# Bir GitHub deposunu açma

Web sürümünde GitHub depolarını klonlamadan doğrudan açıp okuyabilirsiniz. Herkese açık depolar için oturum açmanız gerekmez.

## Ekrandan açma

1. Araç çubuğundaki [Belgeleri aç] düğmesine (klasör simgesi) basın. “Belgeleri aç” ekranı açılır.
2. Soldaki sütunda açılacak konumu seçin.

   | Konum | Listelenenler |
   |---|---|
   | Tümü | Aşağıdakilerin tümü. Son açılanlar en üstte listelenir |
   | Son açılanlar | Daha önce açtığınız depolar ve klasörler |
   | Önerilenler | Sitenin tanıttığı kılavuzlar |
   | GitHub depoları | GitHub ile oturum açtığınızda, okuyabildiğiniz depolar |
   | Bu bilgisayar | Bu cihazdaki klasörler |

3. Açmak istediğiniz satırdaki [Aç] düğmesine basın. Üstteki [Belge veya depo adıyla filtrele] alanına yazarak satırları daraltabilirsiniz.

Listede olmayan bir depoyu, soldaki sütunda bulunan [owner/repo girerek aç] ile belirtin.

> **İpucu**
>
> - Listede görünen GitHub depoları, “Lunascape Docs” GitHub App'inin yüklü olduğu ve sizin okuma izninizin bulunduğu depolardır. Aradığınız depo görünmüyorsa depo sahibinden App'i eklemesini isteyin.

## Belgenin konumunu kontrol etme

Araç çubuğunun sol tarafındaki küçük simge (konum çipi), okuduğunuz belgenin nerede olduğunu gösterir.

| Simge | Konum |
|---|---|
| GitHub işareti | GitHub'dan okunuyor. Bu cihaza kaydedilmemiştir |
| Klasör | Bu cihazdaki bir klasör |

Simgeye bastığınızda konum, durum ve oradan yapabileceğiniz işlemler ([GitHub'da görüntüle], [Bağlantıyı kopyala] vb.) görüntülenir.

## URL ile açma

Adres, deponun ve belgenin konumunu olduğu gibi sıralayan bir biçimdedir. Yol, depo içindeki konumu gösterdiği için GitHub URL'siyle aynı sırayı izler.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Belirtilen | Yazılışı |
|---|---|
| Yalnızca depo (varsayılan dal) | `/github/owner/repo` |
| Depo içindeki bir belge | `/github/owner/repo/docs/01-product/vision.md` |
| Dal veya etiket belirtme | Sonuna `?ref=v1.2.0` ekleyin |

Sayfalar arasında geçiş yaptığınızda adres de değişir. Araç çubuğundaki [Bu belgeyi paylaş] düğmesine basarak okuduğunuz sayfanın bağlantısını başkasına iletebilirsiniz. Tarayıcının [Geri] ve [İleri] düğmeleri de kullanılabilir.

Eski `?source=` biçimi de önceden olduğu gibi açılır. Açıldıktan sonra adres yeni biçime dönüştürülür.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Not**
>
> - Oturum açmadığınızda GitHub API kullanım sınırı (saatte 60 istek) uygulanır. Çok sayıda belge içeren depolarda veya tekrarlı okumalarda [GitHub ile oturum aç] düğmesine basın.
> - `/` içeren dal adları (`feature/xxx` gibi), yukarıdaki adres biçiminde `?ref=` ile belirtilebilir. `?source=` biçiminde yazılamaz.
> - Belgeler, okuyan kişinin GitHub izinleriyle yüklenir. Okuma izni olmayan kişiler belgeleri göremez.

## Yerel klasördeki belgeleri açma

Araç çubuğundaki [Belgeleri aç] düğmesine basın ve soldaki sütunda bulunan [Yerel klasördeki belgeleri aç] ile cihazınızdaki bir klasörü seçin. Dosyalar tarayıcının içinde işlenir ve dışarıya gönderilmez. Klasör seçimini destekleyen tarayıcılarda (Chrome, Edge vb.) kullanılabilir.

## İlgili konular

- [Özel bir depoyu görüntüleme](private-repository.md)
- [Web sürümü açılmıyor veya oturum açılamıyor](../07-troubleshooting/web.md)
