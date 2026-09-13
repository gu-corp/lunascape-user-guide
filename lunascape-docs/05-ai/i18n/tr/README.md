# İşi bir yapay zekâya devretme

Lunascape Docs bir dil modeli çağırmaz. **Bağlam, araçlar ve denetimleri** hazırlar; çeviri, redaksiyon ve yazma işlerini kullandığınız yapay zekâya bırakır.

## Yaklaşım

| Ürünün sağladıkları | İçerik |
|---|---|
| Bağlam | Belge kuralları (çevirilerin bulunduğu yer, front matter, belge standardı, sözlük) ve hedef belgenin konumu |
| Çalışma araçları | Çevrilmemiş ve güncelliğini yitirmiş çevirilerin defteri, belgeleri okuma ve yazma, şablondan oluşturma |
| Sonraki denetim | docs-lint ile doğrulama, kapsam ve tazelik farkı |

Yönergede belgenin metni yer almaz. Yapay zekâ dosyaları kendisi okur, kendisi yazar ve kendisi doğrular.

## İşi devretme

1. Araç çubuğunda [Belge Araçları] düğmesine basın ve [AI] sekmesini açın.
2. [İş] listesinden devretmek istediğiniz işi seçin.
3. Gerekli alanları (hedef dil, konu) doldurun.
4. [Bu işi devret] düğmesine basın.
   Bir VS Code terminali açılır ve seçtiğiniz yapay zekâ yönergeyi alıp çalışmaya başlar.

> **İpucu**
>
> Claude Code oturumuna çalışma araçları (`lunascape-docs` MCP sunucusu) eşlik eder. Oturum, çevrilmemiş ve güncelliğini yitirmiş belgelerin listesini almayı, docs-lint çalıştırmayı ve çeviri sonrası tazeliği kaydetmeyi kendisi yapabilir.

## Sonucu inceleme

| Sağlayıcı türü | Sonucun ulaştığı yer |
|---|---|
| Oturum türü (Claude Code, Codex) | Doğrudan çalışma ağacına yazar. **Git farkında inceleyin** |
| API türü (VS Code dil modelleri, Anthropic, OpenAI uyumlu) | Her seferinde tek bir belge için öneri döndürür. [Farkı aç] ile inceleyin, [Kaydet] ile yazın |

### API türü önerileri inceleme

API türüyle çalıştırdığınızda [AI] sekmesine bir öneri gelir.

1. [Farkı aç] düğmesine basın ve mevcut içerikle farkını inceleyin.
2. Uygunsa [Kaydet] düğmesine basın. Çeviri için tazelik de kaydedilir. Vazgeçmek için [At] düğmesine basın.
   Üretimi yarıda bırakmak için [Durdur] düğmesine basın.

> **Not**
>
> - Lunascape Docs hiçbir zaman Git'te hazırlama veya işleme yapmaz. Değişiklikleri mutlaka farkta inceleyin.
> - Güvenilmeyen bir çalışma alanında ve belge kökü dışındaki geçici klasör görünümünde iş devredilemez.

## İlgili konular

- [Devredilebilecek işler](tasks.md)
- [AI ayarları](settings.md)
- [Defter ve kayıtlar](ledger.md)
