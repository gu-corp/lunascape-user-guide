# Lunascape Docs nedir

Lunascape Docs, bir Git deposundaki Markdown belgelerini olduğu gibi bir "şartname sitesi" olarak kullanmanızı sağlayan bir araçtır. Önceden derleme, belge sunucusu veya özel bir veritabanı gerekmez.

## Yapabilecekleriniz

| Amaç | Başlıca işlevler |
|---|---|
| Okuma | INDEX (içindekiler), metin içi bağlantılar, içerik haritası, geri/ileri, sayfa içi içindekiler, süzerek arama |
| Görüntüleme | Tablolar, kod blokları, görüntülerin otomatik sığdırılması, KaTeX matematik ifadeleri, Mermaid, Vega-Lite, Markmap, WaveDrom ve Svgbob diyagramları, belge yönetim tablolarının katlanmış gösterimi |
| Yazma | Görsel düzenleme ile Markdown kaynak düzenleme arasında geçiş; INDEX üzerinden oluşturma, çoğaltma, yeniden adlandırma ve sıralama |
| Doğrulama | docs-lint ile belge denetimi, Standard Pack temelinde zorunlu belge, bölüm ve terim denetimi, şablondan oluşturma |
| Çeviri | Tek sayfa veya toplu olarak çeviri önerisi oluşturma. Gözden geçirdikten sonra kaydedin <!-- ai-only --> |
| AI'dan kullanma | VS Code aracılarının başvurabileceği, salt okunur şartname aracı <!-- ai-only --> |

## Kullanabileceğiniz ortamlar

| Ortam | Kullanım amacı |
|---|---|
| VS Code uzantısı | Bilgisayarınızdaki deponun görüntülenmesi, düzenlenmesi, denetlenmesi ve çevrilmesi. Bu yardımın odağı budur |
| Web tarayıcı sürümü | GitHub üzerindeki belgelerin (herkese açık veya özel) görüntülenmesi, cihaz içindeki taslaklar, yerel klasörlerin görüntülenmesi |
| Chromium uzantısı | Web tarayıcı sürümünü bir tarayıcı sekmesinde açar |
| Lunascape tarayıcısı | Aynı belge modelini içerecek şekilde planlanmıştır |

## Temel yaklaşım

- **Asıl belge Markdown'dır.** Belgeler, Git ile yönetilen Markdown dosyaları olarak kalır. Lunascape Docs bunları başka bir biçime dönüştürüp saklamaz.
- **Kaydetme işini kullanıcı yapar.** Düzenlediğiniz içerik yalnızca [Kaydet] düğmesine bastığınızda dosyaya yazılır. Git'te hazırlama ve işleme otomatik olarak yapılmaz.
- **Belgeler cihaz içinde işlenir.** Görüntülemek veya düzenlemek için belgeler dışarıya gönderilmez. Yalnızca çeviri sırasında, gönderim yeri ve içeriği önceden gösterilir ve onayınızdan sonra gönderilir.
- **Çeviriler `i18n/<dil>/` altına yerleştirilir.** Varsayılan dildeki belgeler bulundukları yerde kalır; çeviriler aynı göreli yolla `i18n/en/` gibi klasörlere yerleştirilir.
- **AI yalnızca öneri sunar.** Çeviri önerileri, farkları gözden geçirdikten sonra kaydedilir. Belgeler sessizce değiştirilmez. <!-- ai-only -->

## İlgili konular

- [Ekran bölümlerinin adları ve işlevleri](screen.md)
- [Uzantıyı yükleme](install.md)
- [Temel işlemler](../02-reading/README.md)
