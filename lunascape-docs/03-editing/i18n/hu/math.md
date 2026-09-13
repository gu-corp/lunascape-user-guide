# Képletek írása

A képleteket TeX jelöléssel írjuk, és a KaTeX jeleníti meg a készüléken. Hálózatot nem használ.

## Jelölés

| Fajta | Határolójelek | Példa |
|---|---|---|
| Sorközi képlet (mondaton belül) | `$...$` vagy `\(...\)` | `A tömeg és az energia kapcsolatát az $E = mc^2$ fejezi ki.` |
| Kiemelt képlet (önálló sorban) | `$$...$$` vagy `\[...\]` | Lásd alább |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- A határolójelek köré nem kell szóköz. A közvetlenül japán szöveg mellé írt képletet, például `値は$V=-H$である`, is felismeri.
- A sorközi kódban vagy kódblokkban lévő `$` nem képletként, hanem betű szerint jelenik meg.
- A pénzösszegre emlékeztető írásmódot, például `$5 and $10`, nem tekinti képletnek.

## Szerkesztés

Vizuális nézetben a képlet megjelenített alakban látszik. A tartalom módosításához a szerkesztőben nyomja meg a [Markdown] gombot, és a forrást szerkessze. A vizuális nézetből mentve a TeX forrás és az eredeti határolójel (`$` vagy `\(`) változatlan marad.

> **Megjegyzés**
>
> - A KaTeX a biztonság érdekében `trust: false` beállítással fut, és korlátozza a méretet (`maxSize: 50`), valamint a makrókifejtések számát (`maxExpand: 1000`). Az ezeket meghaladó képleteket nem jeleníti meg.
> - A meglévő dokumentumokban a `$$...$$` vagy `\[...\]` közé írt `tikzpicture` nem képletként, hanem TikZ ábraként jelenik meg.

## Kapcsolódó témák

- [Ábrák és grafikonok írása](diagrams.md)
- [Az ábra, a képlet vagy a kép nem jelenik meg](../07-troubleshooting/rendering.md)
