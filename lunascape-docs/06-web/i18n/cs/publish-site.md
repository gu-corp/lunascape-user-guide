# Publikování vlastních dokumentů na webu

Dokumenty z vlastního úložiště můžete publikovat jako web na GitHub Pages nebo na libovolném statickém hostingu. Existují dva způsoby. Tento postup je určen vývojářům, kteří dokážou naklonovat úložiště Lunascape Docs a používat `npm`.

## Způsob 1: umístit dva soubory prohlížeče

Nasadíte pouze prohlížeč (`index.html` a `lsdoc.js`) a dokumenty se načítají z GitHubu. Samotné dokumenty nejsou součástí webu, takže je tento způsob bezpečný i pro neveřejná úložiště (čtenáři se přihlásí přes GitHub).

1. V úložišti Lunascape Docs spusťte následující příkaz.

   ```sh
   npm run build:viewer
   ```

   Ve složce `dist/viewer/` se vytvoří soubory `index.html` a `lsdoc.js`.
2. Oba soubory umístěte do složky `docs/` v úložišti, které chcete publikovat.
3. Zapněte GitHub Pages.

Kořen dokumentace, který se zobrazí, se určuje v tomto pořadí.

1. Nastavení `source` uvnitř souboru `index.html`
2. Položka `repository` v souboru `lunascape-docs.json` ve stejné složce
3. Odhad podle adresy URL `*.github.io` a uspořádání větví

## Způsob 2: exportovat statický web včetně dokumentů

Prohlížeč exportujete společně se soubory dokumentů a výsledek hostujete tak, jak je.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Výstup obsahuje prohlížeč, dokumenty ze složky `docs/`, soubor se seznamem `lunascape-docs-manifest.json` a `.nojekyll`. Publikovat jej můžete umístěním na S3 nebo GitHub Pages. Příklad automatického publikování pomocí GitHub Actions najdete v úložišti v souboru `examples/workflows/publish-docs-pages.yml`.

> **Poznámka**
>
> - **Nikdy neexportujte dokumenty z neveřejného úložiště na GitHub Pages.** GitHub Pages mimo Enterprise Cloud si může přečíst kdokoli. Pokud potřebujete omezené publikování, použijte způsob 1 a nechte čtenáře přihlásit se přes GitHub.
> - Otevření souboru `index.html` přímo přes `file://` nefunguje, protože prohlížeče takto blokují načítání sousedních souborů a spouštění modulů ES. Pro místní kontrolu použijte rozšíření pro VS Code nebo server HTTP.
> - Vykreslovací knihovny pro TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob a Penrose se načítají až při zobrazení. K exportovanému webu umístěte i složku `vendor/`.

## Související témata

- [Co umí webová verze](README.md)
- [Čtení neveřejného úložiště](private-repository.md)
