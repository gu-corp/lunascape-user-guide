# Securitatea și limitele de scriere

Limitele pe care Lunascape Docs le menține pentru a vă proteja documentele și dispozitivul.

## Afișare

- Codul HTML generat din Markdown și fișierele SVG generate din diagrame sunt igienizate cu DOMPurify 3.4.14 înainte de afișare.
- Scripturile arbitrare din MDX nu sunt niciodată executate.
- KaTeX rulează cu `trust: false`, `maxSize: 50` și `maxExpand: 1000` și nu are încredere nici în codul HTML extern, nici în comenzile arbitrare.
- Bibliotecile de randare Markmap, WaveDrom, Svgbob, Vega-Lite și Penrose se încarcă local, în versiuni fixate, numai atunci când există blocul corespunzător. Referințele la resurse externe, codul HTML brut și notațiile executabile nu sunt permise, iar scripturile, imaginile externe, `link`, `style` și `foreignObject` sunt eliminate din fișierele SVG generate.
- Randarea TikZ nu pornește niciodată programul LaTeX al gazdei. Ea rulează secvențial într-un proces de lucru TeX în WebAssembly, cu un sistem de fișiere în memorie, cu limite pentru date de intrare, coada de așteptare, memorie, timp de execuție (15 secunde) și ieșirea SVG, și respinge instrucțiunile de intrare/ieșire pentru fișiere.

## Accesul la documente și fișiere

- Legăturile dintre documente și operațiile cu fișiere nu pot ieși din rădăcina documentației.
- Crearea, redenumirea, mutarea și ștergerea din INDEX sunt verificate din nou de extensie — rădăcina documentației, versiunea INDEX, calea documentului canonic, tipul elementului vizat, limitele legăturilor simbolice și documentele nesalvate — înainte de a fi aplicate. Cererile venite dintr-un meniu învechit sau din altă rădăcină a documentației nu sunt aplicate.
- Modificările din INDEX sunt dezactivate cât timp un document este în curs de editare sau cât timp se aplică o altă operație din INDEX.
- Crearea dintr-un șablon verifică din nou, după previzualizare, încrederea în spațiul de lucru, identitatea rădăcinii documentației, versiunea INDEX, Standard Pack și conținutul generat, destinația și limitele legăturilor simbolice. Nu suprascrie niciodată un fișier existent și nu creează niciodată conținut diferit de previzualizare sau un rezultat mai mare de 4 MiB.
- Salvarea unui fișier de configurare îi verifică versiunea imediat înainte și se oprește atunci când este detectată o modificare externă.

## Trimiterea către exterior

- Documentele nu sunt trimise niciodată în exterior pentru citire, editare sau verificare. Verificările documentelor rulează local și determinist.
- Numai traducerea (a paginii curente sau în bloc) trimite documente către un model lingvistic, după ce afișează destinația și domeniul de aplicare și numai cu aprobare explicită. <!-- ai-only -->
- Propunerile de traducere sunt prezentate ca diferențe, versiunile documentului canonic și ale celui tradus sunt verificate din nou, iar o propunere este aplicată numai atunci când o persoană o salvează în mod explicit. <!-- ai-only -->
- Instrumentul de specificație pentru agenții AI nu returnează conținutul documentelor, numele spațiilor de lucru sau căile locale. <!-- ai-only -->

## Git

- Salvarea doar scrie fișierul. Nicio funcție nu face automat pregătirea pentru comitere („staging”) sau comiterea în Git.
- Fișierele existente, precum `_meta.json`, nu sunt niciodată șterse sau modificate în tăcere. Traducerile rămase fără document canonic nu sunt niciodată șterse sau mutate automat.

## Subiecte conexe

- [Specificații](README.md)
- [Utilizarea din agenți AI](ai-agents.md)
