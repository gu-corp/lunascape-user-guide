# A webes megjelenítő nem nyílik meg, vagy nem lehet bejelentkezni

## Bejelentkezés után sem jelenik meg az adattár a listában

Az adott fiókban nincs telepítve a „Lunascape Docs” GitHub App, vagy a telepítés nem terjed ki az érintett adattárra. Kérje meg az adattár tulajdonosát vagy a szervezet rendszergazdáját, hogy telepítse a [Nem nyilvános adattár megtekintése](../06-web/private-repository.md) című oldal lépései szerint.

## Nem lehet továbblépni a bejelentkezési képernyőről

- Nincs olvasási jogosultsága az érintett adattárhoz. Kérje meg az adattár tulajdonosát, hogy adja meg a jogosultságot.
- „Ezen a webhelyen nincs beállítva a GitHub-bejelentkezés”: a saját üzemeltetésű megjelenítőhöz nincs beállítva bejelentkezési szolgáltatás. A rendszergazdának kell beállítania egyet.

## Nem nyílik meg a bejelentkezési felugró ablak

A böngésző letiltotta a felugró ablakot. Engedélyezze a felugró ablakokat ehhez a webhelyhez, majd próbálja meg újra.

## „Lejárt a bejelentkezés” üzenet jelenik meg

A bejelentkezés érvényessége lejárt. Nyomja meg újra a [Bejelentkezés GitHubbal] gombot.

## Nyilvános adattár megnyitásakor 404-es hiba jelenik meg

- Ellenőrizze az `owner/repo@ref/dir` alakot.
- A `/` jelet tartalmazó ágnevek nem adhatók meg.

## Egy idő után nem sikerül a betöltés

Bejelentkezés nélkül a GitHub API használati korlátja (óránként 60 kérés) érvényes. Ha megjelenik az „Elérte a kérésszám korlátját” üzenet, várjon egy kis ideig, vagy jelentkezzen be a [Bejelentkezés GitHubbal] gombbal.

## „Erről a webhelyről nem jeleníthető meg ez az adattár” üzenet jelenik meg

Ha saját üzemeltetésű megjelenítőből szeretné megnyitni, az adattár `lunascape-docs.json` fájljának `viewer.origins` beállításához hozzá kell adni a webhely URL-címét.

## Az `index.html` megnyitásakor semmi nem jelenik meg

Közvetlenül `file://` protokollal megnyitva nem működik. Nyissa meg HTTP-kiszolgálón keresztül, vagy használja a VS Code-változatot.

## Az exportált webhelyen a „lunascape-docs-manifest.json nem található” üzenet jelenik meg

Helyezze ki változtatás nélkül mindazokat a fájlokat, amelyeket az `npm run export:web` parancs hozott létre (a jegyzékfájlt is beleértve).

## Nem menthető a piszkozat

- „Nem nyitható meg az IndexedDB”, „Egy másik lap használja”: ennek oka a böngésző privát módja, vagy egy másik lap, amelyen ugyanez a webhely van megnyitva. Nyissa meg szokásos ablakban, és zárja be a többi lapot.
- A piszkozatok eszközönként és böngészőnként tárolódnak. Másik eszközre nem kerülnek át.

## Kapcsolódó témák

- [GitHub-adattár megnyitása](../06-web/open-repository.md)
- [Piszkozatok mentése](../06-web/drafts.md)
