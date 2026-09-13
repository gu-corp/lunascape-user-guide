# Belge kökünü değiştirme

Belge kökü, bir belge kümesinin en üst klasörüdür. INDEX, filtreleme, denetim ve çeviri işlemlerinin tümü belge kökü birimiyle çalışır.

## Belge kökü nasıl bulunur

Lunascape Docs, açılan Markdown dosyasından üst klasörlere doğru ilerler ve aşağıdakilerden birine uyan en yakın klasörü belge kökü olarak kullanır.

- `lunascape-docs.json` dosyasını içeren klasör (klasör adı önemli değildir)
- `docs` adlı klasör (`lunascapeDocEditor.rootDirectoryNames` ayarıyla başka adlar ekleyebilirsiniz)

"Lunascape Docs: Şartname görüntüleyicisini aç" komutunu çalıştırdığınızda, `lunascapeDocEditor.root` ayarındaki (varsayılan `docs`) belge kökü açılır.

## Başka bir belge köküne geçme

Çalışma alanında birden çok belge kökü olduğunda, araç çubuğunun en solundaki belge kökü adı bir açılır listeye dönüşür.

1. Araç çubuğunun en solundaki belge kökü adına basın.
2. Listeden bir belge kökü seçin.
   Seçtiğiniz belge kökünün başlangıç sayfası görüntülenir ve INDEX değişir.

> **İpucu**
>
> Listede görünen adlar şu sırayla belirlenir. Görüntüleme dilini değiştirseniz de bu adlar değişmez.
>
> 1. `lunascape-docs.json` dosyasındaki `title`
> 2. Kökteki `README.md` dosyasının `navigation.title` değeri, yoksa H1 başlığı
> 3. Kökteki `index.md` dosyasının `navigation.title` değeri, yoksa H1 başlığı
> 4. Klasör adı (standart `docs` klasöründe, üst klasörünün adı)

## Belge köküne ait olmayan bir Markdown dosyasını açma

Bir belge köküne dahil olmayan bir Markdown dosyasını açtığınızda, dosyanın bulunduğu klasör geçici belge kökü olarak görüntülenir. INDEX panelinde, aynı klasördeki ve altındaki Markdown dosyaları listelenir.

- Araç çubuğundaki [Üst klasöre] düğmesine basarak görüntüleme kapsamını çalışma alanı içindeki üst klasöre genişletebilirsiniz.
- Bu görünümde projenin dil ayarları ve toplu çeviri kullanılamaz. Klasöre bir `lunascape-docs.json` dosyası koyup klasörü belge kökü haline getirdiğinizde kullanılabilir olur.

## Her zaman belirli bir belge kökünü açma

`lunascapeDocEditor.rootMode` ayarını `fixed` yaparsanız, hangi Markdown dosyasını açarsanız açın her zaman `lunascapeDocEditor.root` ayarındaki belge kökü açılır.

## İlgili konular

- [Belge kökleri ve dosya kuralları](../04-document-tools/structure.md)
- [Proje yapılandırması](../04-document-tools/project-configuration.md)
- [VS Code ayarları listesi](../08-reference/settings.md)
