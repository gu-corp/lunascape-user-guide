# Diagrammi, formule o immagini non vengono visualizzati

## Una figura TikZ appare come sorgente ripiegato

- L'estensione distribuita non include il motore di disegno TikZ. Questa visualizzazione è normale.
- A scopo di sviluppo e valutazione, installare `node-tikzjax` 1.0.5 direttamente nella radice di un'area di lavoro attendibile e impostare `lunascapeDocEditor.tikz.runtime` su `workspace`: il disegno viene generato.
- Nella versione per browser Web TikZ non viene disegnato.

## Le formule restano visualizzate come testo

- Controllare i delimitatori: `$...$` oppure `\(...\)` per le formule in linea, `$$...$$` oppure `\[...\]` per le formule isolate.
- Un `$` all'interno di codice in linea o di un blocco di codice non diventa una formula.
- Una scrittura che sembra un importo, come `$5 and $10`, non viene trattata come formula.
- Le formule molto grandi o con molte espansioni di macro non vengono disegnate se superano i limiti (`maxSize: 50`, `maxExpand: 1000`). Suddividerle.

## Un diagramma indica che non può essere disegnato

- I messaggi di errore di Mermaid, Vega-Lite, WaveDrom e altri indicano il problema di sintassi. Controllare il sorgente nella schermata di modifica con [Markdown].
- Vega-Lite: incorporare i dati in `data.values` o `datasets`. Non è possibile usare dati da URL esterni né marcatori immagine.
- WaveDrom: scrivere in JSON rigoroso. Il formato JavaScript (chiavi senza virgolette e simili) non è utilizzabile.
- Penrose: usare solo `@preset set-theory` all'inizio e le istruzioni consentite (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- «L'SVG generato contiene riferimenti non sicuri» / «L'SVG generato supera il limite»: i diagrammi che fanno riferimento a risorse esterne, o troppo grandi, non vengono visualizzati. Ridurre il contenuto o rimuovere i riferimenti.

## Un'immagine non viene visualizzata

- I percorsi delle immagini si indicano come percorsi relativi al documento. Le immagini che si trovano fuori dalla radice della documentazione non vengono visualizzate.
- Per `width` di `<img>` indicare solo un numero (`width="360"`).

## I diagrammi non compaiono nel sito Web esportato

Le librerie di disegno di TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob e Penrose vengono caricate al momento della visualizzazione. Collocare anche la cartella `vendor/` insieme al sito esportato.

## Argomenti correlati

- [Scrivere formule](../03-editing/math.md)
- [Scrivere diagrammi e grafici](../03-editing/diagrams.md)
- [Regolare la dimensione delle immagini](../03-editing/images.md)
