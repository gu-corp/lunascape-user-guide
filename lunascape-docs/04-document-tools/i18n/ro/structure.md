# Rădăcina documentației și convențiile de fișiere

Regulile după care Lunascape Docs găsește documentele și construiește INDEX. Sistemul de fișiere este el însuși documentul canonic, așadar nu este nevoie de un registru sau de o configurație de compilare.

## Rădăcina documentației

- Cel mai apropiat folder `docs` sau folderul în care ați pus `lunascape-docs.json` devine rădăcina documentației.
- Dacă puneți un `lunascape-docs.json`, folderul nu trebuie să se numească `docs`.
- Când deschideți un fișier Markdown care nu aparține niciunei rădăcini a documentației, folderul acestuia este afișat ca rădăcină temporară a documentației.

## Fișierele afișate în INDEX

- Sunt afișate fișierele `.md`, `.markdown` și `.mdx`. Fișierele noi apar întotdeauna, chiar și fără front matter sau informații de navigare.
- Folderele care încep cu `.`, `node_modules` și folderele indicate în `ignoredDirectories` (implicit `99-archive`) nu sunt afișate.
- Tot ce se află sub `i18n/` este tratat ca traducere și nu este afișat separat în INDEX.

## Pagina de deschidere a unui folder

- Un `README.md` cu conținut (sau `index.md`, dacă nu există README) este pagina de deschidere a folderului respectiv. Când apăsați numele folderului în INDEX, se deschide această pagină.
- Un `README.md` format doar din front matter, fără conținut, este tratat ca „descriptor de configurare” și nu este afișat ca pagină. Folosiți-l când un folder are nevoie doar de un titlu sau de o ordine.
- Când există atât `README.md`, cât și `index.md`, are prioritate `README.md`.

## Limba implicită și traducerile

- Documentele în limba implicită (documentele canonice) rămân la locul lor.
- Traducerea se pune în folderul `i18n/<limbă>/` de lângă document, cu același nume de fișier. Recrearea structurii de foldere sub `i18n/` nu este recunoscută.
- Aceasta este singura locație din care se rezolvă o traducere. Același fișier pus în altă parte rămâne un fișier orfan, pe care niciun document nu îl revendică drept traducere.

```text
docs/
  lunascape-docs.json
  README.md                  ← pagina de deschidere a rădăcinii (pagina de start)
  i18n/en/README.md          ← versiunea în engleză a acesteia
  01-product/
    README.md                ← pagina de deschidere a folderului
    requirements.md
    i18n/en/README.md        ← versiunile în engleză ale celor două documente de mai sus
    i18n/en/requirements.md
  99-archive/                ← exclus implicit din INDEX
```

## Despre `_meta.json`

Fișierul `_meta.json` din Nextra nu este folosit pentru navigare. Fișierele existente nu sunt nici modificate, nici șterse. Pe viitor, acestea vor fi tratate doar printr-o funcție explicită de import/export.

## Subiecte înrudite

- [Setarea informațiilor de navigare](navigation-metadata.md)
- [Configurarea proiectului](project-configuration.md)
- [Comutarea între rădăcinile documentației](../02-reading/roots.md)
