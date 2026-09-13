# Özel bir depoyu görüntüleme

GitHub ile oturum açtığınızda, özel depoların belgelerini yalnızca okuma izniniz olanlarla sınırlı olarak görüntüleyebilirsiniz. Lunascape Docs'un kendine ait bir hesabı veya izni yoktur.

## Oturum açıp açma

1. <https://docs.lunascape.org/> adresini açın.
   Özel bir belge belirttiğinizde veya henüz oturum açmadığınızda oturum açma ekranı görünür.
2. [GitHub ile oturum aç] düğmesine basın.
   GitHub kimlik doğrulama ekranı bir açılır pencerede açılır.
3. Oturum açtıktan sonra araç çubuğundaki [Belgeleri aç] düğmesine basın ve [Okuyabildiğiniz depolardan seç] ile açmak istediğiniz depoyu seçin.

> **İpucu**
>
> - Oturum açtığınız hesabın adı araç çubuğunda görünür. [Oturumu kapat] veya [Başka bir hesapla oturum aç] işlemlerini de buradan yapabilirsiniz.
> - Listede, "Lunascape Docs" GitHub App'inin yüklü olduğu hesapların (kuruluş veya kişisel) depolarından, yalnızca okuma izniniz olanlar görünür.

## Depo sahibinin yapacağı ayarlar

İlgili depo listede görünmüyorsa, deponun sahibi veya kuruluşun yöneticisi "Lunascape Docs" GitHub App'ini yüklemelidir.

- İstenen izinler Contents (okuma ve yazma) ile Pull requests (okuma ve yazma) izinleridir. Okuma görüntüleme içindir; yazma ise Web üzerinden gönderilen yayımlama isteği (Pull Request) içindir. Lunascape Docs belgelerin içeriğini saklamaz.
- Yükleme birimi hesaptır (kuruluş veya kişisel). Hedefin "All repositories" (bundan sonra oluşturulacak depoları da otomatik olarak içerir) mı yoksa yalnızca seçilen depolar mı olacağını ayarlarsınız.

| Durum | Adımlar |
|---|---|
| Yeni bir kuruluşa veya kişisel hesaba kurma | [Yükleme sayfasından](https://github.com/apps/lunascape-docs/installations/new) gerçekleştirin |
| Kurulu bir kuruluşta hedef depo ekleme | Kuruluşun Settings → GitHub Apps → Lunascape Docs → Configure → Repository access bölümünden ayarlayın |

Uygulama kuruluşun tamamına yüklenmiş olsa bile, her üye yalnızca kendi okuma iznine sahip olduğu depoları görüntüleyebilir. Yayımlama isteğini de yalnızca kendi yazma iznine sahip olduğu depolara gönderebilir.

> **İpucu**
> - Yeni bir kurulumda istenen izinler kurulum ekranında bir liste hâlinde görünür ve "Install" düğmesine bastığınız anda onaylamış olursunuz. Başka bir işlem gerekmez.
> - İzinler eklenmeden önce uygulamayı yüklemiş olan bir kuruluşa yöneticilere bir onay e-postası gelir ve kuruluşun Settings → GitHub Apps → Lunascape Docs → Configure bölümünün üstünde bir onay düğmesi görünür. Onaylanana kadar o kuruluşta yalnızca görüntüleme yapılabilir; yayımlama isteği gönderildiğinde "yazma izni verilmesi gerekiyor" mesajı görünür.
> - Şu anda hangi izinlerle yüklü olduğunuzu aynı Configure ekranında görebilirsiniz. Kişisel hesaplarda bu, Settings → Applications → Installed GitHub Apps bölümüdür.
> - Hedef depoyu yanlışlıkla çıkardıysanız veya uygulamayı kaldırdıysanız, [yükleme sayfasından](https://github.com/apps/lunascape-docs/installations/new) yeniden yükleyerek eski durumuna getirebilirsiniz. Reddedilen yayımlama isteği mesajı, düzeltme ekranına bir bağlantı içerir.
> - Depo tarafında yayımlama isteği kabul etmek istemiyorsanız, `lunascape-docs.json` dosyasına `"publish": { "enabled": false }` yazın. Görüntüleme olduğu gibi kullanılmaya devam eder.

## İlgili konular

- [GitHub deposu açma](open-repository.md)
- [Web sürümü açılmıyor veya oturum açılamıyor](../07-troubleshooting/web.md)
