# Güvenlik ve yazma sınırları

Lunascape Docs'un belgelerinizi ve cihazınızı korumak için koyduğu sınırlar.

## Görüntüleme

- Markdown'dan üretilen HTML ve diyagramlardan üretilen SVG, görüntülenmeden önce DOMPurify 3.4.14 ile temizlenir.
- MDX içindeki gelişigüzel betikler çalıştırılmaz.
- KaTeX, `trust: false`, `maxSize: 50` ve `maxExpand: 1000` ile çalışır; ne dış HTML'e ne de gelişigüzel komutlara güvenir.
- Markmap, WaveDrom, Svgbob, Vega-Lite ve Penrose çizim kitaplıkları, yalnızca ilgili blok bulunduğunda, sabitlenmiş sürümlerle cihaz içinde yüklenir. Dış kaynaklara başvurulmasına, ham HTML'e ve çalıştırılabilir gösterimlere izin verilmez; üretilen SVG'den betikler, dış görüntüler, `link`, `style` ve `foreignObject` çıkarılır.
- TikZ çizimi, ana sistemdeki LaTeX'i başlatmaz. Bellek içi dosya sistemine sahip bir WebAssembly TeX işçisinde sırayla çalışır; girdi, kuyruk, bellek, çalışma süresi (15 saniye) ve SVG çıktısı sınırlıdır, dosya G/Ç komutları reddedilir.

## Belgelere ve dosyalara erişim

- Belge bağlantıları ve dosya işlemleri belge kökünün dışına çıkamaz.
- INDEX üzerinden oluşturma, yeniden adlandırma, taşıma ve silme işlemleri uygulanmadan önce uzantı tarafında yeniden doğrulanır: belge kökü, INDEX sürümü, asıl belgenin yolu, hedefin türü, sembolik bağlantı sınırları ve kaydedilmemiş belgeler. Eski bir menüden veya başka bir belge kökünden gelen işlem istekleri uygulanmaz.
- Bir belge düzenlenirken veya başka bir INDEX işlemi uygulanırken INDEX değiştirme işlemleri devre dışı bırakılır.
- Şablondan oluşturma işlemi, önizlemeden sonra çalışma alanının güvenilirliğini, belge kökünün gerçekliğini, INDEX sürümünü, Standard Pack'i ve üretilen içeriği, kayıt yerini ve sembolik bağlantı sınırlarını yeniden doğrular. Var olan bir dosyanın üzerine yazmaz; önizlemeden farklı bir içerik veya 4 MiB'ı aşan bir açılım sonucu oluşturmaz.
- Ayar dosyasının kaydedilmesinde, kaydetmeden hemen önce sürüm denetlenir ve dışarıdan bir değişiklik saptanırsa işlem durdurulur.

## Dışarıya gönderim

- Belgeler; görüntüleme, düzenleme veya denetim için dışarıya gönderilmez. Belge denetimleri cihaz içinde, belirlenimci biçimde çalışır.
- Yalnızca çeviri (bu sayfanın çevirisi, toplu çeviri), gönderim hedefini ve kapsamını önceden gösterir ve yalnızca açıkça onaylandığında belgeleri bir dil modeline gönderir. <!-- ai-only -->
- Çeviri önerileri fark olarak sunulur; asıl belgenin ve çeviri hedefinin sürümleri yeniden doğrulanır ve öneri yalnızca bir kişi açıkça kaydettiğinde uygulanır. <!-- ai-only -->
- AI aracılarına yönelik şartname aracı; belge metnini, çalışma alanı adlarını ve yerel yolları döndürmez. <!-- ai-only -->

## Git

- Kaydetme yalnızca dosyaya yazar. Hiçbir özellik Git'te otomatik olarak hazırlama ya da işleme yapmaz.
- `_meta.json` gibi var olan dosyalar sessizce silinmez veya değiştirilmez. Sahipsiz kalan çeviri sürümleri de otomatik olarak silinmez veya taşınmaz.

## İlgili konular

- [Başlıca şartnameler](README.md)
- [AI'dan kullanım](ai-agents.md)
