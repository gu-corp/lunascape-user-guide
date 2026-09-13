# Proje yapılandırması

Belge kökünün hemen altındaki `lunascape-docs.json`, ekiple paylaşılan belge kökü ayarlarını tutar. Git ile yönetilir.

## Yapılandırma dosyasını oluşturma veya düzenleme

- Araç çubuğundaki [Belge Araçları] → [Denetim] sekmesi → [Kuralların kaynağı ve belge ayarları] → [Belge ayarlarını düzenle] öğesine basınca dosya VS Code'da açılır. Dosya yoksa, bu sırada başlangıç dosyası oluşturulur.
- `lunascape-docs.json` dosya adına, birlikte gelen JSON Schema otomatik olarak ilişkilendirilir; giriş tamamlama ve her alanın açıklaması gösterilir. `$schema` yazmanız gerekmez.

## Yapılandırma örneği

```json
{
  "id": "product-docs",
  "title": "Ürün belgeleri",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Alanların açıklaması

| Alan | İçerik | Varsayılan |
|---|---|---|
| `id` | Kullanıcıya özel görüntüleme ayarlarının saklandığı anahtardır. Klasör taşınsa bile ayarları korumak için sabit bir kimlik verin | Klasör yolu |
| `title` | Araç çubuğunun sol ucunda ve belge kökü listesinde gösterilen addır. Görüntüleme dili değişse de değişmez | Kökteki README/index başlığı, yoksa klasör adı |
| `indexTitle` | INDEX başlığıdır | `INDEX` |
| `startPage` | İlk açılan belgedir (belge köküne göreli yol) | `README.md` |
| `appearance` | Renk düzenidir: `light` (her zaman açık) veya `auto` (VS Code temasını izler) | `light` |
| `defaultLocale` | Varsayılan dildir (asıl belgenin dili). `ja`, `en`, `zh-Hant` gibi BCP 47 dil etiketiyle belirtilir. Çeviri kaynağı olur | Ayarsız (yalnızca görüntüleme için metinden çıkarsanır) |
| `fallbackLocale` | Ortamının dili desteklenen dillerin hiçbiriyle eşleşmeyen okura ilk gösterilecek dildir. `locales` içinde yer alan bir dili belirtin | Ayarsız (`defaultLocale` kullanılır) |
| `locales` | Desteklenen dillerin listesidir. `defaultLocale` de dahildir. Dil menüsünde görünürler ve çeviri hedefi olurlar | Yalnızca `defaultLocale` |
| `ignoredDirectories` | INDEX, arama ve denetimlerden dışlanan klasör adlarıdır. Belirtildiğinde varsayılanın yerine geçer | `["99-archive"]` |
| `tree` | INDEX'in gösterim varsayılanlarıdır. Kullanıcılar görünüm ayarlarından bunları geçersiz kılabilir | Yukarıdaki örnekteki gibi |
| `editor.defaultMode` | Kullanıcı henüz geçiş yapmadığında kullanılan düzenleme görünümüdür: `visual` veya `source` | `visual` |
| `editor.showEditButton` | Belgenin sağ alt köşesinde [Düzenle] öğesinin gösterilip gösterilmeyeceğidir | `true` |
| `documentStandards.pack` | Belge denetimi ve şablonlar için kullanılan Standard Pack'tir: `builtin:<ad>` veya belge köküne göreli yol | Yok |
| `documentStandards.profile` | Pack'in tanımladığı profil adıdır | Yok |
| `translation.enabled` | Çeviri önerilerini ve toplu çeviriyi etkinleştirir | `true` |
| `translation.contextFiles` | Çeviri sırasında terim ve üslup referansı olarak aktarılan, asıl belgeye ait Markdown dosyalarıdır (belge köküne göreli yol) | `[]` |
| `translation.maxContextCharacters` | Referans belgelerin toplam karakter sayısının üst sınırıdır (en fazla 1048576) | `49152` |
| `description` | Belge kümesini anlatan tek satırlık açıklamadır. Deponun ana sayfasındaki kartlarda gösterilir. `title` gibi, dize veya dile göre bir nesne olarak yazılabilir | Yok |

## Belgelerin depoda nerede olduğunu bildirme

Deponun hemen altına konan `lunascape-docs.json`, o klasörün ayarları yerine bir **depo haritası** tutabilir. Aşağıdaki 3 alandan birini yazınca dosya haritaya dönüşür ve o klasörün kendisi belge kökü olmaz.

| Alan | İçerik | Varsayılan |
|---|---|---|
| `defaultFolder` | Belgelerin hangi klasörde olduğudur (hemen altına göreli yol). Gösterdiği yerde ayar dosyası gerekmez | Yok (`docs` kullanılır) |
| `roots` | Birden çok belge kümesi olduğunda bunların listesidir (hemen altına göreli yol, gösterim sırasıyla). Bu durumda hemen altı ana sayfa olur | Yok |
| `excludes` | Belge kökü keşfinden dışlanacak klasörlerdir (hemen altına göreli yol). `node_modules` gibi varsayılan dışlamalara eklenir | `[]` |
| `home.cards` | Ana sayfanın README'sinin altında belge kümesi kartlarının gösterilip gösterilmeyeceğidir. Bağlantıları README'ye kendiniz yazacaksanız `false` yapın | `true` |

Belge kökü şu sırayla belirlenir. Yukarıdan aşağıya, ilk bulunan kullanılır.

1. Ayar veya komutla bir klasör belirtildiğinde, o klasör
2. Hemen altındaki `lunascape-docs.json` dosyasındaki `defaultFolder` veya `roots` alanının gösterdiği yer
3. `lunascape-docs.json` bulunan klasör (ortak bir üst klasörün altında 2 veya daha fazlası varsa, o üst klasör ana sayfa olur)
4. `docs` klasörü (`lunascapeDocEditor.rootDirectoryNames`)
5. Deponun hemen altının kendisi

> **İpucu**
>
> Hiçbir şey yazmazsanız 4. madde geçerli olur; dolayısıyla tek bir `docs/` içeren sıradan bir depo öncekiyle aynı çalışır. Klasör adını `manual` yapmak istediğinizde yalnızca `defaultFolder` yazın.

### Harita örneği

```json
{
  "title": "Lunascape yardımı",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Ayarların önceliği

Görüntülemeyle ilgili alanlar şu sırayla önceliklidir.

1. Kullanıcının görüntüleme ayarları ([Görünüm ayarları] paneli)
2. VS Code ayarları (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Ürünün varsayılan değerleri

Yalnızca diller (`defaultLocale`, `fallbackLocale`, `locales`) istisnadır; asıl kaynak `lunascape-docs.json` dosyasıdır. Kişisel VS Code ayarlarıyla projenin dilleri geçersiz kılınamaz.

> **Not**
>
> Standard Pack, `docs-lint.config.json` dosyasında `standard` olarak da belirtilebilir. Her ikisinde de bulunursa `docs-lint.config.json` öncelikli olur.

## İlgili konular

- [Denetim kurallarını değiştirme](rules.md)
- [Görüntüleme ayarlarını değiştirme](../02-reading/display-settings.md)
- [VS Code ayarları listesi](../08-reference/settings.md)
