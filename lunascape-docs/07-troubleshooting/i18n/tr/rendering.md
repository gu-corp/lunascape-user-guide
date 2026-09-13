# Diyagramlar, matematik veya görseller görüntülenmiyor

## TikZ diyagramı katlanmış kaynak olarak görünüyor

- Dağıtılan uzantıda TikZ çizim motoru yer almaz. Bu, beklenen görünümdür.
- Geliştirme ve değerlendirme amacıyla, güvenilen bir çalışma alanının kök dizinine `node-tikzjax` 1.0.5 sürümünü kurun ve `lunascapeDocEditor.tikz.runtime` ayarını `workspace` yapın.
- Web tarayıcı sürümünde TikZ çizilmez.

## Matematik düz metin olarak görünüyor

- Ayraçları denetleyin: satır içi için `$...$` veya `\(...\)`, bağımsız matematik için `$$...$$` veya `\[...\]`.
- Satır içi kodun veya kod bloğunun içindeki `$` matematik sayılmaz.
- `$5 and $10` gibi para birimini andıran yazımlar matematik olarak işlenmez.
- Çok büyük matematik ifadeleri veya çok sayıda makro açılımı içeren ifadeler, sınırları (`maxSize: 50`, `maxExpand: 1000`) aştığında çizilmez. İfadeyi bölün.

## Diyagram için "çizilemiyor" uyarısı çıkıyor

- Mermaid, Vega-Lite, WaveDrom ve benzerlerinin hata iletisi söz dizimi sorununu gösterir. Düzenleme ekranında [Markdown] ile kaynağı denetleyin.
- Vega-Lite: veriyi `data.values` veya `datasets` içine gömün. Dış URL'lerden gelen veriler ve görsel işaretleri kullanılamaz.
- WaveDrom: katı JSON yazın. JavaScript biçimi (tırnaksız anahtarlar vb.) kullanılamaz.
- Penrose: yalnızca en başta `@preset set-theory` ve izin verilen ifadeleri (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`) kullanın.
- "Üretilen SVG güvenli olmayan başvurular içeriyor" / "Üretilen SVG sınırı aşıyor": dış kaynaklara başvuran veya çok büyük olan diyagramlar görüntülenmez. İçeriği azaltın ya da başvuruları kaldırın.

## Görsel görüntülenmiyor

- Görsel yollarını belgeye göre göreli olarak belirtin. Belge kökünün dışındaki görseller görüntülenmez.
- `<img>` öğesinin `width` değeri yalnızca sayı alır (`width="360"`).

## Dışa aktarılan web sitesinde diyagramlar görünmüyor

TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob ve Penrose çizim kitaplıkları görüntüleme sırasında yüklenir. Dışa aktarılan siteyle birlikte `vendor/` klasörünü de yerleştirin.

## İlgili konular

- [Matematik yazma](../03-editing/math.md)
- [Diyagram ve grafik yazma](../03-editing/diagrams.md)
- [Görsel boyutunu ayarlama](../03-editing/images.md)
