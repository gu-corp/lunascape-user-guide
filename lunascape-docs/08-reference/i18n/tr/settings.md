# VS Code ayarları

VS Code ayarlarında (`⌘,` / `Ctrl+,`) "Lunascape Docs" araması yaparak aşağıdaki maddeleri değiştirebilirsiniz. Bunların tümü kullanıcıya özel ayarlardır ve projenin belgelerine kaydedilmez.

## Belge kökü

| Ayar | Değerler | Varsayılan | İşlevi |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto`, açılan Markdown dosyasına en yakın belge kökünü otomatik seçer; dosya hiçbirine ait değilse üst klasörü geçici olarak açar. `fixed` ise her zaman `root` içindeki belge kökünü açar |
| `lunascapeDocEditor.rootDirectoryNames` | Dizi (metin) | `["docs"]` | `auto` modunda belge kökü olarak otomatik bulunacak klasör adlarıdır. İçinde `lunascape-docs.json` bulunan klasör, adı ne olursa olsun bulunur. Deponun kök dizinindeki `lunascape-docs.json` içinde `defaultFolder` veya `roots` varsa onlar önceliklidir |
| `lunascapeDocEditor.root` | Yol | `docs` | `fixed` modunda veya komutla açarken kullanılan, çalışma alanına göreli belge köküdür |
| `lunascapeDocEditor.startPage` | Yol | `README.md` | Belge köküne göreli başlangıç sayfasıdır |
| `lunascapeDocEditor.title` | Metin | `Lunascape Docs` | Belge sekmesinin başlığını geçersiz kılar. Belge kökü seçicisindeki adı etkilemez |
| `lunascapeDocEditor.ignoredDirectories` | Dizi (metin) | `["99-archive"]` | INDEX dışında bırakılacak klasör adlarıdır |

## Görünüm

| Ayar | Değerler | Varsayılan | İşlevi |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` beyaz arka plan kullanır, `auto` ise VS Code'un renk düzenini izler |
| `lunascapeDocEditor.locale` | Dil etiketi | Yok | Mevcut olduğunda öncelikli gösterilecek kişisel belge dilinizdir. Projenin asıl belge dilini değiştirmez |
| `lunascapeDocEditor.documentMetadata.compact` | Mantıksal | `true` | H1 başlığının hemen altındaki belge yönetim tablosunu "Belge bilgileri" satırına katlar |
| `lunascapeDocEditor.tree.showFileNames` | Mantıksal | `false` | INDEX içinde belge adı yerine dosya adını gösterir |
| `lunascapeDocEditor.tree.showDocumentIcons` | Mantıksal | `false` | INDEX içinde belge simgelerini gösterir |
| `lunascapeDocEditor.tree.showFolderIcons` | Mantıksal | `false` | INDEX içinde klasör simgelerini gösterir |
| `lunascapeDocEditor.tree.showItemCounts` | Mantıksal | `false` | INDEX içinde her klasörün doğrudan altındaki öğe sayısını gösterir |
| `lunascapeDocEditor.tree.showGuides` | Mantıksal | `true` | INDEX içinde hiyerarşi kılavuz çizgilerini gösterir |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | INDEX satır aralığıdır |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Mantıksal | `true` | Yalnızca bir belge olduğunda INDEX'i ilk seferde kapatır |

## Düzenleme

| Ayar | Değerler | Varsayılan | İşlevi |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Siz değiştirmediğiniz sürece kullanılan düzenleme görünümüdür. En son kullanılan görünüm önceliklidir |
| `lunascapeDocEditor.editor.showEditButton` | Mantıksal | `true` | Belgenin sağ alt köşesinde [Düzenle] düğmesini gösterir |

## Diyagramlar

| Ayar | Değerler | Varsayılan | İşlevi |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | TikZ çizim çalışma ortamıdır. `bundled`, birlikte gelen onaylı çalışma ortamını kullanır (geçerli dağıtım sürümünde bulunmaz); `workspace`, güvenilen çalışma alanının kök dizinindeki `node-tikzjax` 1.0.5 sürümünü kullanır (yalnızca geliştirme ve değerlendirme için); `disabled` ise çizim yapmaz |

## Kullanımdan kaldırılan ayarlar

| Ayar | Bunun yerine kullanın |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `lunascape-docs.json` içindeki `defaultLocale` |
| `lunascapeDocEditor.locales` | `lunascape-docs.json` içindeki `locales` |

Kişisel ayarlarla projenin dilleri geçersiz kılınamaz.

## İlgili konular

- [Görünüm ayarlarını değiştirme](../02-reading/display-settings.md)
- [Proje yapılandırması](../04-document-tools/project-configuration.md)
