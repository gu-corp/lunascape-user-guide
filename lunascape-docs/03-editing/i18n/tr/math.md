# Matematik yazma

Matematik, TeX gösterimiyle yazılır ve KaTeX ile cihazınızda işlenir. Ağ bağlantısı kullanılmaz.

## Gösterim

| Tür | Ayraçlar | Örnek |
|---|---|---|
| Satır içi matematik (cümle içinde) | `$...$` veya `\(...\)` | `Kütle ile enerji arasındaki ilişki $E = mc^2$ ile gösterilir.` |
| Blok matematik (kendi satırında) | `$$...$$` veya `\[...\]` | Aşağıya bakın |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Ayraçların önünde ve arkasında boşluk gerekmez. `値は$V=-H$である` örneğindeki gibi Japonca metne bitişik yazılsa da tanınır.
- Satır içi kodun veya kod bloğunun içindeki `$` matematik sayılmaz, olduğu gibi gösterilir.
- `$5 and $10` gibi para tutarına benzeyen yazımlar matematik olarak işlenmez.

## Düzenleme

Görsel görünümde matematik, işlenmiş hâliyle gösterilir. İçeriği değiştirmek için düzenleme ekranında [Markdown] düğmesine basıp kaynağı düzenleyin. Görsel görünümden kaydettiğinizde TeX kaynağı ve özgün ayraç biçimi (`$` mi `\(` mi) olduğu gibi korunur.

> **Not**
>
> - KaTeX, güvenlik için `trust: false` ile çalışır; boyut (`maxSize: 50`) ve makro genişletme sayısı (`maxExpand: 1000`) için üst sınırlar vardır. Bu sınırları aşan matematik işlenmez.
> - Mevcut bir belgede `$$...$$` veya `\[...\]` içine yazılmış `tikzpicture`, matematik olarak değil TikZ diyagramı olarak tanınır.

## İlgili konular

- [Diyagram ve grafik yazma](diagrams.md)
- [Diyagram, matematik veya görseller görüntülenmiyor](../07-troubleshooting/rendering.md)
