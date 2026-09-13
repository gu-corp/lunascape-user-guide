# AI ayarları

Çalışmanızı devredeceğiniz AI'ı ve modeli seçin. VS Code'un hızlı seçim kutusu kullanılmaz; seçim bu ekrandaki açılır listelerden yapılır.

1. [Belge Araçları] → [AI] sekmesi → [AI ayarları…] düğmesine basın.
2. [Sağlayıcı] listesinden bir sağlayıcı seçin.
   Bu ortamda kullanılamayanlar, nedeni belirtilerek seçilemez durumda görünür.
3. [Model] listesinden bir model seçin. Seçenekler sağlayıcıya göre değişir.
4. Ekranı kapatın. Seçim kullanıcı başına kaydedilir ve bir sonraki sefer de kullanılır.

## Sağlayıcılar

| Sağlayıcı | Biçim | Algılama yöntemi |
|---|---|---|
| Claude Code | Oturum tipi | `claude` komutunun bulunması |
| Codex | Oturum tipi | `codex` komutunun bulunması |
| VS Code dil modelleri | API tipi | VS Code Language Model API'ye kayıtlı modeller |
| Anthropic API | API tipi | API anahtarının kaydı |
| OpenAI uyumlu API | API tipi | API anahtarı ve uç noktasının kaydı |

**Oturum tipi** sağlayıcı dosyaları kendisi okuyup yazar, belge denetimini de kendisi çalıştırır. Sonuçlar doğrudan çalışma ağacına yazılır ve Git farkında görülür.

**API tipi** sağlayıcı bir belgelik Markdown döndürür; uzantı farkı gösterdikten sonra kaydeder.

## API anahtarı kaydetme

Anthropic API ve OpenAI uyumlu API, bir API anahtarı kaydedildiğinde kullanılabilir hale gelir.

1. [Sağlayıcı] listesinden kaydı yapacağınız sağlayıcıyı seçin. API anahtarı giriş alanı görünür.
2. [API anahtarı] alanına anahtarı girin. OpenAI uyumlu API için ayrıca [Uç nokta] alanını da girin (örneğin `https://api.openai.com/v1`).
3. [Kaydet] düğmesine basın. "Anahtar kaydedildi" yazısı görünür.

> **Not**
>
> - Anahtarlar VS Code'un SecretStorage alanına kaydedilir ve bir daha gösterilmez. `settings.json` dosyasına veya belgelere de yazılmaz. [Anahtarı sil] ile silebilirsiniz.
> - Model listesi, kaydettiğiniz anahtarla her hizmetten alınır. Liste alınamadığı sürece bilinen bir liste gösterilir.
> - API tipinde yalnızca "Bu sayfayı çevir" ve "Bu sayfayı düzelt" işleri çalıştırılabilir. Birden çok belgeyi dolaşma ve belge oluşturma işlerini oturum tipiyle çalıştırın.

> **İpucu**
>
> Hiçbir sağlayıcı bulunamıyorsa Claude Code ya da Codex'i kurun veya bir API anahtarı kaydedin. [AI ayarları…] ekranını yeniden açtığınızda algılanır.

## İlgili konular

- [AI'a iş devretme](README.md)
- [VS Code ayarları listesi](../08-reference/settings.md)
