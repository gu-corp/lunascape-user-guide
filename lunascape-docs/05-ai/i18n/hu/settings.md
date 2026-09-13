# AI-beállítások

Válassza ki azt az AI-t és modellt, amely megkapja a munkát. Ez a képernyő saját legördülő listákat használ, nem a VS Code gyorsválasztóját.

1. Nyomja meg a [Dokumentumeszközök] → [AI] lapot → [AI-beállítások…] gombot.
2. Válasszon szolgáltatót a [Szolgáltató] alatt.
   Azok, amelyek ezen a gépen nem használhatók, nem választható állapotban, az okkal együtt jelennek meg.
3. Válasszon modellt a [Modell] alatt. A választható elemek szolgáltatónként változnak.
4. Zárja be a képernyőt. A választás felhasználónként mentődik, és legközelebb is ez lesz érvényben.

## Szolgáltatók

| Szolgáltató | Forma | Felismerés |
|---|---|---|
| Claude Code | Munkamenet | A `claude` parancs megléte |
| Codex | Munkamenet | A `codex` parancs megléte |
| VS Code nyelvi modellek | API | A VS Code Language Model API-ban regisztrált modellek |
| Anthropic API | API | Regisztrált API-kulcs |
| OpenAI-kompatibilis API | API | Regisztrált API-kulcs és végpont |

A **munkamenet** típusú szolgáltató maga olvassa és írja a fájlokat, és a dokumentum-ellenőrzést is maga futtatja. Az eredmény közvetlenül a munkafába kerül, és a Git-különbségben tekinthető át.

Az **API** típusú szolgáltató egy dokumentumnyi Markdown-szöveget ad vissza, a bővítmény pedig mentés előtt megmutatja a különbséget.

## API-kulcs regisztrálása

Az Anthropic API és az OpenAI-kompatibilis API-k akkor használhatók, ha regisztrál egy API-kulcsot.

1. Válassza ki a szolgáltatót a [Szolgáltató] alatt. Megjelenik a kulcs beviteli mezője.
2. Írja be a kulcsot az [API-kulcs] mezőbe. OpenAI-kompatibilis API esetén a [Végpont] mezőt is töltse ki (például: `https://api.openai.com/v1`).
3. Nyomja meg a [Mentés] gombot. Megjelenik a „Kulcs regisztrálva” felirat.

> **Megjegyzés**
>
> - A kulcsok a VS Code SecretStorage tárolójába kerülnek, és többé nem jelennek meg. A `settings.json` fájlba vagy bármely dokumentumba sem íródnak be. A [Kulcs törlése] gombbal törölhetők.
> - A modellek listáját a bővítmény a regisztrált kulccsal kéri le az egyes szolgáltatásoktól; amíg ez nem sikerül, egy ismert listát mutat.
> - Az API típusú szolgáltatóval csak az „Oldal fordítása” és az „Oldal korrektúrázása” futtatható. Több dokumentum végigjárása és dokumentumok létrehozása munkamenet típusú szolgáltatót igényel.

> **Tipp**
>
> Ha egyetlen szolgáltató sem található, telepítse a Claude Code-ot vagy a Codexet, illetve regisztráljon egy API-kulcsot. Nyissa meg újra az [AI-beállítások…] ablakot, és a rendszer felismeri.

## Kapcsolódó témák

- [Munka átadása az AI-nak](README.md)
- [VS Code beállítások](../08-reference/settings.md)
