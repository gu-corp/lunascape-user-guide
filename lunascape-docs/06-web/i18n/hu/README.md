# Mit tud a webes megjelenítő

A Lunascape Docs webes változata a <https://docs.lunascape.org/> címen érhető el. Telepítés nélkül olvashatja a GitHubon tárolt dokumentumokat, mintha egy webhely lenne.

## Funkciók

| Funkció | Leírás |
|---|---|
| Nyilvános adattárak megtekintése | Bejelentkezés nélkül megnyitja egy nyilvános GitHub-adattár dokumentumait |
| Nem nyilvános adattárak megtekintése | GitHub-bejelentkezés után megnyithatja azokat az adattárakat, amelyekhez olvasási jogosultsága van |
| Helyi mappák megtekintése | A [Dokumentumok megnyitása], majd a [Dokumentumok megnyitása helyi mappából] paranccsal megnyit egy mappát az eszközén (csak a támogatott böngészőkben) |
| Olvasási funkciók | INDEX, hivatkozások, előzmények, szűrés, oldalon belüli tartalomjegyzék, nyelvváltás és témaváltás. Ugyanaz, mint a VS Code-változatban |
| Ábrák és képletek | Mermaid, Vega-Lite, Markmap, WaveDrom, Svgbob, Penrose, KaTeX-képletek |
| Piszkozatok | Szerkesztheti a dokumentumokat, és a módosításokat piszkozatként tarthatja meg az eszközén. Az adattárba semmi nem íródik |
| Közvetlen hivatkozás egy oldalra | Az URL-ben megadható az adattár és az oldal, így egy adott oldal közvetlenül megnyitható |

## Eltérések a VS Code-változattól

- A dokumentumellenőrzés, a sablonból való létrehozás, a fordítási javaslatok készítése és az INDEX-ből való rendezés a webes változatban nem érhető el.
- A TikZ-ábrák nem jelennek meg.
- A szerkesztések nem íródnak be az adattárba, hanem piszkozatként maradnak az eszközén. A piszkozatokat pull requestként elküldő „közzétételi kérés” funkció el van készítve, de a nyilvános megjelenítőben nincs bekapcsolva. Ha az adattárban is érvényesíteni szeretné a módosításokat, szerkesszen a VS Code-változattal vagy egy helyi klónban.

## Kapcsolódó témák

- [GitHub-adattár megnyitása](open-repository.md)
- [Nem nyilvános adattár megtekintése](private-repository.md)
- [Piszkozatok mentése](drafts.md)
