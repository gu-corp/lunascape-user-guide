# Képek méretének beállítása

A dokumentumba illesztett képek automatikusan a szövegtörzs szélességéhez és a képernyő magasságához igazodnak. Ha egy képet adott méretben szeretne megjeleníteni, megadhatja a szélességét.

## Az automatikus igazítás működése

- A szokásos Markdown-képek (`![leírás](./images/screen.png)`) a szövegtörzs szélességéhez kicsinyítve jelennek meg. Az eredeti méretüknél nagyobbra soha nem nagyítja őket.
- Az álló tájolású képernyőképek legfeljebb a képernyő magasságának 72%-áig vagy 720px-ig jelennek meg, amelyik kisebb.

## A szélesség megadása a szerkesztőben

1. Nyomja meg a [Szerkesztés] gombot, majd jelölje ki a képet a vizuális nézetben.
2. Válasszon szélességet az eszköztár [Képméret] menüjéből.
3. Nyomja meg a [Mentés] gombot.

| Lehetőség | Szélesség |
|---|---|
| [Automatikus] | Nincs megadva (automatikus igazítás) |
| [Kicsi (360px)] | 360px |
| [Közepes (560px)] | 560px |
| [Nagy (760px)] | 760px |
| [Szövegtörzs szélessége (920px)] | 920px |
| [Egyéni…] | Tetszőleges egész szám 16 és 4096px között |

## A szélesség megadása Markdownban

Adjon meg számértékű `width` attribútumot a HTML `img` címkéjén. Ez a írásmód a GitHubon és MDX-ben is ugyanígy jelenik meg.

```html
<img src="./images/screen.png" alt="Beállítási képernyő" width="360" />
```

> **Megjegyzés**
>
> - A `width` értéke csak szám lehet, `px` vagy `%` nélkül. Ha a szövegtörzs szélességénél nagyobb értéket ad meg, a megjelenítés akkor is a szövegtörzs szélességéhez igazodik.
> - A képekre a dokumentumhoz viszonyított relatív útvonallal hivatkozzon. A dokumentumgyökéren kívüli képek nem jelennek meg.

## Kapcsolódó témák

- [Dokumentum szerkesztése](README.md)
- [Az ábrák, képletek vagy képek nem jelennek meg](../07-troubleshooting/rendering.md)
