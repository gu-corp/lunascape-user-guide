# Psaní vzorců

Vzorce se píší v zápisu TeX a vykreslují se přímo ve vašem zařízení pomocí KaTeX. Síť se nepoužívá.

## Zápis

| Druh | Oddělovače | Příklad |
|---|---|---|
| Vzorec v textu (uvnitř věty) | `$...$` nebo `\(...\)` | `Hmotnost a energii spojuje vztah $E = mc^2$.` |
| Vzorec na samostatném řádku | `$$...$$` nebo `\[...\]` | Viz níže |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Kolem oddělovačů nejsou potřeba mezery. Vzorec bezprostředně navazující na japonský text, například `値は$V=-H$である`, se rozpozná.
- Znak `$` uvnitř kódu v textu nebo uvnitř bloku kódu se zobrazí doslovně.
- Zápis vypadající jako částka, například `$5 and $10`, se za vzorec nepovažuje.

## Úpravy

Ve vizuálním zobrazení se vzorce ukazují vykreslené. Chcete-li je změnit, stiskněte v editoru [Markdown] a upravte zdrojový text. Uložení z vizuálního zobrazení zachová zdrojový text TeX i původní podobu oddělovačů (`$`, nebo `\(`) beze změny.

> **Poznámka**
>
> - Z bezpečnostních důvodů běží KaTeX s nastavením `trust: false` a má omezenou velikost (`maxSize: 50`) i počet rozvinutí maker (`maxExpand: 1000`). Vzorce, které tyto meze překročí, se nevykreslí.
> - Zápis `tikzpicture` uvnitř `$$...$$` nebo `\[...\]` ve stávajícím dokumentu se rozpozná jako obrázek TikZ, nikoli jako vzorec.

## Související témata

- [Psaní diagramů a grafů](diagrams.md)
- [Diagramy, vzorce nebo obrázky se nevykreslují](../07-troubleshooting/rendering.md)
