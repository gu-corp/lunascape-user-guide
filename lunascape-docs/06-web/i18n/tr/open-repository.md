# GitHub deposu açma

Web sürümünde belgeleri, bir GitHub deposu belirterek açarsınız. Genel depolar için oturum açmanız gerekmez.

## Ekrandan açma

1. <https://docs.lunascape.org/> adresini açın.
2. Araç çubuğundaki [Belgeleri aç] (klasör simgesi) düğmesine basın.
3. [Depoyu doğrudan belirt] alanına depoyu yazın ve [Aç] düğmesine basın.
   GitHub'da oturum açmışsanız [Okuyabildiğiniz depolardan seç] ile listeden de seçebilirsiniz.

> **İpucu**
>
> - Yanındaki GitHub simgesi, okumakta olduğunuz belgeyi github.com üzerinde açar. Belge açma işlemi değildir.

## URL ile açma

Adres, deponun ve belgenin konumunu olduğu gibi sıralar. Yol, depo içindeki konum olduğundan GitHub URL'siyle aynı sırada yazılır.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Belirtilen | Yazılışı |
|---|---|
| Yalnızca depo (varsayılan dal) | `/github/owner/repo` |
| Depo içindeki bir belge | `/github/owner/repo/docs/01-product/vision.md` |
| Dal veya etiket belirtme | Sonuna `?ref=v1.2.0` ekleyin |

Sayfalar arasında gezindikçe adres de değişir. Araç çubuğundaki [Bu belgeyi paylaş] düğmesine bastığınızda, okumakta olduğunuz sayfanın bağlantısını başkasına verebilirsiniz. Tarayıcının [Geri] ve [İleri] düğmeleri de çalışır.

Önceki `?source=` biçimi de eskisi gibi açılır. Açıldıktan sonra yeni biçime dönüştürülür.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Not**
>
> - Oturum açmadığınızda GitHub API kullanım sınırı (saatte 60 istek) geçerlidir. Çok sayıda belge içeren depolarda veya tekrarlanan okumalarda [GitHub ile oturum aç] düğmesini kullanın.
> - `/` içeren dal adları (`feature/xxx` gibi) yukarıdaki adres biçiminde `?ref=` ile belirtilebilir. `?source=` biçiminde yazılamaz.
> - Belgeler, okuyucunun kendi GitHub yetkileriyle yüklenir. Okuma yetkisi olmayan kişilere görünmez.

## Yerel klasördeki belgeleri açma

Araç çubuğundaki [Belgeleri aç] düğmesine basın, listenin altındaki [Yerel klasördeki belgeleri aç] seçeneğinden cihazınızdaki klasörü seçin. Dosyalar tarayıcının içinde işlenir, dışarıya gönderilmez. Klasör seçimini destekleyen tarayıcılarda (Chrome, Edge gibi) kullanılabilir.

## İlgili konular

- [Özel depoyu görüntüleme](private-repository.md)
- [Web sürümü açılmıyor veya oturum açılamıyor](../07-troubleshooting/web.md)
