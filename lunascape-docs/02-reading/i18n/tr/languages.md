# Başka bir dilde okuma

Bir belgenin çevirisi varsa, araç çubuğundaki dil menüsünden (küre) dili değiştirerek okuyabilirsiniz.

## Dili değiştirme

1. Araç çubuğundaki dil menüsüne basın.
   Görüntülenen sayfanın dili ve bunun dayanağı (çevirinin yolu, otomatik algılama, projenin varsayılan dili) gösterilir.
2. Okumak istediğiniz dili seçin.
   Aynı belgenin çevirisi açılır. Seçtiğiniz dil hatırlanır; bir sonraki açtığınız belgede de çeviri varsa o dilde gösterilir.

Listede, her dil için bu belgenin çevirisinin olup olmadığı gösterilir.

| Gösterim | Anlamı |
|---|---|
| Çeviri var | Bir çeviri mevcut ve açılabilir |
| Çeviri yok | Dil projede destekleniyor, ancak bu belgenin henüz çevirisi yok |
| Güncelleme var | Çeviri mevcut, ancak çeviriden sonra asıl belge değişmiş |

> **Not**
>
> - Bir dil seçmek yalnızca var olan çeviriyi açar. Çeviri üretmez, dosya oluşturmaz. Çeviri oluşturmak için aynı menüdeki [Çeviri oluştur ve yönet…] öğesini kullanın.
> - Görüntülenen sayfanın dili projenin varsayılan dilinden farklı olarak belirlendiğinde bir uyarı gösterilir. Ayarlar hiçbir zaman değiştirilmez.

## İlk gösterilen dil

Bir belge açıldığında ilk görüntüleme dili şu sırayla belirlenir.

1. Bu belge kökünde daha önce kendi seçtiğiniz dil. Seçiminiz kaydedilir (varsayılan dili seçtiğinizde de bu bir seçim olarak kaydedilir).
2. VS Code'un görüntüleme dili (Web tarayıcı sürümünde tarayıcının dil ayarı). Desteklenen dillerden eşleşen biri otomatik seçilir. Bölge etiketli diller (`en-US` gibi) temel dille (`en`) de eşleşir.
3. Projenin yedek dili (`lunascape-docs.json` içindeki `fallbackLocale`).
4. Projenin varsayılan dili.

> **İpucu**
>
> - Otomatik seçim yapıldığında, dil menüsündeki geçerli dilin yanında "otomatik seçildi" ifadesi görünür. İşaretçiyi rozetin üzerine getirdiğinizde nedeni gösterilir.
> - `fallbackLocale`, okuma ortamının dili desteklenen dillerin hiçbiriyle eşleşmeyen okuyuculara gösterilecek dildir. Asıl dili Japonca olan ve İngilizce sürümü bulunan bir projede `"en"` ayarlanırsa, örneğin İspanyolca ortamdaki okuyucuya İngilizce sürüm açılır. Ayarlanmadığında varsayılan dil kullanılır.

## Çevirilerin bulunduğu yer

Varsayılan dildeki belgeler olduğu yerde kalır; çeviriler ise **aynı klasördeki `i18n/<dil>/` klasörüne**, aynı dosya adıyla konur.

```text
docs/
  README.md                  ← default language (for example Japanese)
  i18n/en/README.md          ← its English translation
  guide/
    setup.md
    i18n/en/setup.md         ← its English translation
```

> **Not**
>
> - Klasör yapısını `i18n/` altında yeniden kurmak (`i18n/en/guide/setup.md`) tanınmaz. `i18n/` klasörü her zaman, çevirdiği belgeyle aynı klasörde bulunur.
> - Çevirinin çözümlendiği tek yer burasıdır. Aynı belgenin çevirisini üst klasördeki `i18n/` içine de koymak "hangisi öncelikli" çatışmasına yol açmaz; oradaki kopya yalnızca dil menüsünde de kayıtta da hiç görünmeyen öksüz bir dosya olur (ve otomatik olarak silinmez). Aynı çeviriyi iki yere koymayın.

## Web tarayıcı sürümünde okuma

Web tarayıcı sürümünde de çeviri varsa aynı şekilde dil değiştirilebilir. Çevirisi olmayan bir dilde okumak istediğinizde tarayıcının sayfa çevirisi özelliğini kullanabilirsiniz. Kod, matematik ve diyagramlar çeviri kapsamının dışında tutulur.

## İlgili konular

- [Çalışmayı bir yapay zekâya devretme](../05-ai/README.md)
- [Devredilebilecek işler](../05-ai/tasks.md)
- [Görünüm ayarlarını değiştirme](../02-reading/display-settings.md)
