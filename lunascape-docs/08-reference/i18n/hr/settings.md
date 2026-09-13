# Postavke za VS Code

U postavkama VS Codea (`⌘,` / `Ctrl+,`) potražite „Lunascape Docs” da biste promijenili sljedeće stavke. Sve su to korisničke postavke i ne spremaju se u dokumente projekta.

## Korijen dokumentacije

| Postavka | Vrijednosti | Zadano | Funkcija |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` automatski odabire korijen dokumentacije najbliži otvorenoj Markdown datoteci, a ako datoteka ne pripada nijednom, privremeno otvara nadređenu mapu. `fixed` uvijek otvara korijen dokumentacije naveden u `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Niz nizova znakova | `["docs"]` | Nazivi mapa koje se u načinu `auto` automatski prepoznaju kao korijen dokumentacije. Mapa s datotekom `lunascape-docs.json` prepoznaje se bez obzira na naziv. Ako datoteka `lunascape-docs.json` u korijenu repozitorija sadrži `defaultFolder` ili `roots`, prednost ima to |
| `lunascapeDocEditor.root` | Putanja | `docs` | Korijen dokumentacije relativan u odnosu na radni prostor, za način `fixed` i za otvaranje naredbom |
| `lunascapeDocEditor.startPage` | Putanja | `README.md` | Početna stranica relativna u odnosu na korijen dokumentacije |
| `lunascapeDocEditor.title` | Niz znakova | `Lunascape Docs` | Zamjenjuje naslov kartice dokumenta. Ne utječe na naziv odabranog korijena dokumentacije |
| `lunascapeDocEditor.ignoredDirectories` | Niz nizova znakova | `["99-archive"]` | Nazivi mapa isključenih iz INDEX‑a |

## Prikaz

| Postavka | Vrijednosti | Zadano | Funkcija |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` koristi bijelu pozadinu, a `auto` prati boje VS Codea |
| `lunascapeDocEditor.locale` | Oznaka jezika | Nema | Vaš osobni jezik dokumenta, koji ima prednost kada je dostupan. Ne mijenja jezik izvornika u projektu |
| `lunascapeDocEditor.documentMetadata.compact` | Booleova vrijednost | `true` | Sažima tablicu za upravljanje dokumentom nakon naslova H1 u redak „Podaci o dokumentu” |
| `lunascapeDocEditor.tree.showFileNames` | Booleova vrijednost | `false` | U INDEX‑u prikazuje nazive datoteka umjesto naziva dokumenata |
| `lunascapeDocEditor.tree.showDocumentIcons` | Booleova vrijednost | `false` | U INDEX‑u prikazuje ikone dokumenata |
| `lunascapeDocEditor.tree.showFolderIcons` | Booleova vrijednost | `false` | U INDEX‑u prikazuje ikone mapa |
| `lunascapeDocEditor.tree.showItemCounts` | Booleova vrijednost | `false` | U INDEX‑u prikazuje broj stavki neposredno unutar mape |
| `lunascapeDocEditor.tree.showGuides` | Booleova vrijednost | `true` | U INDEX‑u prikazuje linije vodilje za razine |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Razmak redaka u INDEX‑u |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Booleova vrijednost | `true` | Kada postoji samo jedan dokument, zatvara INDEX samo prvi put |

## Uređivanje

| Postavka | Vrijednosti | Zadano | Funkcija |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Prikaz za uređivanje dok ga još niste promijenili. Prednost ima posljednji upotrijebljeni prikaz |
| `lunascapeDocEditor.editor.showEditButton` | Booleova vrijednost | `true` | Prikazuje [Uredi] u donjem desnom kutu teksta |

## Dijagrami

| Postavka | Vrijednosti | Zadano | Funkcija |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Izvršno okruženje za crtanje TikZ‑a. `bundled` koristi priloženo odobreno izvršno okruženje (nije uključeno u trenutačnu distribuciju), `workspace` koristi `node-tikzjax` 1.0.5 u korijenu pouzdanog radnog prostora (samo za razvoj i vrednovanje), a `disabled` ne crta ništa |

## Zastarjele postavke

| Postavka | Upotrijebite umjesto toga |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` u datoteci `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` u datoteci `lunascape-docs.json` |

Osobnim postavkama ne možete zamijeniti jezike projekta.

## Povezane teme

- [Promjena postavki prikaza](../02-reading/display-settings.md)
- [Konfiguracija projekta](../04-document-tools/project-configuration.md)
