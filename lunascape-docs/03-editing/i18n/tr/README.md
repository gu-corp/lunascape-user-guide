# Belge düzenleme

Belgeler doğrudan görüntüleyicinin içinde düzenlenebilir. Düzenleme ekranında, gördüğünüz şekilde düzenlediğiniz "görsel görünüm" ile "Markdown kaynak görünümü" bulunur; tek bir düğmeyle bunlar arasında geçiş yaparsınız.

## Düzenlemeye başlama

Aşağıdakilerden birine basın. Hepsi aynı düzenleme ekranını açar.

- Belgenin sağ alt köşesindeki [Düzenle]
- Belgenin sağ üst köşesindeki [⋯] (Diğer işlemler) → [Düzenle]
- INDEX öğe menüsü → [Düzenle]

## Düzenleme

1. Metni doğrudan düzenleyin.
   Düzenleme ekranının üst kısmındaki araç çubuğunda paragraf biçimini (gövde, başlık 1–4, alıntı, kod), [Kalın], [İtalik], [Madde işaretli liste], [Numaralı liste], [Bağlantı], [Tablo ekle], [Görsel boyutu], [Geri al] ve [Yinele] öğelerini kullanabilirsiniz.
2. Markdown kaynağını doğrudan düzenlemek istediğinizde [Markdown] öğesine basın.
   Tekrar bastığınızda görsel görünüme dönersiniz. En son kullandığınız görünüm hatırlanır ve bir sonraki sefer [Düzenle] öğesine bastığınızda geri yüklenir.
3. [Kaydet] öğesine basın (Ctrl+S / ⌘S ile de kaydedebilirsiniz).
   Markdown dosyasına yazılır ve görüntüleyici okuma görünümüne döner. Düzenlemeyi bırakıp en son kaydedilen içeriğe dönmek için [Düzenlemeleri iptal et] öğesine basın.

## Her zaman düzenleme ekranından başlama (düzenleme modu)

Araç çubuğundaki [Düzenleme modu] öğesine basıp açtığınızda, her belge açtığınızda düzenleme ekranından başlarsınız. Bir not defteri gibi yazmaya devam ettiğinizde kullanılır.

- Açık olduğu sürece, [Kaydet] öğesine bassanız bile düzenleme ekranı kapanmaz. [Düzenlemeleri iptal et] en son kaydedilen içeriğe döndürür ve düzenleme ekranı açık kalır.
- Tekrar bastığınızda kapanır ve okuma görünümüne dönersiniz. Açık/kapalı durumu her kullanıcı için ayrı hatırlanır.
- Yazılamayan bir belge kökünde (yalnızca okunabilir GitHub kaynağı gibi) görünmez.

## Kaydedilmemiş düzenlemeler

Kaydetmediğiniz düzenlemeler bu cihazda otomatik olarak saklanır. Başka bir belgeye geçseniz de, sekmeyi veya pencereyi kapatsanız da kaybolmazlar.

- Düzenleme ekranındaki [Kaydedilmedi], metnin en son kaydedilen içerikten farklı olduğunu gösterir.
- Aynı belgeyi bir sonraki açışınızda, saklanan düzenlemelerden devam eder ve bunu bildirir. Belgenin kendisi o zamandan beri güncellendiyse bunu da bildirir; [Düzenlemeleri iptal et] ile en güncel içeriğe dönebilirsiniz.
- Saklanan düzenlemeler [Kaydet] veya [Düzenlemeleri iptal et] ile silinir. Kaydedilmedikleri için Git'te veya taslaklar arasında görünmezler.

> **Not**
>
> - Kaydetme yalnızca dosyaya yazma işlemi yapar. Git'te hazırlama (staging) veya işleme (commit) hiçbir zaman otomatik yapılmaz.
> - Matematik ile Mermaid, TikZ ve Vega-Lite gibi diyagramlar, görsel görünümde işlenmiş sonuçları olarak gösterilir. İçeriklerini değiştirmek için [Markdown] öğesine geçin.
> - MDX'e özgü söz dizimi (bileşenler, `import` vb.) içeren belgeler, söz dizimini korumak için yalnızca Markdown görünümünde düzenlenir.
> - Front matter (baştaki `---` satırları arasında yer alan ayarlar), görsel görünümde düzenleseniz de korunur.

> **İpucu**
>
> - [VS Code'da aç] öğesine bastığınızda dosya normal metin düzenleyicisinde açılır. Orada kaydettiğinizde görüntüleyicinin görünümü de otomatik olarak güncellenir.
> - [Düzenle] düğmesini göstermek istemediğinizde, [Görünüm ayarları] içindeki [Düzenleme düğmesi] öğesini kapatın. Projenin tamamında gizlemek için `lunascape-docs.json` dosyasındaki `editor.showEditButton` değerini `false` yapın.
> - İlk açılan görünümün (görsel/Markdown) varsayılanını, `lunascapeDocEditor.editor.defaultMode` ayarı veya `lunascape-docs.json` dosyasındaki `editor.defaultMode` ile değiştirebilirsiniz.

## İlgili konular

- [Belge ve klasör oluşturma ve düzenleme](organize.md)
- [Görsel boyutunu ayarlama](images.md)
- [Matematik yazma](math.md)
- [Diyagram ve grafik yazma](diagrams.md)
