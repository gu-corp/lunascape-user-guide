# Dokumentumok és mappák létrehozása és rendszerezése

Az INDEX elemmenüjéből dokumentumokat és mappákat hozhat létre, másolhat, nevezhet át és törölhet. A bevitel a megjelenítőn belüli kis párbeszédpanelen történik, így az olvasás nem szakad meg.

> **Megjegyzés**
>
> Ezek a műveletek csak akkor érhetők el, ha a munkaterület megbízható a VS Code-ban. Nem hajthatók végre dokumentum szerkesztése közben, másik művelet feldolgozása alatt, illetve ha az elemen nem mentett módosítások vannak.

## Dokumentum vagy mappa létrehozása

1. Nyissa meg a célmappa elemmenüjét ([⋯] vagy jobb kattintás).
   Ha közvetlenül a dokumentumgyökérben szeretne létrehozni, használja az INDEX fejlécének jobb szélén lévő [⋯] gombot, vagy kattintson jobb gombbal az INDEX üres területére.
2. Válassza az [Új dokumentum] vagy az [Új mappa] lehetőséget.
3. Adjon meg egy nevet, majd nyomja meg a [Létrehozás] gombot.
   A dokumentum nevének Markdown-kiterjesztéssel kell rendelkeznie (`.md`, `.markdown`, `.mdx` és így tovább).

Az új dokumentumok az alapértelmezett nyelv dokumentumaként (hiteles dokumentumként) jönnek létre.

## Dokumentum másolatának készítése

1. Nyissa meg a dokumentum elemmenüjét, és válassza a [Másolat készítése] lehetőséget.
2. Adjon meg egy új nevet, majd nyomja meg a [Létrehozás] gombot.

Csak a hiteles dokumentumról készül másolat; a fordításairól nem.

## A cím módosítása

Módosítja a dokumentum címsorát (H1). A fájlnév nem változik.

1. Nyissa meg a dokumentum vagy a mappa elemmenüjét, és válassza a [Cím módosítása] lehetőséget.
2. Adja meg az új címet egy sorban, majd nyomja meg a [Módosítás] gombot.

Mappa esetén az adott mappa `README.md` fájljának címsora módosul. Ha éppen egy fordítás látható, az adott nyelvű dokumentum címe változik meg.

## A dokumentumnév módosítása

Módosítja az eszköztáron látható dokumentumnevet (a dokumentumgyökér nevét).

1. Kattintson jobb gombbal az eszköztáron lévő dokumentumnévre. Ugyanez a menü az INDEX fejlécének jobb szélén lévő [⋯] gombbal is megnyitható.
2. Válassza a [Dokumentumnév módosítása] lehetőséget, és adjon meg egy új nevet.

Amíg nincs beállítva, a mappa neve jelenik meg.

A megadott név **arra a helyre kerül, amely jelenleg a dokumentumnevet adja**. A név nem olyan helyre íródik, amely nem jelenik meg, így a látható címsor soha nem marad figyelmen kívül.

| Jelenlegi állapot | Írás helye |
|---|---|
| A `lunascape-docs.json` tartalmaz nevet | A `lunascape-docs.json` frissül |
| Nincs név, de a dokumentumgyökérben van README | A README címsora (H1) íródik felül |
| Egyik sincs | Létrejön a `lunascape-docs.json`, és a név ott mentődik |

A módosítás után megjelenő üzenet megmutatja, melyik helyre történt az írás.

> **Tipp**
>
> A dokumentumnevet a rendszer ebben a sorrendben határozza meg: a `lunascape-docs.json` fájlban megadott név, majd a dokumentumgyökér README fájljának címsora, végül a mappa neve.

## Fájlnév vagy mappanév módosítása

1. Nyissa meg az elemmenüt, és válassza a [Fájlnév módosítása] vagy a [Mappanév módosítása] lehetőséget.
2. Adja meg az új nevet, majd nyomja meg a [Módosítás] gombot.

A megfelelő fordítások (ugyanaz az útvonal az `i18n/<nyelv>/` mappa alatt) is átnevezésre kerülnek.

## Törlés

1. Nyissa meg az elemmenüt, és válassza az [Áthelyezés a kukába] lehetőséget.
2. Ellenőrizze a megerősítő üzenet tartalmát, és hagyja jóvá az áthelyezést.

Az elem az operációs rendszer kukájába kerül, így szükség esetén visszaállítható. A fordítások nem törlődnek, a helyükön maradnak.

## Nem használható nevek

- `.` karakterrel kezdődő nevek (mert nem jelennének meg az INDEX panelen)
- `i18n` (a fordítási fájlok számára fenntartva)
- A Windows által fenntartott nevek (`CON`, `PRN` és hasonlók)
- Ponttal vagy szóközzel végződő nevek
- Vezérlőkaraktereket vagy fájlnévben nem engedélyezett karaktereket tartalmazó nevek
- Az adott mappában már létező nevek (beleértve a csak kis- és nagybetűkben eltérő neveket is)

> **Megjegyzés**
>
> A kezdőlap (általában a gyökérben lévő `README.md`) nem nevezhető át és nem helyezhető át. Előbb módosítsa a `startPage` értékét a `lunascape-docs.json` fájlban.

## Kapcsolódó témák

- [A dokumentumok sorrendjének módosítása](reorder.md)
- [Az INDEX használata](../02-reading/index-panel.md)
