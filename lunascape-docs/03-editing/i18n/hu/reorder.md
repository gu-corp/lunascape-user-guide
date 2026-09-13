# A dokumentumok sorrendjének módosítása

Az INDEX-ben megjelenő sorrend fogd és vidd módszerrel vagy billentyűzettel módosítható. A módosított sorrend a dokumentum front matterébe kerül `navigation.order` néven.

## Átrendezés fogd és vidd módszerrel

1. Húzzon meg egy dokumentumot vagy mappát az INDEX-ben.
2. Ejtse egy azonos szintű elem elé vagy mögé, illetve egy mappára.
   Azonos szinten a sorrend változik meg. Ha másik mappára ejti, az elem abba a mappába kerül át.

## Átrendezés billentyűzettel vagy menüből

- Vigye a fókuszt egy INDEX-elemre, és nyomja meg az `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓` billentyűket.
- Válassza az elem menüjéből a [Mozgatás eggyel feljebb] / [Mozgatás eggyel lejjebb] parancsot.

## A mentett tartalom

- Azonos szinten történő átrendezéskor a hiteles dokumentum front matterében lévő `navigation.order` érték frissül. Mappa esetén az érték a mappa `README.md` fájljába íródik. Ha a mappában nincs `README.md`, csak front mattert tartalmazó `README.md` jön létre.
- Másik mappába mozgatáskor a hiteles dokumentum és a hozzá tartozó fordítások együtt kerülnek át. A mozgatás előtt megerősítő kérdés jelenik meg a relatív hivatkozásokat érintő hatásról.
- A program nem végez Git-előkészítést (staging) és nem készít commitot.

> **Megjegyzés**
>
> - Szűrés közben, dokumentum szerkesztése közben és nem megbízható munkaterületen nem lehet átrendezni.
> - Ha megjelenik az „Az INDEX frissült” üzenet, akkor éppen egy másik módosítás érvényesült. Végezze el újra a műveletet.
> - A kezdőoldal nem helyezhető át másik mappába.

> **Tipp**
>
> Ha a `navigation.order` értékeket 100-as lépésekben adja meg – például 100, 200, 300 –, később könnyen beszúrhat közéjük dokumentumokat. Részletek: [Navigációs adatok beállítása](../04-document-tools/navigation-metadata.md).

## Kapcsolódó témák

- [Dokumentumok és mappák létrehozása és rendezése](organize.md)
- [Navigációs adatok beállítása](../04-document-tools/navigation-metadata.md)
