# Documentele nu apar

## Apare „Nu s-a găsit niciun fișier Markdown sau folder docs care să poată fi deschis”

- Spațiul de lucru nu are un folder `docs` sau folosește un nume diferit de `docs`.
  - Dacă puneți un fișier `lunascape-docs.json` în acel folder, acesta este recunoscut ca rădăcina documentației, indiferent de nume.
  - Sau adăugați numele folderului în setarea `lunascapeDocEditor.rootDirectoryNames`.
- Dacă nu există încă documente, creați-le cu „Lunascape Docs: Creează documentație dintr-un șablon”.
- Există și varianta de a deschide un fișier Markdown în editor și de a executa „Lunascape Docs: Deschide în vizualizatorul de specificații”.

## Un document nu apare în INDEX

- Verificați ca extensia să fie `.md`, `.markdown` sau `.mdx`.
- Următoarele foldere nu sunt afișate: folderele care încep cu `.`, `node_modules` și folderele indicate în `ignoredDirectories` (implicit `99-archive`).
- Traducerile aflate sub `i18n/` nu apar separat în INDEX. Treceți la ele din meniul de limbi.
- Dacă un fișier tocmai adăugat nu apare, apăsați [Reîncarcă].
- Este posibil să priviți o altă rădăcină a documentației. Verificați numele rădăcinii din extrema stângă a barei de instrumente.

## Apăs un folder și nu se afișează nimic

Fișierul `README.md` al acelui folder este un „descriptor exclusiv pentru configurare”, care are doar front matter, fără text. Deschideți folderul în INDEX și alegeți un document din el.

## Se deschide o rădăcină a documentației nedorită

- Dacă setarea `lunascapeDocEditor.rootMode` este `fixed`, se deschide întotdeauna `lunascapeDocEditor.root`.
- Cu `auto`, este aleasă rădăcina documentației cea mai apropiată de fișierul Markdown deschis. Puteți schimba din lista derulantă aflată în extrema stângă a barei de instrumente.

## Numele rădăcinii documentației este altul decât cel așteptat

Numele este stabilit în ordinea: `title` din `lunascape-docs.json` → `navigation.title` din `README.md` al rădăcinii → titlul H1 al acestuia → `index.md` → numele folderului. Dacă doriți să îl fixați, configurați `title`.

## INDEX a dispărut

- Într-o rădăcină a documentației cu un singur document, INDEX se închide automat doar prima dată. Îl puteți deschide cu pictograma de afișare pe coloane din bara de instrumente. Puteți dezactiva comportamentul din [Setări de afișare], cu [Ascunde automat dacă există un singur document].
- Când ecranul este îngust, deschideți-l din [Deschide INDEX] (cele trei linii), aflat la stânga butonului [Înapoi].

## Apăs pe o legătură și nu se deschide

- „Ținta legăturii nu a fost găsită”: fișierul indicat nu există. Puteți verifica legăturile interne cu [Verificare] din Instrumente pentru documente.
- „O legătură nesigură sau neacceptată nu a fost deschisă”: legăturile din afara rădăcinii documentației sau către alte scheme decât `https://` și `mailto:` nu se deschid.

## Limba afișată este alta decât cea dorită

- În meniul de limbi, verificați limba paginii afișate și motivul alegerii ei.
- Limba interfeței aleasă ultima dată este memorată. Alegeți din nou limba implicită din meniul de limbi.
- Dacă setarea personală `lunascapeDocEditor.locale` este configurată, are prioritate traducerea în acea limbă.

## Subiecte conexe

- [Schimbarea rădăcinii documentației](../02-reading/roots.md)
- [Rădăcina documentației și convențiile de fișiere](../04-document-tools/structure.md)
