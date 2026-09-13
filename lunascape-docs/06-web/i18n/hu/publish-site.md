# Saját dokumentumok közzététele a weben

A saját adattárában lévő dokumentumokat webhelyként teheti közzé a GitHub Pages vagy bármely statikus tárhely segítségével. Erre két mód van. Az alábbi lépések olyan fejlesztőknek szólnak, akik klónozni tudják a Lunascape Docs adattárát, és tudják használni az `npm` parancsot.

## 1. mód: a megjelenítő két fájljának elhelyezése

Csak magát a megjelenítőt (`index.html` és `lsdoc.js`) helyezi ki, a dokumentumokat pedig a GitHub felől tölti be. Maguk a dokumentumok nem részei a webhelynek, ezért ez a mód nem nyilvános adattárak esetén is biztonságos (az olvasók a GitHubon jelentkeznek be).

1. Futtassa a következő parancsot a Lunascape Docs adattárában.

   ```sh
   npm run build:viewer
   ```

   A `dist/viewer/` mappában létrejön az `index.html` és az `lsdoc.js`.
2. Helyezze a két fájlt a közzétenni kívánt adattár `docs/` mappájába.
3. Kapcsolja be a GitHub Pages szolgáltatást.

A megjelenítendő dokumentumgyökeret a rendszer a következő sorrendben határozza meg.

1. Az `index.html` fájlban lévő `source` beállítás
2. Az ugyanabban a mappában lévő `lunascape-docs.json` fájlban megadott `repository`
3. A `*.github.io` URL-ből és az ágak felépítéséből való következtetés

## 2. mód: statikus webhely kiírása a dokumentumokkal együtt

A megjelenítőt és a dokumentumfájlokat együtt írja ki, és az eredményt változatlanul helyezi ki tárhelyre.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

A kimenet tartalmazza a teljes megjelenítőt, a `docs/` alatti dokumentumokat, a `lunascape-docs-manifest.json` listafájlt és a `.nojekyll` fájlt. A közzétételhez helyezze a kimenetet S3-ra vagy a GitHub Pagesre. A GitHub Actions segítségével történő automatikus közzétételre példát az adattár `examples/workflows/publish-docs-pages.yml` fájljában talál.

> **Megjegyzés**
>
> - **Ne írja ki nem nyilvános adattár dokumentumait a GitHub Pagesre.** Az Enterprise Cloudon kívüli GitHub Pages tartalmát bárki megtekintheti. Ha korlátozott közzétételre van szüksége, használja az 1. módot, és jelentkeztesse be az olvasókat a GitHubon.
> - Az `index.html` közvetlen, `file://` protokollal való megnyitása nem működik, mert a böngésző így tiltja a szomszédos fájlok betöltését és az ES modulok futtatását. Helyi ellenőrzéshez használja a VS Code-os változatot vagy egy HTTP-kiszolgálót.
> - A TikZ, a Vega-Lite, a Markmap, a WaveDrom, a Svgbob és a Penrose rajzoló programkönyvtárai megjelenítéskor töltődnek be. A kiírt webhelynél helyezze ki a `vendor/` mappát is.

## Kapcsolódó témák

- [Mire képes a webes változat](README.md)
- [Nem nyilvános adattár olvasása](private-repository.md)
