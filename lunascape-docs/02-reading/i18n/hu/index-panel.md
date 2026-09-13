# Az INDEX használata

A bal oldali INDEX a dokumentumgyökérben található mappák és dokumentumok fája.

## Szűrés

1. Írjon be egy szót az INDEX fölötti [Dokumentumok szűrése] mezőbe.
2. Csak azok az elemek jelennek meg, amelyek neve egyezik. Ha törli a beírt szöveget, minden visszaáll.

> **Megjegyzés**
>
> Szűrés közben a fogd és vidd módszerrel történő átrendezés nem használható.

## Mappák kinyitása és becsukása

- A mappanév bal oldalán lévő nyíl, illetve a borító nélküli mappa nevének megnyomása nyitja vagy csukja a mappát.
- Ha a mappának van borítója (tartalommal rendelkező `README.md` vagy `index.md`), a nevének megnyomása a borítót nyitja meg. Ha csak nyitni vagy csukni szeretné, használja az elem menüjében a [Mappa kinyitása] / [Mappa becsukása] parancsot.
- A mappák nyitott vagy csukott állapotát a rendszer felhasználónként jegyzi meg, és nem írja bele a Git által kezelt fájlokba.

## A README és a mappa borítója

A `README.md` az a fájl, amely leírja az adott mappa tartalmát.

- Ha a mappában van README, a mappanév megnyomásakor az jelenik meg.
- Ha nincs README, a mappában lévő legfelső dokumentum jelenik meg.
- A README címsora (H1) lesz a mappa neve az INDEX-ben.

A README nem kötelező. Utólagos hozzáadásához válassza a mappa elemmenüjében a [README létrehozása] parancsot (csak olyan mappáknál jelenik meg, amelyekben nincs README).

## Az INDEX megjelenítése és elrejtése

- Az eszköztár oszlopvezérlőinek bal oldali ikonja jeleníti meg vagy rejti el az INDEX-et. A jobb oldali ikon az „Ezen az oldalon” panelt jeleníti meg vagy rejti el.
- Keskeny képernyőn az INDEX csukott állapotban indul. A [Vissza] gombtól balra megjelenő [INDEX megnyitása] (három vonal) gomb megnyomásakor az INDEX a szöveg fölé úszva nyílik meg. Bezárni az INDEX-en belüli [×] gombbal, a háttérre kattintással, az `Esc` billentyűvel vagy másik dokumentumra lépéssel lehet. Ez az átmeneti állapot nem változtatja meg a széles képernyőn érvényes beállítást.
- Olyan dokumentumgyökérben, ahol csak egy megjelenítendő dokumentum van, az INDEX az első alkalommal magától becsukódik. Az oszlopvezérlő ikonjával újra megnyitható. Ez a viselkedés a [Megjelenítési beállítások] alatt az [Elrejtés, ha csak egy dokumentum van] kapcsolóval kikapcsolható.

## Az elemmenü használata

Az elemmenüt az INDEX egy elemére mutatva megjelenő [⋯] gombbal vagy az elemre jobb gombbal kattintva nyithatja meg. Az elemek a következő sorrendben jelennek meg.

| Csoport | Elemek |
|---|---|
| Gyakori műveletek | [Mappa kinyitása] / [Mappa becsukása], [INDEX megnyitása] (a mappa borítójának megnyitása), [Szerkesztés], [Cím módosítása], [Megnyitás VS Code-ban], [Útvonal másolása] |
| Létrehozás és rendezés | [README létrehozása] (csak README nélküli mappáknál), [Új dokumentum], [Új mappa], [Másolat készítése], [Fájlnév módosítása] / [Mappanév módosítása], [Mozgatás eggyel feljebb], [Mozgatás eggyel lejjebb] |
| Törlés | [Áthelyezés a kukába] |

- Ha közvetlenül a dokumentumgyökérben szeretne létrehozni valamit, nyomja meg az INDEX címsorának jobb szélén lévő [⋯] gombot, vagy kattintson jobb gombbal az INDEX üres részére, majd válassza az [Új dokumentum] vagy az [Új mappa] parancsot. Ugyanebben a menüben szerepel a [Dokumentumnév módosítása], és ha a dokumentumgyökérben nincs README, a [README létrehozása] is. Ugyanez a menü nyílik meg akkor is, ha az eszköztáron látható dokumentumnévre jobb gombbal kattint.
- A menün belül az `↑` `↓` billentyűkkel lépkedhet, a `Home` és az `End` az első, illetve az utolsó elemre ugrik. Az `Esc` bezárja a menüt, és a fókusz visszakerül oda, ahonnan megnyitotta.

> **Megjegyzés**
>
> A létrehozásra, rendezésre és törlésre szolgáló elemek csak akkor jelennek meg, ha a munkaterület megbízható a VS Code-ban. Nem használhatók dokumentum szerkesztése közben, sem akkor, amíg egy másik INDEX-művelet feldolgozása folyik.

## A megjelenés módosítása

A [Megjelenítési beállítások] alatt módosíthatja a fájlnevek megjelenítését, a dokumentumok és mappák ikonjait, a mappákban lévő elemek számát, a szintjelző vonalakat és a megjelenítési sűrűséget. Részletekért lásd: [A megjelenítési beállítások módosítása](display-settings.md).

## Kapcsolódó témák

- [Dokumentumok és mappák létrehozása és rendezése](../03-editing/organize.md)
- [A dokumentumok sorrendjének módosítása](../03-editing/reorder.md)
