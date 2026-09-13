# Diagramele, formulele matematice sau imaginile nu se afișează

## O figură TikZ apare ca sursă restrânsă

- Extensia distribuită nu include un motor de randare TikZ. Aceasta este afișarea normală.
- În scop de dezvoltare și evaluare, instalați `node-tikzjax` 1.0.5 direct în rădăcina unui spațiu de lucru de încredere și setați `lunascapeDocEditor.tikz.runtime` la `workspace`.
- Versiunea pentru browser web nu randează TikZ.

## Formulele matematice se afișează ca text simplu

- Verificați delimitatorii. Pentru formule în linie: `$...$` sau `\(...\)`; pentru formule separate: `$$...$$` sau `\[...\]`.
- Un `$` aflat în cod în linie sau într-un bloc de cod nu devine formulă.
- Scrierile care par sume de bani, precum `$5 and $10`, nu sunt tratate ca formule.
- Formulele foarte mari sau cu multe expandări de macrocomenzi nu sunt randate dacă depășesc limitele (`maxSize: 50`, `maxExpand: 1000`). Împărțiți-le.

## O diagramă afișează „nu poate fi randată”

- Mesajul de eroare de la Mermaid, Vega-Lite, WaveDrom și altele indică problema de sintaxă. Verificați sursa în ecranul de editare, cu [Markdown].
- Vega-Lite: datele se includ în `data.values` sau `datasets`. Datele de la adrese URL externe și marcajele de tip imagine nu pot fi folosite.
- WaveDrom: scrieți JSON strict. Forma JavaScript (chei fără ghilimele și altele asemenea) nu poate fi folosită.
- Penrose: folosiți doar `@preset set-theory` la început și instrucțiunile permise (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- „SVG-ul generat conține referințe nesigure”, „SVG-ul generat depășește limita”: diagramele care conțin referințe către resurse externe sau care sunt prea mari nu se afișează. Reduceți conținutul sau eliminați referințele.

## O imagine nu se afișează

- Calea imaginii se indică relativ la document. Imaginile aflate în afara rădăcinii documentației nu se afișează.
- Atributul `width` al unui `<img>` acceptă doar o valoare numerică (`width="360"`).

## Diagramele lipsesc de pe site-ul web exportat

Bibliotecile de randare pentru TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob și Penrose se încarcă în momentul afișării. Publicați și folderul `vendor/` împreună cu site-ul exportat.

## Subiecte conexe

- [Scrierea formulelor matematice](../03-editing/math.md)
- [Scrierea diagramelor și a graficelor](../03-editing/diagrams.md)
- [Ajustarea dimensiunii imaginilor](../03-editing/images.md)
