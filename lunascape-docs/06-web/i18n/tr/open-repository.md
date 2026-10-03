# Bir GitHub deposunu açma

Web sürümünde ve Lunascape'te bir GitHub deposunu çoğaltmadan doğrudan açıp okuyabilirsiniz. Herkese açık depolar için oturum açmanız gerekmez.

## Ekrandan açma

1. Araç çubuğundaki [Belgeleri aç] düğmesine (klasör simgesi) basın. “Belgeleri aç” ekranı açılır.
2. Soldaki sütunda, açılacak yeri seçin.

   | Yer | Listelenenler |
   |---|---|
   | Tümü | Aşağıdakilerin tümü. Son açılanlar en üstte yer alır |
   | Son açılanlar | Daha önce açtığınız depolar ve klasörler |
   | Önerilenler | Sitenin tanıttığı kılavuzlar |
   | GitHub depoları | GitHub ile oturum açtığınızda, okuyabildiğiniz depolar |
   | Bu bilgisayar | Bu cihazdaki klasörler. Lunascape'te çoğalttığınız depolar da burada yer alır |

3. Açmak istediğiniz satırdaki [Aç] düğmesine basın. Üstteki [Belge veya depo adıyla filtrele] alanına yazarak satırları daraltabilirsiniz.

Listede olmayan bir depoyu açmak için soldaki sütunda [owner/repo girerek aç] seçeneğini kullanın.

> **İpucu**
>
> - Listede görünen GitHub depoları, “Lunascape Docs” GitHub App'inin yüklü olduğu ve okuma izninizin bulunduğu depolardır. Bir depo görünmüyorsa depo sahibinden uygulamayı eklemesini isteyin.

## Belgenin yerini kontrol etme

Araç çubuğunun sol tarafındaki küçük simge (konum etiketi), okuduğunuz belgenin nerede olduğunu gösterir.

| Simge | Konum |
|---|---|
| GitHub logosu | GitHub'dan okuyorsunuz. Belge bu cihaza kaydedilmemiştir |
| Bilgisayar | Lunascape'in yönettiği, bu cihazdaki bir klasör. Git dal adı ve değiştirilen dosya sayısı da gösterilir |
| Klasör | Bu cihazdaki bir klasör |

Simgeye bastığınızda konum, durum ve oradan yapabileceğiniz işlemler ([GitHub'da görüntüle], [Bağlantıyı kopyala] vb.) gösterilir.

## Lunascape'te bir depoyu çoğaltma

Lunascape'te bir GitHub deposunu bu cihaza çoğaltabilir, ardından Git ile düzenleme yapıp commit edebilirsiniz.

- “Belgeleri aç” ekranında deponun satırındaki [Çoğalt] düğmesine basın.
- GitHub'dan açılmış bir depoyu okurken konum etiketine, ardından [Bu bilgisayara çoğalt] düğmesine basın. Çoğaltma bittiğinde aynı belge, bu cihazdaki kopyadan açılır.

Çoğaltılan depo listede “Bu bilgisayarda” olarak işaretlenir ve satırında ilk olarak [Bu bilgisayarda aç] düğmesi yer alır.

## URL ile açma

Adres, depoyu ve belgenin konumunu sırayla içerir. Yol, belgenin depo içindeki konumu olduğundan adres aynı dosyanın GitHub URL'si ile aynı sırayı izler.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Belirtilecek | Yazılışı |
|---|---|
| Yalnızca depo (varsayılan dal) | `/github/owner/repo` |
| Depo içindeki bir belge | `/github/owner/repo/docs/01-product/vision.md` |
| Dal veya etiket | Sonuna `?ref=v1.2.0` ekleyin |

Başka bir sayfaya geçtiğinizde adres de değişir. Okuduğunuz sayfanın bağlantısını birine iletmek için araç çubuğundaki [Bu belgeyi paylaş] düğmesine basın. Tarayıcının [Geri] ve [İleri] düğmeleri de çalışır.

Eski `?source=` biçimi de eskisi gibi açılır. Sayfa açıldıktan sonra adres yeni biçime dönüştürülür.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Dikkat**
>
> - Oturum açmadığınızda GitHub API kullanım sınırı (saatte 60 istek) uygulanır. Çok sayıda belge içeren depolar için ya da sayfaları tekrar tekrar okuyacaksanız [GitHub ile oturum aç] düğmesiyle oturum açın.
> - `/` içeren dal adları (`feature/xxx` gibi) yukarıdaki adres biçiminde `?ref=` ile belirtilebilir. `?source=` biçiminde bu dal adları yazılamaz.
> - Belgeler, okuyan kişinin GitHub izinleriyle yüklenir. Okuma izni olmayan kişiler belgeleri göremez.

## Yerel klasördeki belgeleri açma

Araç çubuğundaki [Belgeleri aç] düğmesine basın. Soldaki sütunda [Yerel klasördeki belgeleri aç] seçeneğine basın ve cihazdaki bir klasörü seçin. Dosyalar tarayıcı içinde işlenir ve hiçbir yere gönderilmez. Bu özellik, klasör seçmeyi destekleyen tarayıcılarda (Chrome, Edge vb.) kullanılabilir.

## İlgili konular

- [Özel bir depoyu görüntüleme](private-repository.md)
- [Web sürümü açılmıyor veya oturum açılamıyor](../07-troubleshooting/web.md)
