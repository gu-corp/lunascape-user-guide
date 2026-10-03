# Lunascape Docs nedir

Lunascape Docs, bir Git deposuna koyduğunuz Markdown belgelerini olduğu gibi bir “şartname sitesi” olarak kullanmanızı sağlayan bir araçtır. Önceden derleme, belge sunucusu veya özel bir veritabanı gerekmez.

## Neler yapabilirsiniz

| Amaç | Başlıca özellikler |
|---|---|
| Okuma | INDEX (içindekiler), metin içi bağlantılar, gezinti yolu, geri/ileri, sayfa içi içindekiler, filtreli arama |
| Görüntüleme | Tablolar, kod blokları, görsellerin otomatik sığdırılması, KaTeX matematik, Mermaid/Vega-Lite/Markmap/WaveDrom/Svgbob diyagramları, belge yönetim tablolarının daraltılmış gösterimi |
| Yazma | Görsel düzenleme ile Markdown kaynak düzenleme arasında geçiş; INDEX'ten oluşturma, çoğaltma, yeniden adlandırma ve sıralama |
| Denetleme | docs-lint ile belge denetimi, Standard Pack'e göre zorunlu belge, bölüm ve terimlerin denetimi, şablondan oluşturma |
| Çeviri | Sayfa sayfa veya toplu olarak çeviri önerisi oluşturma; gözden geçirdikten sonra kaydetme <!-- ai-only --> |
| Yapay zekâ üzerinden kullanma | VS Code ajanlarının başvurabildiği, salt okunur şartname aracı <!-- ai-only --> |

## Kullanılabileceği ortamlar

| Ortam | Kullanım amacı |
|---|---|
| VS Code uzantısı | Yerel depoyu görüntüleme, düzenleme, denetleme ve çevirme. Bu yardımın odak noktasıdır |
| Web tarayıcı sürümü | GitHub'daki belgeleri (herkese açık ve özel) görüntüleme, cihazdaki taslaklar, yerel klasörleri görüntüleme |
| Chromium uzantısı | Web tarayıcı sürümünü bir tarayıcı sekmesinde açar |

## Temel ilkeler

- **Asıl belge Markdown'dır.** Belgeler, Git ile yönetilen Markdown dosyaları olarak kalır. Lunascape Docs bunları başka bir biçime dönüştürüp saklamaz.
- **Kaydetmeyi siz yaparsınız.** Düzenlemeler yalnızca [Kaydet] düğmesine bastığınızda dosyaya yazılır. Git'te hazırlama alanına ekleme ve commit işlemleri otomatik olarak yapılmaz.
- **Belgeler cihazınızda işlenir.** Görüntüleme veya düzenleme için belgeler dışarıya gönderilmez. Yalnızca çeviri sırasında, gönderim hedefi ve içerik önceden gösterilir; onayınızdan sonra gönderilir.
- **Çeviriler `i18n/<言語>/` altına konur.** Varsayılan dildeki belgeler oldukları yerde kalır; çeviriler aynı göreli yolla `i18n/en/` gibi klasörlere konur.
- **Yapay zekâ yalnızca öneride bulunur.** Çeviri önerileri, farkı inceledikten sonra kaydedilir. Belgeler habersizce yeniden yazılmaz. <!-- ai-only -->

## İlgili konular

- [Ekranın bölümleri ve işlevleri](screen.md)
- [Uzantıyı yükleme](install.md)
- [Temel işlemler](../02-reading/README.md)
