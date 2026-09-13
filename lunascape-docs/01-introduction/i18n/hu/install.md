# A bővítmény telepítése

A VS Code „Lunascape Docs Pro” bővítménye VSIX fájlként érhető el. Ingyenes; a „Pro” azt a kiadást jelöli, amely átadja a munkát egy AI-nak, és önmagát frissíti.

## Rendszerkövetelmények

- VS Code 1.90 vagy újabb
- Az írással járó funkciók — Dokumentum létrehozása, az INDEX rendezése, az Ellenőrzés beállításainak mentése, Fordítás — csak olyan munkaterületen működnek, amelyet a VS Code-ban megbízhatónak jelöltél.

## Telepítés

1. Szerezd meg a VSIX fájlt. Ez a hivatkozás mindig a legfrissebb változatra mutat.

   [lunascape-docs-pro.vsix letöltése](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Nyisd meg a Bővítmények nézetet (`⇧⌘X` / `Ctrl+Shift+X`).
3. A jobb felső `…` menüből válaszd a [Telepítés VSIX-ből…] parancsot, és add meg a letöltött fájlt.

### Parancssorból

Egyetlen sor, ha nem szeretnél kilépni a terminálból. Letölti és telepíti.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Megjegyzés**
> Ha a `code` nem található, futtasd a [Rendszerhéj-parancs: A „code” parancs telepítése a PATH-ba] parancsot a Parancspalettából (`⇧⌘P` / `Ctrl+Shift+P`).

## Frissítés

Amikor új változat jelenik meg, a bővítmény maga tölti le és telepíti. A VS Code felajánlja az ablak újratöltését, és attól kezdve azt használod. A beállításaid és a dokumentumaid érintetlenek maradnak.

Naponta egyszer ellenőriz. Ha most szeretnéd ellenőrizni, futtasd a [Lunascape Docs: Frissítés keresése] parancsot a Parancspalettából (`⇧⌘P` / `Ctrl+Shift+P`).

A `lunascapeDocEditor.update.check` beállítással változtathatod meg a működést.

| Beállítás | Működés |
|---|---|
| Új változat telepítése, amikor megjelenik | Alapértelmezett |
| Jelezze, és mindig magam döntsem el | Értesítés jelenik meg, és semmi nem változik, amíg meg nem nyomod a [Frissítés] gombot |
| Ne ellenőrizzen | Nem történik semmi |

### Amikor nem tud frissülni

Ha a „A frissítést nem sikerült letölteni: No Servers” üzenet jelenik meg, a telepített változat 0.22.18 vagy régebbi. Ennek a változatnak a frissítési útvonala mindig az utolsó lépésnél hibázik el, ezért nem tud magától újabb változatra jutni. Telepítsd egyszer kézzel a fenti módon; attól kezdve maga frissül.

## A verzió ellenőrzése

Nyisd meg a „Lunascape Docs Pro” elemet a Bővítmények nézetben, hogy lásd a telepített verziót. Erre szükséged lesz, amikor hibát jelentesz.

## Kapcsolódó témák

- [Első dokumentumaid létrehozása](first-documents.md)
- [Hiba jelentése](../07-troubleshooting/report.md)
