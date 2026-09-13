# Dokumentum létrehozása sablonból

A Dokumentumeszközök [Létrehozás] lapján sablont választhat, megtekintheti a tartalom előnézetét, majd létrehozhat egy új dokumentumot.

1. Nyomja meg az eszköztáron a [Dokumentumeszközök] gombot, és nyissa meg a [Létrehozás] lapot.
2. Nyomja meg a [Létrehozás sablonból] gombot, és válasszon sablont.
3. Töltse ki a beviteli mezőket (cím, összefoglalás stb.). A kötelező mezőknél a „Kötelező” jelzés látható.
4. Adja meg a mentési helyet a dokumentumgyökérhez viszonyított relatív útvonalként (például: `03-design/api.md`).
5. Nyomja meg az [Előnézet] gombot, és ellenőrizze a létrejövő Markdown tartalmat.
6. Nyomja meg a [Létrehozás ezzel a tartalommal] gombot.
   A dokumentum létrejön, és megjelenik a megjelenítőben. Ezt követően a rendszer a teljes dokumentumgyökeret ellenőrzi.

## Választható sablonok

| Sablon | Tartalom |
|---|---|
| Egyoldalas dokumentum | Rövid specifikáció, jegyzet vagy önálló magyarázó dokumentum egyetlen fájlban |
| Specifikáció, kézikönyv, súgó | Egy fájl általános fejezetszerkezettel, amely specifikációhoz, kézikönyvhöz és súgóhoz egyaránt használható |
| Standard Pack sablonjai | Ha a `lunascape-docs.json` fájlban a Standard Pack van kiválasztva, kiegészül az adott profilban használható dokumentumtípusokkal (követelményleírás, tervdokumentum stb.) |

> **Megjegyzés**
>
> - A létrehozáshoz megbízható munkaterület szükséges.
> - A meglévő fájlokat a program nem írja felül. Ha a mentési helyen már van azonos nevű dokumentum, a létrehozás nem sikerül.
> - A mentési helyhez `.md` vagy `.mdx` kiterjesztés szükséges. Az `i18n` alatt (a fordítások helyén) nem hozható létre dokumentum.
> - Ha módosítja a bevitt adatokat, a létrehozás előtt nyomja meg ismét az [Előnézet] gombot.

> **Tipp**
>
> Olyan projektben, amelyben még nincs dokumentummappa, az első készletet a parancskatalógus „Lunascape Docs: Dokumentum létrehozása sablonból” parancsával hozhatja létre. Lásd: [Az első dokumentumok létrehozása](../01-introduction/first-documents.md).

## Kapcsolódó témák

- [A Dokumentumeszközök használata](README.md)
- [Ellenőrzési szabályok módosítása](rules.md)
