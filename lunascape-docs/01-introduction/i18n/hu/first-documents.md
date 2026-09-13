# Az első dokumentumok létrehozása

Olyan projektben, amelyben még nincs dokumentummappa, a parancspalettáról létrehozhatja az első dokumentumkészletet.

1. Nyissa meg a projekt mappáját a VS Code-ban, és tegye megbízhatóvá a munkaterületet.
2. A parancspalettán (`⇧⌘P` / `Ctrl+Shift+P`) futtassa a „Lunascape Docs: Dokumentáció létrehozása sablonból" parancsot.
   Ha a munkaterület több mappát tartalmaz, válassza ki azt, amelyikben a dokumentumok létrejönnek.
3. Válassza ki a létrehozandó szerkezetet.
   - [Egyoldalas dokumentum]: csak egy `README.md`, a lehető legkisebb szerkezet. Rövid specifikációhoz, jegyzethez vagy önálló leíráshoz való.
   - [Dokumentumkészlet]: egy főoldal, valamint a `specification/` (specifikáció), a `manual/` (kézikönyv) és a `help/` (súgó) belépő oldala.
4. Adja meg a dokumentáció címét. A program a README-ben és az egyes dokumentumok címsoraiban használja.
5. Adja meg a létrehozandó dokumentummappát. A munkaterülethez képest relatív útvonal, alapértelmezés szerint `docs`.
6. Ellenőrizze a létrehozandó fájlok listáját, majd nyomja meg a [Létrehozás] gombot.
   A létrehozás végén az új `README.md` megnyílik a megjelenítőben.

> **Megjegyzés**
>
> - A meglévő fájlokat a program nem írja felül. Ha a létrehozandó fájlok közül akár egy is létezik már, semmi sem jön létre, és a művelet megszakad.
> - Nem megbízható munkaterületen nem lehet létrehozni.

> **Tipp**
>
> - Ha már van dokumentummappája, erre a lépéssorra nincs szükség. Folytassa az [Alapvető műveletek](../02-reading/README.md) oldallal.
> - Ahogy nő a dokumentumok száma, a Dokumentumeszközök [Létrehozás] lapján sablont választva egyesével vehet fel újabb dokumentumokat.

## Kapcsolódó témák

- [Dokumentum létrehozása sablonból](../04-document-tools/templates.md)
- [Dokumentumgyökerek és fájlkonvenciók](../04-document-tools/structure.md)
