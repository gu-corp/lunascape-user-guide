# Pisanje matematičkih izraza

Matematički izrazi pišu se u TeX zapisu i iscrtavaju se na vašem uređaju pomoću KaTeX-a. Mreža se ne koristi.

## Zapis

| Vrsta | Graničnici | Primjer |
|---|---|---|
| Matematički izraz u retku (unutar rečenice) | `$...$` ili `\(...\)` | `Masa i energija povezane su izrazom $E = mc^2$.` |
| Istaknuti izraz (u vlastitom retku) | `$$...$$` ili `\[...\]` | Vidi u nastavku |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Razmaci oko graničnika nisu potrebni. Izraz koji neposredno graniči s japanskim tekstom, primjerice `値は$V=-H$である`, prepoznaje se.
- Znak `$` unutar koda u retku ili unutar bloka koda ostaje doslovan tekst.
- Zapisi nalik iznosima, primjerice `$5 and $10`, ne smatraju se matematičkim izrazom.

## Uređivanje

U vizualnom prikazu matematički izraz prikazuje se iscrtan. Da biste ga izmijenili, u uređivaču pritisnite [Markdown] i uredite izvorni zapis. Spremanje iz vizualnog prikaza ostavlja TeX izvor i izvorni oblik graničnika (`$` ili `\(`) nepromijenjenima.

> **Napomena**
>
> - Radi sigurnosti KaTeX radi uz `trust: false` te ograničava veličinu (`maxSize: 50`) i broj proširenja makronaredbi (`maxExpand: 1000`). Izrazi koji prelaze te granice ne iscrtavaju se.
> - `tikzpicture` napisan unutar `$$...$$` ili `\[...\]` u postojećem dokumentu prepoznaje se kao TikZ dijagram, a ne kao matematički izraz.

## Povezane teme

- [Pisanje dijagrama i grafikona](diagrams.md)
- [Dijagrami, matematički izrazi ili slike ne prikazuju se](../07-troubleshooting/rendering.md)
