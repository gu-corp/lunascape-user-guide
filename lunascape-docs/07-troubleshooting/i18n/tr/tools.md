# Denetim, oluşturma veya çeviri yapılamıyor

## Denetim

### “docs-lint kullanılamıyor” iletisi görüntüleniyor

- Uzantı docs-lint çalışma ortamını içermiyor ya da ayarlarda bir sorun var. Uzantıyı yeniden kurun.
- “Yerel Pack’i ve ayarları güvenli biçimde yüklemek için bu çalışma alanına VS Code’da güvenin”: yerel Standard Pack’i kullanmak için güvenilen çalışma alanı gerekir.

### Sonuç “yeniden denetim gerekli” olarak kalıyor

Bir belgeyi veya ayarı değiştirdiğinizde önceki sonuç geçersiz olur. [Belge kökünü denetle] düğmesine yeniden basın. Kaydedilmemiş değişiklikler yansıtılmaz.

### Bulguya bastığınızda hiçbir şey açılmıyor

“Belge kökünün tamamı” başlıklı maddeler belirli bir belgeye bağlı olmadığından bir konumları yoktur. Bulgunun içeriğine göre ilgili belgeleri denetleyin.

### Kurallar kaydedilemiyor

- Güvenilen çalışma alanı gerekir.
- “Lint ayarları başka bir işlem tarafından değiştirildi”: `docs-lint.config.json` dışarıdan değiştirilmiş. En son durumu yükleyip yeniden deneyin.
- Sembolik bağ olan veya belge kökünün dışında bulunan ayar dosyaları düzenlenemez.

## Şablondan oluşturma

- “Şablon önizlemesinin süresi doldu” / “Girilen bilgiler değişti”: oluşturmadan önce [Önizleme] düğmesine yeniden basın.
- “Hedefte zaten bir belge var”: var olan dosyaların üzerine yazılmaz. Başka bir hedef belirtin.
- Hedef için belge köküne göre göreli bir yol ve `.md` / `.mdx` uzantısı gerekir. `i18n` altında belge oluşturulamaz.
- “Belge oluşturmak için çalışma alanına güvenin”: VS Code’da çalışma alanına güvenin.

<!-- ai-only:start -->
## Çeviri

### Çeviri düğmeleri etkin değil

- “Bu belge kökünde yapay zekâ çevirisi etkin değil”: `lunascape-docs.json` dosyasındaki `translation.enabled` değerini `true` yapın.
- “Proje varsayılan dili ayarlanmamış”: [Görünüm ayarlarını değiştirme](../02-reading/display-settings.md) bölümündeki gibi varsayılan dili kaydedin.
- “Hedef dili desteklenen dillere ekleyin”: çeviri hedefi olan dili `locales` listesine ekleyin.
- “Çevrilecek asıl belge bulunamadı”: çeviri sayfası açık. Varsayılan dildeki sayfaya geçin.
- Klasör geçici olarak görüntülenirken toplu çeviri kullanılamaz. O klasöre bir `lunascape-docs.json` koyarak onu belge kökü yapın.

### Çeviri önerisi reddediliyor veya yeniden oluşturulması isteniyor

- “Asıl belge değişti. Çeviri önerisini yeniden oluşturun”: öneri hazırlandıktan sonra asıl belge ya da çeviri hedefi değişmiş. Yeniden çevirin.
- Dil modelinin yanıtında korunması gereken tanımlayıcılar veya kod eksikse yanıt kabul edilmez. Yanıtın içeriğini çıktı panelindeki “Lunascape Docs Çeviri” bölümünden görebilirsiniz.
- “Toplu çeviri her seferinde en çok 1000 belge işler”: kapsamı klasöre göre veya açık seçimle bölün.
<!-- ai-only:end -->

## İlgili konular

- [Belgeleri denetleme](../04-document-tools/check.md)
- [Şablondan belge oluşturma](../04-document-tools/templates.md)
- [İşi bir yapay zekâya devretme](../05-ai/README.md)
