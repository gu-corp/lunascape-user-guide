# Devredilebilir işler

[AI] sekmesindeki [İş] alanından seçilir. Her iş için devredilen yönerge ve ardından yapılan denetim değişir.

| İş | İçerik | Gerekenler | API türü |
|---|---|---|---|
| Bu sayfayı çevir | Görüntülenen belgeyi, seçilen dile çevirir | Hedef belgenin açık olması, hedef dil | ○ |
| Çevrilmemiş olanları topluca çevir | Seçilen dilde çevrilmemiş ve güncelliğini yitirmiş belgeleri sırayla çevirir | Hedef dil | Yalnızca oturum türü |
| Bu sayfayı düzelt | Terimleri, üslubu ve belge standardının istediği bölümlemeyi denetler ve düzeltir | Hedef belgenin açık olması | ○ |
| Yeni belge oluştur | Belge standardına ve şablonlara uyarak yeni bir belge oluşturur | Konu (isteğe bağlı) | Yalnızca oturum türü |

## Yönergenin içerdikleri

| No. | İçerik |
|---|---|
| 1 | Belge kökünün konumu. Bunun dışında değişiklik yapılmaması söylenir |
| 2 | Varsayılan dil (asıl belge) ve çeviri sürümlerinin yeri (belgeyle aynı klasördeki `i18n/<dil>/`) |
| 3 | `navigation.order` alanının yalnızca asıl belgeye ait olduğu, çeviri sürümünün yalnızca `navigation.title` alanını değiştirebileceği |
| 4 | Gereksinim kimlikleri, bağlantılar, kod, Mermaid, TeX ve front matter yapısının değiştirilmemesi |
| 5 | Belge standardı ve terim sözlüğü (`docs-lint.config.json` içindeki `terminology`) |
| 6 | Bitince belge denetimini çalıştırması, değiştirdiği dosyaları bildirmesi ve Git işlemi yapmaması |

> **İpucu**
>
> "Çevrilmemiş olanları topluca çevir" işinin hedefleri defterden alınır ve her çalıştırmada en çok 200 belgedir. Daha fazlası varsa işi yineleyin.

## İlgili konular

- [AI'ya iş devretme](README.md)
- [Defter ve kayıtlar](ledger.md)
