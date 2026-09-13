# Ce este Lunascape Docs

Lunascape Docs este un instrument care tratează documentele Markdown aflate într-un depozit Git direct ca pe un „site de specificații”. Nu sunt necesare o etapă de compilare, un server de documentație sau o bază de date dedicată.

## Ce puteți face

| Scop | Funcții principale |
|---|---|
| Citire | INDEX (cuprins), linkuri în text, fir de navigare, Înapoi/Înainte, cuprinsul paginii, căutare cu filtrare |
| Vizualizare | Tabele, blocuri de cod, încadrarea automată a imaginilor, formule matematice KaTeX, diagrame Mermaid, Vega-Lite, Markmap, WaveDrom și Svgbob, afișarea pliată a tabelelor de gestiune a documentelor |
| Scriere | Comutarea între editarea vizuală și editarea sursei Markdown; creare, duplicare, redenumire și reordonare din INDEX |
| Verificare | Verificarea documentelor cu docs-lint, confirmarea documentelor, capitolelor și termenilor obligatorii pe baza unui Standard Pack, creare din șabloane |
| Traducere | Generarea de propuneri de traducere pentru o singură pagină sau în bloc. Salvare după verificare <!-- ai-only --> |
| Utilizare din AI | Un instrument de specificații, doar pentru citire, pe care îl pot consulta agenții din VS Code <!-- ai-only --> |

## Medii disponibile

| Mediu | Utilizare |
|---|---|
| Extensie VS Code | Consultarea, editarea, verificarea și traducerea depozitului de pe calculatorul dumneavoastră. Acest ajutor se concentrează pe el |
| Versiunea pentru browser web | Consultarea documentelor de pe GitHub (publice sau private), ciorne păstrate pe dispozitiv, consultarea unui folder local |
| Extensie Chromium | Deschide versiunea pentru browser web într-o filă a browserului |
| Browserul Lunascape | Va integra același model de documente |

## Principii de bază

- **Markdown este sursa de referință.** Documentele rămân fișierele Markdown gestionate de Git. Lunascape Docs nu le convertește și nu păstrează o copie într-un alt format.
- **Salvarea o faceți dumneavoastră.** Conținutul editat este scris în fișier numai când apăsați [Salvează]. Lunascape Docs nu face automat nici stocarea temporară („staging”), nici comiterea în Git.
- **Documentele sunt prelucrate pe dispozitiv.** Documentele nu sunt trimise în exterior pentru a fi consultate sau editate. Doar la traducere, destinația și conținutul sunt afișate în prealabil, iar trimiterea are loc după aprobarea dumneavoastră.
- **Traducerile se află în `i18n/<limbă>/`.** Documentele în limba implicită rămân la locul lor, iar traducerile se plasează sub aceeași cale relativă, în `i18n/en/` și așa mai departe.
- **AI doar propune.** Propunerile de traducere se salvează după ce verificați diferențele. Documentele nu sunt niciodată rescrise în tăcere. <!-- ai-only -->

## Subiecte conexe

- [Denumirea și rolul elementelor de pe ecran](screen.md)
- [Instalarea extensiei](install.md)
- [Operații de bază](../02-reading/README.md)
