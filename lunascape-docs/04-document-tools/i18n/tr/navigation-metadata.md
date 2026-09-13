# Gezinme bilgilerini ayarlama

INDEX içinde gösterilen ad ve sıra, her belgenin YAML front matter bölümüne yazılır. Bu bilgi olmasa da belgeler gösterilir; başlık (H1) ve dosya adı sıralaması kullanılır.

## Belgenin adı ve sırası

Belgenin en başına şunu yazın.

```yaml
---
navigation:
  title: Başlarken
  order: 200
---
```

| Alan | Anlamı |
|---|---|
| `navigation.title` | INDEX içinde gösterilen addır. Atlandığında H1, o da yoksa dosya adı kullanılır |
| `navigation.order` | Sıralamayı belirleyen bir tam sayıdır; küçükten büyüğe sıralanır. Atlandığında kararlı bir varsayılan sıra (dosya adına göre) geçerli olur |

> **İpucu**
>
> - `order` değerlerini 100, 200, 300 gibi 100'er 100'er verin; böylece sonradan araya 150 gibi bir değer ekleyebilirsiniz.
> - Eksik, geçersiz veya yinelenen `order` değerleri bir belgeyi asla gizlemez.
> - INDEX içinde yeniden sıraladığınızda `navigation.order` sizin için yazılır; elle yazmanıza gerek yoktur.

## Klasörün adı ve sırası

Bir klasörün adı ve sırası, o klasörün `README.md` dosyasının (README yoksa `index.md`) front matter bölümüne aittir. Kapak sayfasının gövde içeriği olması gerekmez.

```yaml
---
navigation:
  title: Ürün planlama
  order: 100
---
```

Kapak sayfası olmayan bir klasör, klasör adını ve varsayılan sırayı kullanır. INDEX içinde bir başlık değişikliği veya yeniden sıralama bunu gerektirdiğinde, yalnızca front matter içeren bir `README.md` oluşturulur. Yalnızca görüntülemek asla bir dosya oluşturmaz.

## Çevirilerde durum

- Sıra ve klasörün rolü (kapak sayfası mı yoksa yalnızca yapılandırma mı) yalnızca varsayılan dildeki belge tarafından belirlenir.
- Bir çeviri yalnızca `navigation.title` değerini geçersiz kılabilir. Asıl belgenin gövde içeriği olduğunda, çevirinin H1 başlığı da ad olarak kullanılır.
- Tek başına bir çeviri asla bir sayfa eklemez.

## Alt öğelerin sıralanması ve daraltılması

Bir klasörün kapak sayfasındaki `navigation.children.sort` ve `navigation.children.defaultCollapsed`, doğrudan alt öğelerinin nasıl sıralanacağını ve başlangıçta daraltılmış olup olmayacağını denetlemek için tanımlanmıştır. Bunların VS Code içinde okunması ve düzenlenmesi ilerideki sürümlerde desteklenecektir.

## İlgili konular

- [Belge sıralamasını değiştirme](../03-editing/reorder.md)
- [Belge kökleri ve dosya kuralları](structure.md)
