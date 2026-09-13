# Belge düzenleme

Belgeleri doğrudan görüntüleyicinin içinde düzenleyebilirsiniz. Düzenleme ekranında, gördüğünüz gibi düzenlediğiniz "görsel görünüm" ile "Markdown kaynak görünümü" bulunur; tek bir düğmeyle bunlar arasında geçiş yapılır.

## Düzenlemeye başlama

Aşağıdakilerden birine basın. Hepsi aynı düzenleme ekranını açar.

- Belgenin sağ alt köşesindeki [Düzenle]
- Belgenin sağ üst köşesindeki [⋯] (diğer işlemler) → [Düzenle]
- INDEX öğe menüsü → [Düzenle]

## Düzenleme

1. Metni doğrudan düzenleyin.
   Düzenleme ekranının üst kısmındaki araç çubuğunda paragraf biçimi (gövde metni, başlık 1–4, alıntı, kod), [Kalın], [İtalik], [Madde işaretli liste], [Numaralı liste], [Bağlantı], [Tablo ekle], [Görsel boyutu], [Geri al] ve [Yinele] kullanılabilir.
2. Markdown kaynağını doğrudan düzenlemek istediğinizde [Markdown] düğmesine basın.
   Yeniden bastığınızda görsel görünüme dönersiniz. En son kullandığınız görünüm hatırlanır ve [Düzenle] düğmesine bir sonraki basışınızda geri yüklenir.
3. [Kaydet] düğmesine basın.
   Markdown dosyasına yazılır ve görüntüleme ekranına dönülür. Vazgeçmek için [İptal] düğmesine basın.

> **Not**
>
> - Kaydetme yalnızca dosyaya yazar. Git'te hazırlama (staging) veya işleme (commit) otomatik olarak yapılmaz.
> - Matematik ile Mermaid, TikZ, Vega-Lite gibi diyagramlar görsel görünümde işlenmiş hâlleriyle gösterilir. İçeriklerini değiştirmek için [Markdown] görünümüne geçin.
> - MDX'e özgü sözdizimi (bileşenler, `import` vb.) içeren belgeler, bu sözdizimini korumak için yalnızca Markdown görünümünde düzenlenir.
> - Front matter (en üstte `---` satırları arasında kalan ayarlar), görsel görünümde düzenleseniz de korunur.

> **İpucu**
>
> - [VS Code'da aç] düğmesine bastığınızda dosya normal metin düzenleyicisinde açılır. Metin düzenleyicisinde kaydettiğinizde görüntüleyicideki görünüm de otomatik olarak güncellenir.
> - [Düzenle] düğmesini göstermek istemediğinizde [Görünüm ayarları] içindeki [Düzenleme düğmesi] seçeneğini kapatın. Projenin tamamında gizlemek için `lunascape-docs.json` dosyasındaki `editor.showEditButton` değerini `false` yapın.
> - İlk açılan görünümün (görsel/Markdown) varsayılanını `lunascapeDocEditor.editor.defaultMode` ayarıyla veya `lunascape-docs.json` dosyasındaki `editor.defaultMode` ile değiştirebilirsiniz.

## İlgili konular

- [Belge ve klasör oluşturma ve düzenleme](organize.md)
- [Görsel boyutunu ayarlama](images.md)
- [Matematik yazma](math.md)
- [Diyagram ve grafik yazma](diagrams.md)
