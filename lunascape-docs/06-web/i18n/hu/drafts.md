# Piszkozat mentése

Ha a webes nézegetőben szerkeszt egy dokumentumot, a módosítások nem íródnak be az adattárba, hanem „piszkozatként” a böngészőben tárolódnak.

## Piszkozat létrehozása

1. Nyisson meg egy dokumentumot, és nyomja meg a jobb alsó sarokban a [Szerkesztés] gombot.
2. Szerkessze, majd nyomja meg a [Mentés] gombot.
   Megjelenik a „Mentve piszkozatként” üzenet, és a módosítás a böngészőben tárolódik.

- A piszkozattal rendelkező dokumentumok jelvényt kapnak az INDEX panelen. A szöveg fölött a „Ez a dokumentum az eszközön tárolt piszkozat (nincs közzétéve)” felirat jelenik meg.
- Az eszköztáron a [Piszkozatok] gomb mutatja a darabszámot, megnyomva pedig megnyílik a piszkozatok listája.

## Piszkozat elvetése

- Egyetlen dokumentum piszkozatának elvetéséhez nyomja meg a szöveg fölötti [A piszkozat elvetése] gombot.
- Az összes elvetéséhez használja a piszkozatok listáját.

## Átvezetés az adattárba

A piszkozatokat Pull Requestként elküldő „közzétételi kérés” megvalósult, de a nyilvános nézegetőben nincs engedélyezve. Ha az adattárba szeretné átvezetni a változtatásokat, szerkesszen a VS Code-változattal vagy egy helyi klónban.

> **Megjegyzés**
>
> - A piszkozatok a böngészőben (IndexedDB) tárolódnak. Nem kerülnek át másik böngészőbe vagy másik eszközre, és a böngésző webhelyadatainak törlésekor a piszkozatok is törlődnek.
> - Ha a piszkozat létrehozása után az adattárban lévő dokumentum megváltozik, megjelenik a „Az eredeti forrás megváltozott” felirat. Nézze át a tartalmat, majd döntse el, hogy elveti a piszkozatot, vagy megtartja.
> - Ha a [Dokumentumok megnyitása] paranccsal megnyitott helyi mappában szerkeszt, a mentés közvetlenül a fájlba történik, amennyiben a böngésző támogatja. Az ezt nem támogató böngészőkben a módosítások csak az adott munkamenet idejére maradnak meg.

## Kapcsolódó témák

- [Mire képes a webes nézegető](README.md)
- [Dokumentum szerkesztése](../03-editing/README.md)
