# Web sürümünde açılamıyor veya oturum açılamıyor

## Oturum açıldı, ancak depo listede görünmüyor

O hesapta "Lunascape Docs" GitHub App'i yüklü değildir veya ilgili depo kapsama dahil edilmemiştir. Depo sahibinden ya da kuruluş yöneticisinden, [Özel bir depoyu görüntüleme](../06-web/private-repository.md) sayfasındaki adımlara göre yüklemesini isteyin.

## Oturum açma ekranından ileri gidilemiyor

- İlgili depo için okuma izniniz yok. Depo sahibinden izin vermesini isteyin.
- "Bu sitede GitHub oturum açma yapılandırılmamış": kendi yerleştirdiğiniz görüntüleyicide oturum açma hizmeti yapılandırılmamıştır. Bir yöneticinin oturum açma hizmetini yapılandırması gerekir.

## Oturum açma penceresi açılmıyor

Tarayıcı açılır pencereyi engelliyor. Bu site için açılır pencerelere izin verdikten sonra yeniden deneyin.

## "Oturumunuzun süresi doldu" görünüyor

Oturumun süresi doldu. Yeniden [GitHub ile oturum aç] düğmesine basın.

## Genel bir depo açıldığında 404 dönüyor

- `owner/repo@ref/dir` yazımını denetleyin.
- İçinde `/` bulunan dal adları belirtilemez.

## Bir süre sonra yükleme yapılamıyor

Oturum açmadığınızda GitHub API kullanım sınırı (saatte 60 istek) geçerlidir. "İstek sınırına ulaşıldı" görüntülendiğinde bir süre bekleyin veya [GitHub ile oturum aç] düğmesini kullanın.

## "Bu siteden bu depo görüntülenemez" görünüyor

Kendi yerleştirdiğiniz görüntüleyiciden açmak için, deponun `lunascape-docs.json` dosyasındaki `viewer.origins` alanına o sitenin URL'sini eklemeniz gerekir.

## `index.html` açıldığında hiçbir şey görünmüyor

`file://` ile doğrudan açıldığında çalışmaz. HTTP sunucusu üzerinden açın veya VS Code sürümünü kullanın.

## Dışa aktarılan sitede "lunascape-docs-manifest.json bulunamadı" görünüyor

`npm run export:web` ile oluşturulan dosyaların tamamını (manifest dahil) olduğu gibi yerleştirin.

## Taslak kaydedilemiyor

- "IndexedDB açılamıyor" / "Başka bir sekmede kullanımda": tarayıcının gizli modundan ya da aynı siteyi açan başka bir sekmeden kaynaklanır. Normal bir pencerede açın ve diğer sekmeleri kapatın.
- Taslaklar aygıt ve tarayıcı başına kaydedilir. Başka bir aygıta aktarılmaz.

## İlgili konular

- [GitHub deposunu açma](../06-web/open-repository.md)
- [Taslak kaydetme](../06-web/drafts.md)
