# Düzenleme, kaydetme veya sıralama yapılamıyor

## [Düzenle] düğmesi yok

- [Görünüm ayarları] içindeki [Düzenleme düğmesi] kapalı. Açın ya da belgenin sağ üstündeki [⋯] → [Düzenle] veya INDEX öğe menüsündeki [Düzenle] seçeneğini kullanın.
- `lunascape-docs.json` dosyasındaki `editor.showEditButton` değeri `false` olduğunda da aynı durum geçerlidir.
- Yardım görüntülenirken düzenleme yapılamaz. Yardımı kapatın.

## Görsel görünüme geçilemiyor

"Bu belgede MDX söz dizimi bulunduğu için normal düzenleme ekranına geçilemiyor": MDX'e özgü söz dizimi (bileşenler, `import` vb.) içeren belgeler, bu söz dizimini korumak için yalnızca Markdown görünümünde düzenlenir.

## Matematik veya diyagram doğrudan düzenlenemiyor

Görsel görünüm, çizim sonucunu gösterir. Düzenleme ekranında [Markdown] düğmesine basıp kaynağı düzenleyin.

## Sıralama veya sürükleme yapılamıyor

- Süzme sırasında, belge düzenlenirken ve başka bir INDEX işlemi sürerken sıralama yapılamaz.
- Çalışma alanı güvenilen olarak işaretlenmediğinde oluşturma, düzenleme ve silme işlemleri kullanılamaz. Çalışma alanını VS Code'da güvenilen olarak işaretleyin.
- "INDEX güncellendi. Lütfen yeniden sürükleyin": Başka bir değişiklik az önce uygulandı. İşlemi yineleyin.
- Başlangıç sayfası (kökteki `README.md`) taşınamaz.

## "Kaydedilmemiş değişiklikler var" iletisi görünüyor

İlgili dosya VS Code düzenleyicisinde açık ve değiştirilmiş durumda. Önce değişiklikleri kaydedin veya geri alın, sonra yeniden deneyin.

## Ad değiştirilemiyor

Aşağıdaki adlar kullanılamaz.

- `.` ile başlayan adlar, `i18n` ve Windows'un ayrılmış adları (`CON` vb.)
- Nokta veya boşlukla biten adlar, denetim karakterleri ya da dosya adında kullanılamayan karakterler içeren adlar
- Aynı klasörde hâlihazırda bulunan adlar (yalnızca büyük/küçük harf bakımından farklı olanlar dâhil)
- Markdown uzantısı taşımayan belge adları

## Kaydedildiği hâlde Git'te değişiklik görünmüyor veya işlenmiyor

Lunascape Docs yalnızca dosyaya yazar; Git'te hazırlama veya işleme yapmaz. VS Code'un Kaynak Denetimi görünümünden denetleyin ve gerekirse değişiklikleri işleyin.

## İlgili konular

- [Belge düzenleme](../03-editing/README.md)
- [Belge ve klasör oluşturma ve düzenleme](../03-editing/organize.md)
- [Belge sıralamasını değiştirme](../03-editing/reorder.md)
