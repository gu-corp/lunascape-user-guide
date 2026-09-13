# Munka átadása az AI-nak

A Lunascape Docs nem hív meg nyelvi modellt. **Kontextust, eszközöket és ellenőrzést** készít elő, a fordítást, a korrektúrát és a szövegírást pedig arra az AI-ra bízza, amelyet Ön használ.

## A gondolat

| Amit a termék biztosít | Tartalom |
|---|---|
| Kontextus | A dokumentumok szabályai (hol vannak a fordítások, front matter, dokumentumszabvány, szójegyzék) és a célzott dokumentum helye |
| Munkaeszközök | A hiányzó és az elavult fordítások nyilvántartása, dokumentumok olvasása és írása, létrehozás sablonból |
| Utólagos ellenőrzés | Ellenőrzés a docs-lint segítségével, valamint a lefedettség és a frissesség eltérése |

Az utasítás nem tartalmazza a dokumentum szövegét: az AI maga olvassa be a fájlokat, maga írja őket, és maga ellenőrzi az eredményt.

## A munka átadása

1. Nyomja meg az eszköztáron a [Dokumentumeszközök] gombot, és nyissa meg az [AI] lapot.
2. Válassza ki az átadni kívánt feladatot a [Feladat] listából.
3. Töltse ki a szükséges mezőket (célnyelv, téma).
4. Nyomja meg a [Feladat átadása] gombot.
   Megnyílik a VS Code terminálja, a kiválasztott AI átveszi az utasítást, és megkezdi a munkát.

> **Tipp**
>
> A Claude Code munkamenetét munkaeszközök kísérik (a `lunascape-docs` MCP-kiszolgáló). A munkamenet önállóan le tudja kérni a hiányzó és elavult fordítások listáját, futtatni tudja a docs-lint ellenőrzést, és rögzíteni tudja a fordítás frissességét.

## Az eredmény ellenőrzése

| A szolgáltató típusa | Hová kerül az eredmény |
|---|---|
| Munkamenet alapú (Claude Code, Codex) | Közvetlenül a munkafába ír. **A Git eltérésében ellenőrizze** |
| API alapú (a VS Code nyelvi modelljei, Anthropic, OpenAI-kompatibilis) | Dokumentumonként ad javaslatot. Ellenőrizze az [Eltérés megnyitása] gombbal, majd írja ki a [Mentés] gombbal |

### API alapú javaslat ellenőrzése

API alapú szolgáltatóval futtatva a javaslat az [AI] lapra érkezik.

1. Nyomja meg az [Eltérés megnyitása] gombot, és hasonlítsa össze a javaslatot a jelenlegi tartalommal.
2. Ha megfelel, nyomja meg a [Mentés] gombot. Fordítás esetén a frissesség is rögzül. Ha mégsem kéri, nyomja meg az [Elvetés] gombot.
   A generálás félbeszakításához nyomja meg a [Leállítás] gombot.

> **Megjegyzés**
>
> - A Lunascape Docs soha nem végez Git-előkészítést és nem készít commitot. A változásokat mindig az eltérésben ellenőrizze.
> - Nem megbízható munkaterületen, illetve dokumentumgyökéren kívüli, ideiglenesen megnyitott mappa böngészésekor nem lehet feladatot átadni.

## Kapcsolódó témák

- [Átadható feladatok](tasks.md)
- [AI-beállítások](settings.md)
- [A nyilvántartás és a rögzített adatok](ledger.md)
