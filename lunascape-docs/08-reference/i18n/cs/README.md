# Hlavní specifikace

## Provozní požadavky

| Prostředí | Požadavky |
|---|---|
| Rozšíření pro VS Code | VS Code 1.90 nebo novější. Funkce, které zapisují soubory, vyžadují důvěryhodný pracovní prostor |
| Webový prohlížeč | Nedávné verze Chrome, Edge, Safari nebo Firefox. Otevření místní složky vyžaduje prohlížeč s podporou výběru složky (File System Access API) |
| Rozšíření pro Chromium | Manifest V3. Nevyžaduje žádná oprávnění k hostitelům |

## Podporované dokumenty

| Položka | Obsah |
|---|---|
| Soubory | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tabulky, seznamy úkolů, bloky kódu, přeškrtnutí), místní obrázky, YAML front matter |
| MDX | Zobrazují se pouze povolené komponenty. Libovolné skripty se nespouštějí |
| HTML | Před zobrazením se ošetří pomocí DOMPurify 3.4.14 |

## Diagramy a vzorce

| Druh | Název jazyka | Poznámky |
|---|---|---|
| Vzorce | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Pouze vložená data. Externí URL a značky obrázků nejsou možné |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Pouze striktní JSON |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | V distribuované verzi se zdroj zobrazuje sbalený. Limity: vstup 64 KiB, 15 sekund, SVG 2 MiB |
| Penrose (experimentální) | `penrose` | Pouze předvolba `set-theory` |

## Limity

| Položka | Hodnota |
|---|---|
| Výsledek rozbalení šablony | 4 MiB |
| Referenční kontext překladu | Výchozí 49 152 znaků, nejvýše 1 048 576 znaků |
| Počet dokumentů v jednom hromadném překladu | 1 000 |
| Vlastní šířka obrázku | 16–4096 px |

## Soubory

| Soubor | Role | Ve správě Git |
|---|---|---|
| `lunascape-docs.json` | Nastavení kořene dokumentace | Ano |
| `docs-lint.config.json` | Nastavení pravidel kontroly | Ano |
| `.lunascape-docs/translation-freshness.json` | Záznam aktuálnosti překladů (pouze cesty, jazyky, hashe a časové značky) | Ano |
| Nastavení VS Code a stav pracovního prostoru | Osobní nastavení zobrazení, volba poskytovatele, stav rozbalení panelu INDEX | Ne |

## Přiložený Standard Pack

`builtin:gu-corp-software` — profily: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Související témata

- [Přehled nastavení VS Code](settings.md)
- [Zabezpečení a hranice zápisu](security.md)
