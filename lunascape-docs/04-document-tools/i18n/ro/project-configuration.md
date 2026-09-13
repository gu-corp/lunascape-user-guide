# Configurarea proiectului

Fișierul `lunascape-docs.json` aflat direct sub rădăcina documentației conține setările rădăcinii documentației, partajate în echipă. Este gestionat în Git.

## Crearea și editarea fișierului de configurare

- Apăsați [Instrumente pentru documente] din bara de instrumente → fila [Verificare] → [Sursa regulilor și setările documentelor] → [Editează setările documentelor]; fișierul se deschide în VS Code. Dacă fișierul nu există, în acel moment se creează un fișier inițial.
- Numelui de fișier `lunascape-docs.json` i se asociază automat schema JSON Schema inclusă, care oferă completare automată și o descriere pentru fiecare câmp. Nu este nevoie de o intrare `$schema`.

## Exemplu de configurare

```json
{
  "id": "product-docs",
  "title": "Documentația produsului",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Descrierea câmpurilor

| Câmp | Conținut | Implicit |
|---|---|---|
| `id` | Cheia sub care se salvează setările de afișare ale fiecărui utilizator. Stabiliți un ID fix atunci când doriți ca setările să se păstreze după mutarea folderului | Calea folderului |
| `title` | Numele afișat în extrema stângă a barei de instrumente și în lista rădăcinilor documentației. Nu se schimbă odată cu limba interfeței | Titlul din README/index al rădăcinii, iar în lipsa acestuia numele folderului |
| `indexTitle` | Titlul panoului INDEX | `INDEX` |
| `startPage` | Documentul deschis primul (cale relativă la rădăcina documentației) | `README.md` |
| `appearance` | Schema de culori: `light` (mereu luminoasă) sau `auto` (urmează tema din VS Code) | `light` |
| `defaultLocale` | Limba implicită (limba documentelor canonice). Se indică printr-o etichetă de limbă BCP 47 (`ja`, `en`, `zh-Hant` etc.). Este sursa traducerii | Nesetat (se deduce din text doar pentru afișare) |
| `fallbackLocale` | Limba arătată prima cititorilor a căror limbă a mediului de consultare nu corespunde niciuneia dintre limbile acceptate. Indicați o limbă cuprinsă în `locales` | Nesetat (se folosește `defaultLocale`) |
| `locales` | Lista limbilor acceptate, inclusiv `defaultLocale`. Apar în meniul de limbi și sunt limbile-țintă ale traducerii | Doar `defaultLocale` |
| `ignoredDirectories` | Numele folderelor excluse din INDEX, din căutare și din verificări. Dacă este indicat, înlocuiește valoarea implicită | `["99-archive"]` |
| `tree` | Valorile implicite pentru afișarea panoului INDEX. Utilizatorii le pot suprascrie din setările de afișare | Ca în exemplul de mai sus |
| `editor.defaultMode` | Modul de editare folosit până când utilizatorul comută: `visual` sau `source` | `visual` |
| `editor.showEditButton` | Dacă se afișează [Editează] în dreapta jos a documentului | `true` |
| `documentStandards.pack` | Standard Pack folosit pentru verificarea documentelor și pentru șabloane: `builtin:<nume>` sau o cale relativă la rădăcina documentației | Niciunul |
| `documentStandards.profile` | Numele unui profil definit de pachet | Niciunul |
| `translation.enabled` | Activează crearea propunerilor de traducere și traducerea în bloc | `true` |
| `translation.contextFiles` | Fișiere Markdown canonice (cale relativă la rădăcina documentației) transmise la traducere ca referință pentru terminologie și stil | `[]` |
| `translation.maxContextCharacters` | Limita superioară a numărului total de caractere din documentele de referință (maximum 1048576) | `49152` |
| `description` | O descriere de un rând a setului de documente. Se afișează pe cardurile paginii principale a depozitului. La fel ca `title`, se poate scrie ca șir de caractere sau ca obiect pe limbi | Niciuna |

## Indicarea locului în care se află documentele din depozit

Un fișier `lunascape-docs.json` aflat direct sub depozit poate conține nu setările acelui folder, ci o **hartă a depozitului**. Dacă scrieți oricare dintre următoarele trei câmpuri, fișierul devine o hartă, iar folderul respectiv nu mai este el însuși o rădăcină a documentației.

| Câmp | Conținut | Implicit |
|---|---|---|
| `defaultFolder` | Folderul în care se află documentele (cale relativă la acest folder). Folderul indicat nu are nevoie de un fișier de configurare propriu | Niciunul (se folosește `docs`) |
| `roots` | Lista seturilor de documente, atunci când există mai multe (căi relative la acest folder, în ordinea afișării). În acest caz, folderul devine pagina principală | Niciunul |
| `excludes` | Folderele excluse de la descoperirea rădăcinilor documentației (căi relative la acest folder). Se adaugă la excluderile implicite, precum `node_modules` | `[]` |
| `home.cards` | Dacă pagina principală afișează cardurile seturilor de documente sub README-ul său. Setați `false` dacă scrieți singur legăturile în README | `true` |

Rădăcina documentației se stabilește în ordinea următoare. Se folosește prima găsită, de sus în jos.

1. Folderul indicat printr-o setare sau prin comanda executată
2. Ținta indicată de `defaultFolder` sau `roots` din fișierul `lunascape-docs.json` aflat direct sub depozit
3. Folderul care conține un fișier `lunascape-docs.json` (dacă există două sau mai multe sub un părinte comun, acel părinte devine pagina principală)
4. Folderul `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. Nivelul de sus al depozitului însuși

> **Sfat**
>
> Dacă nu scrieți nimic, se aplică punctul 4, așa că un depozit obișnuit cu un singur folder `docs/` se comportă exact ca până acum. Scrieți `defaultFolder` numai când folderul se numește altfel, de exemplu `manual`.

### Exemplu de hartă

```json
{
  "title": "Ajutor Lunascape",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Ordinea de prioritate a setărilor

Câmpurile privitoare la afișare se aplică în ordinea următoare.

1. Setările de afișare ale utilizatorului (panoul [Setări de afișare])
2. Setările din VS Code (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Valorile implicite ale produsului

Singura excepție o fac limbile (`defaultLocale`, `fallbackLocale`, `locales`): aici `lunascape-docs.json` are întâietate. Setările personale din VS Code nu pot suprascrie limbile proiectului.

> **Notă**
>
> Un Standard Pack poate fi indicat și ca `standard` în `docs-lint.config.json`. Dacă este prezent în ambele locuri, are prioritate `docs-lint.config.json`.

## Subiecte conexe

- [Modificarea regulilor de verificare](rules.md)
- [Modificarea setărilor de afișare](../02-reading/display-settings.md)
- [Lista setărilor VS Code](../08-reference/settings.md)
