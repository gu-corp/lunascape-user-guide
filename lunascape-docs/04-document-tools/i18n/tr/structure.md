# Belge kökleri ve dosya kuralları

Lunascape Docs'un belgeleri bulup INDEX'i oluştururken izlediği kurallardır. Dosya sisteminin kendisi doğrudan asıl kaynak olduğundan, herhangi bir defter ya da derleme yapılandırmasına gerek yoktur.

## Belge kökü

- En yakın `docs` klasörü ya da içinde `lunascape-docs.json` bulunan klasör belge kökü olur.
- `lunascape-docs.json` yerleştirilirse klasörün adının `docs` olması gerekmez.
- Herhangi bir belge köküne ait olmayan bir Markdown dosyası açıldığında, onun klasörü geçici bir belge kökü olarak gösterilir.

## INDEX'te gösterilen dosyalar

- `.md`, `.markdown` ve `.mdx` dosyaları gösterilir. Front matter ya da gezinme bilgisi olmasa bile yeni dosyalar her zaman görünür.
- `.` ile başlayan klasörler, `node_modules` ve `ignoredDirectories` içinde belirtilen klasörler (varsayılan `99-archive`) gösterilmez.
- `i18n/` altındaki her şey çeviri olarak ele alınır ve INDEX'te ayrıca listelenmez.

## Klasör kapak sayfaları

- Gövde metni olan bir `README.md` (yoksa `index.md`) o klasörün kapak sayfası olur. INDEX'te klasör adına basıldığında kapak sayfası açılır.
- Yalnızca front matter içeren, gövdesi olmayan bir `README.md` "yalnızca yapılandırma tanımlayıcısı" olarak ele alınır ve sayfa olarak gösterilmez. Bir klasöre yalnızca başlık ya da sıralama vermek istediğinizde bunu kullanın.
- Hem `README.md` hem `index.md` bulunduğunda `README.md` önceliklidir.

## Varsayılan dil ve çeviriler

- Varsayılan dildeki belgeler (asıl belge) olduğu yerde kalır.
- Çeviri, belgeyle aynı klasördeki `i18n/<dil>/` içine, aynı dosya adıyla yerleştirilir. Klasör yapısını `i18n/` altında yeniden oluşturmak tanınmaz.
- Çeviri yalnızca bu tek konumdan çözümlenir. Başka bir yere konan aynı adlı çeviri, hiçbir belgenin çevirisi olarak sahiplenmeyen bir yetim dosya olur.

```text
docs/
  lunascape-docs.json
  README.md                  ← kökün kapak sayfası (başlangıç sayfası)
  i18n/en/README.md          ← onun İngilizce çevirisi
  01-product/
    README.md                ← klasörün kapak sayfası
    requirements.md
    i18n/en/README.md        ← yukarıdaki iki belgenin İngilizce çevirileri
    i18n/en/requirements.md
  99-archive/                ← varsayılan olarak INDEX'ten hariç tutulur
```

## `_meta.json` hakkında

Nextra'nın `_meta.json` dosyası gezinme için kullanılmaz. Var olan dosyalar ne değiştirilir ne de silinir. Gelecekte yalnızca açık bir içe/dışa aktarma özelliği bunları işleyecektir.

## İlgili konular

- [Gezinme bilgisini ayarlama](navigation-metadata.md)
- [Proje yapılandırması](project-configuration.md)
- [Belge köklerini değiştirme](../02-reading/roots.md)
