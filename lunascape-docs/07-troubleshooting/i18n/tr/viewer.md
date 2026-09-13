# Belgeler görünmüyor

## "Açılabilecek Markdown veya docs klasörü bulunamadı" iletisi görünüyor

- Çalışma alanında `docs` klasörü yok ya da `docs` dışında bir ad kullanılıyor.
  - `lunascape-docs.json` dosyasını o klasöre koyarsanız, adı ne olursa olsun belge kökü olarak tanınır.
  - Ya da `lunascapeDocEditor.rootDirectoryNames` ayarına klasör adını ekleyin.
- Henüz belge yoksa, "Lunascape Docs: Şablondan belge oluştur" ile oluşturun.
- Bir Markdown dosyasını düzenleyicide açıp "Lunascape Docs: Şartname görüntüleyicisinde aç" komutunu çalıştırmak da bir yoldur.

## Belge INDEX'te görünmüyor

- Uzantının `.md`, `.markdown` veya `.mdx` olduğunu doğrulayın.
- Şu klasörler görünmez: `.` ile başlayan klasörler, `node_modules` ve `ignoredDirectories` içinde belirtilen klasörler (varsayılan: `99-archive`).
- `i18n/` altındaki çeviriler INDEX'te ayrı ayrı görünmez. Dil menüsünden geçiş yapın.
- Yeni eklediğiniz bir dosya görünmüyorsa [Yeniden yükle] düğmesine basın.
- Başka bir belge köküne bakıyor olabilirsiniz. Araç çubuğunun en solundaki belge kökü adını denetleyin.

## Klasöre bastığımda hiçbir şey görünmüyor

O klasörün `README.md` dosyası, yalnızca front matter içeren, gövdesi olmayan bir "yalnızca ayar tanımlayıcısı"dır. INDEX'te klasörü açıp içindeki belgeyi seçin.

## İstenmeyen bir belge kökü açılıyor

- `lunascapeDocEditor.rootMode` ayarı `fixed` ise her zaman `lunascapeDocEditor.root` açılır.
- `auto` ayarında, açılan Markdown dosyasına en yakın belge kökü seçilir. Araç çubuğunun en solundaki açılır listeden değiştirebilirsiniz.

## Belge kökünün adı beklediğim gibi değil

Ad şu sırayla belirlenir: `lunascape-docs.json` içindeki `title` → kök `README.md` dosyasının `navigation.title` değeri → onun H1 başlığı → `index.md` → klasör adı. Sabitlemek isterseniz `title` değerini ayarlayın.

## INDEX kayboldu

- Yalnızca 1 belge içeren belge köklerinde INDEX yalnızca ilk seferde kendiliğinden kapanır. Araç çubuğundaki sütun görünümü simgesiyle açabilirsiniz. [Görünüm ayarları] içindeki [Tek belge varsa otomatik olarak gizle] seçeneğiyle kapatabilirsiniz.
- Ekran dar olduğunda, [Geri] düğmesinin solundaki [INDEX'i aç] (üç çizgi) düğmesinden açın.

## Bağlantıya bastığımda açılmıyor

- "Bağlantı hedefi bulunamadı": bağlantının hedef dosyası yok. Belge Araçları'ndaki [Denetim] ile iç bağlantıları doğrulayabilirsiniz.
- "Güvenli olmayan veya desteklenmeyen bağlantı açılmadı": belge kökünün dışına ya da `https://` ve `mailto:` dışındaki şemalara giden bağlantılar açılmaz.

## Görünen dil istediğim gibi değil

- Dil menüsünden, görüntülenen sayfanın dilini ve bunun dayanağını denetleyin.
- En son seçtiğiniz görüntüleme dili anımsanır. Dil menüsünden varsayılan dili yeniden seçin.
- Kişisel `lunascapeDocEditor.locale` ayarı tanımlıysa, o dilin çevirisi yeğlenir.

## İlgili konular

- [Belge kökleri arasında geçiş yapma](../02-reading/roots.md)
- [Belge kökleri ve dosya kuralları](../04-document-tools/structure.md)
