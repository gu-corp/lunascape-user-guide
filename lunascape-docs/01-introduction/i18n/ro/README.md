# Ce este Lunascape Docs

Lunascape Docs este un instrument care tratează documentele Markdown dintr-un depozit Git, așa cum sunt, ca pe un „site de specificații”. Nu aveți nevoie de o compilare prealabilă, de un server de documentație sau de o bază de date dedicată.

## Ce puteți face

| Scop | Funcții principale |
|---|---|
| Citire | INDEX (cuprins), linkuri din text, fir de navigare, Înapoi/Înainte, cuprinsul paginii, căutare cu filtrare |
| Vizualizare | Tabele, blocuri de cod, imagini ajustate automat, formule matematice KaTeX, diagrame Mermaid/Vega-Lite/Markmap/WaveDrom/Svgbob, afișarea restrânsă a tabelelor de control al documentului |
| Scriere | Comutarea între editarea vizuală și editarea sursei Markdown; crearea, duplicarea, redenumirea și reordonarea din INDEX |
| Verificare | Verificarea documentelor cu docs-lint; verificarea documentelor, capitolelor și termenilor obligatorii conform Standard Pack; crearea din șabloane |
| Traducere | Generarea propunerilor de traducere pentru o pagină sau în lot. Salvarea după ce le verificați <!-- ai-only --> |
| Utilizare de către AI | Un instrument de specificații, doar pentru citire, pe care îl pot consulta agenții din VS Code <!-- ai-only --> |

## Unde îl puteți folosi

| Mediu | Utilizare |
|---|---|
| Extensia pentru VS Code | Citirea, editarea, verificarea și traducerea depozitului de pe computer. Acest ajutor se concentrează pe ea |
| Versiunea pentru browser web | Citirea documentelor de pe GitHub (publice sau private), ciorne păstrate pe dispozitiv, citirea unui folder local |
| Extensia pentru Chromium | Deschide versiunea pentru browser web într-o filă a browserului |

## Principii de bază

- **Markdown este forma canonică.** Documentele rămân fișiere Markdown gestionate cu Git. Lunascape Docs nu le convertește și nu le păstrează în alt format.
- **Dumneavoastră decideți când salvați.** Modificările sunt scrise în fișier numai când apăsați [Salvează]. Staging-ul și commit-ul în Git nu se fac automat.
- **Documentele sunt procesate pe dispozitivul dumneavoastră.** Pentru citire sau editare, documentele nu sunt trimise nicăieri. Doar la traducere, destinația și conținutul sunt afișate în prealabil, iar documentul este trimis numai după aprobarea dumneavoastră.
- **Traducerile se află sub `i18n/<limbă>/`.** Documentele în limba implicită rămân la locul lor, iar traducerile se pun la aceeași cale relativă, sub `i18n/en/` și așa mai departe.
- **AI-ul doar propune.** Propunerile de traducere se salvează după ce verificați diferențele. Documentele nu sunt niciodată rescrise fără știrea dumneavoastră. <!-- ai-only -->

## Subiecte conexe

- [Denumirea și rolul elementelor ecranului](screen.md)
- [Instalarea extensiei](install.md)
- [Operații de bază](../02-reading/README.md)
