# Fő specifikációk

## Rendszerkövetelmények

| Környezet | Követelmények |
|---|---|
| VS Code bővítmény | VS Code 1.90 vagy újabb. Az írással járó funkciók megbízható munkaterületen működnek |
| Webes böngészőváltozat | Friss Chrome, Edge, Safari vagy Firefox. Helyi mappa megnyitásához olyan böngésző szükséges, amely támogatja a mappaválasztást (File System Access API) |
| Chromium bővítmény | Manifest V3. Nem kér gazdagép-jogosultságokat |

## Támogatott dokumentumok

| Elem | Tartalom |
|---|---|
| Fájlok | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (táblázatok, feladatlisták, kódblokkok, áthúzás), helyi képek, YAML front matter |
| MDX | Csak az engedélyezett összetevők jelennek meg. Tetszőleges parancsfájlokat nem futtat |
| HTML | A megjelenítés előtt a DOMPurify 3.4.14 tisztítja meg |

## Ábrák és képletek

| Típus | Nyelvnév | Megjegyzés |
|---|---|---|
| Képletek | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Csak beágyazott adatok. Külső URL-ek és képjelölők nem használhatók |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Csak szigorú JSON |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | A terjesztett változatban a forrás összecsukva jelenik meg. Korlátok: 64 KiB bemenet, 15 másodperc, 2 MiB SVG |
| Penrose (kísérleti) | `penrose` | Csak a `set-theory` előbeállítás |

## Korlátok

| Elem | Érték |
|---|---|
| A sablon kibontott mérete | 4 MiB |
| A fordítás hivatkozási környezete | alapértelmezés szerint 49 152 karakter, legfeljebb 1 048 576 karakter |
| Egy kötegelt fordítás dokumentumainak száma | 1000 dokumentum |
| Egyéni képszélesség | 16–4096 px |

## Fájlok

| Fájl | Szerep | Git-ben |
|---|---|---|
| `lunascape-docs.json` | A dokumentumgyökér beállításai | Igen |
| `docs-lint.config.json` | Az ellenőrzési szabályok beállításai | Igen |
| `.lunascape-docs/translation-freshness.json` | A fordítás frissességének nyilvántartása (csak útvonalak, nyelvek, hasítóértékek és időbélyegek) | Igen |
| VS Code-beállítások és munkaterület-állapot | Személyes megjelenítési beállítások, a szolgáltató kiválasztása, az INDEX nyitott vagy zárt állapota | Nem |

## A mellékelt Standard Pack

`builtin:gu-corp-software` — profilok: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Kapcsolódó témák

- [VS Code-beállítások listája](settings.md)
- [Biztonság és írási határok](security.md)
