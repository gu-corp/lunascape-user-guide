# Kayıt defteri ve kayıtlar

[AI] sekmesinin üst kısmındaki kayıt defteri, desteklenen her dilin çeviri durumunu gösterir. AI kullanmadan da neyin eksik olduğunu görebilirsiniz.

| Gösterim | Anlamı |
|---|---|
| Çevrilmemiş | Henüz çevirisi olmayan belge sayısı |
| Güncelliğini yitirmiş | Çevirisi olan, ancak kayıt anına göre asıl belgesi daha yeni olan belge sayısı |
| Çevrildi | Asıl belgesini izleyen çeviri sayısı |

Kayıt defteri, belge kökü taranarak hesaplanır. Ne AI ne de bir dil modeli devreye girer.

## Çeviri kayıtlarını güncelleme

"Güncelliğini yitirmiş" durumunu belirleyebilmek için, çevirinin yapıldığı andaki asıl belgenin ve çevirinin kaydedilmiş olması gerekir. Oturum tabanlı AI dosyaları doğrudan yazdığından, kayıt otomatik olarak oluşturulmaz.

1. Çeviri bittiğinde ve içeriği gözden geçirdiğinizde [Çeviri kayıtlarını güncelle] düğmesine basın.
2. Kaydı bulunmayan çeviriler, geçerli asıl belgeye karşılık gelecek şekilde kaydedilir.

Claude Code oturumları ve API tabanlı kaydetme, kaydı otomatik olarak oluşturur (oturuma `record_translation_freshness` MCP aracını kullanması söylenir). Bu düğme, çeviriyi Codex ya da VS Code sohbetiyle yaptığınızda gerekir.

Bundan sonra asıl belgeyi değiştirdiğinizde, o belgenin çevirisi "Güncelliğini yitirmiş" olarak görünür.

> **Not**
>
> - Kaydı zaten bulunan çevirilerin üzerine yazılmaz. Böylece "Güncelliğini yitirmiş" durumu silinmez.
> - Kayıtlar `.lunascape-docs/translation-freshness.json` dosyasında saklanır. Yalnızca göreli yollar, dil, içerik özeti ve tarih-saat kaydedilir; belge metni saklanmaz.

## İlgili konular

- [Devredilebilecek işler](tasks.md)
- [Başka bir dilde okuma](../02-reading/languages.md)
