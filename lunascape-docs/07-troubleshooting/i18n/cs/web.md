# Webová verze se neotevře nebo se nelze přihlásit

## Po přihlášení se úložiště nezobrazí v seznamu

Na daném účtu není nainstalována aplikace GitHub App „Lunascape Docs“, nebo dané úložiště není zahrnuto. Požádejte vlastníka úložiště nebo správce organizace o instalaci podle postupu v části [Zobrazení neveřejného úložiště](../06-web/private-repository.md).

## Nelze pokračovat za přihlašovací obrazovkou

- Nemáte oprávnění ke čtení daného úložiště. Požádejte vlastníka úložiště o přidělení oprávnění.
- „Pro tento web není nastaveno přihlášení přes GitHub“: u prohlížeče, který jste nasadili sami, není nastavena přihlašovací služba. Přihlašovací službu musí nastavit správce.

## Vyskakovací okno pro přihlášení se neotevře

Prohlížeč blokuje vyskakovací okna. Povolte vyskakovací okna pro tento web a zkuste to znovu.

## Zobrazí se „Přihlášení vypršelo“

Platnost přihlášení vypršela. Znovu stiskněte [Přihlásit se přes GitHub].

## Veřejné úložiště vrací 404

- Zkontrolujte zápis `owner/repo@ref/dir`.
- Názvy větví obsahující `/` nelze zadat.

## Po chvíli se přestane načítat

Bez přihlášení platí omezení používání GitHub API (60krát za hodinu). Pokud se zobrazí „Byl dosažen limit počtu požadavků“, chvíli počkejte, nebo se přihlaste pomocí [Přihlásit se přes GitHub].

## Zobrazí se „Z tohoto webu nelze toto úložiště zobrazit“

Aby bylo možné úložiště otevřít z prohlížeče, který jste nasadili sami, je nutné přidat URL daného webu do `viewer.origins` v souboru `lunascape-docs.json` na straně úložiště.

## Po otevření `index.html` se nic nezobrazí

Při přímém otevření pomocí `file://` to nefunguje. Otevřete soubor přes HTTP server, nebo použijte verzi pro VS Code.

## Na exportovaném webu se zobrazí „Soubor lunascape-docs-manifest.json nebyl nalezen“

Nasaďte beze změn celou sadu souborů vytvořenou příkazem `npm run export:web` (včetně manifestu).

## Koncept nelze uložit

- „Nelze otevřít IndexedDB“, „Používá se v jiné kartě“: příčinou je anonymní režim prohlížeče nebo jiná karta, ve které je otevřen stejný web. Otevřete web v běžném okně a zavřete ostatní karty.
- Koncepty se ukládají zvlášť pro každé zařízení a prohlížeč. Na jiné zařízení se nepřenášejí.

## Související témata

- [Otevření úložiště na GitHubu](../06-web/open-repository.md)
- [Uložení konceptu](../06-web/drafts.md)
