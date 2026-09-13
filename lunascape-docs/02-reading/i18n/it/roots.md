# Cambiare radice della documentazione

Una radice della documentazione è la cartella di livello più alto di un insieme di documenti. INDEX, i filtri, i controlli e la traduzione funzionano tutti per singola radice della documentazione.

## Come viene individuata una radice della documentazione

Lunascape Docs risale dal file Markdown aperto alle cartelle superiori e usa come radice della documentazione la cartella più vicina che corrisponde a una delle condizioni seguenti.

- Una cartella che contiene `lunascape-docs.json` (il nome della cartella è indifferente)
- Una cartella denominata `docs` (con l'impostazione `lunascapeDocEditor.rootDirectoryNames` è possibile aggiungere altri nomi)

Quando si esegue «Lunascape Docs: Apri il visualizzatore delle specifiche», si apre la radice della documentazione indicata nell'impostazione `lunascapeDocEditor.root` (valore predefinito `docs`).

## Passare a un'altra radice della documentazione

Quando l'area di lavoro contiene più radici della documentazione, il nome della radice all'estrema sinistra della barra degli strumenti diventa un menu a discesa.

1. Premere il nome della radice della documentazione all'estrema sinistra della barra degli strumenti.
2. Scegliere una radice della documentazione dall'elenco.
   Viene visualizzata la pagina iniziale della radice scelta e INDEX cambia di conseguenza.

> **Suggerimento**
>
> I nomi visualizzati nell'elenco sono determinati nell'ordine seguente. Non cambiano se si cambia la lingua dell'interfaccia.
>
> 1. `title` in `lunascape-docs.json`
> 2. `navigation.title` del file `README.md` nella radice, altrimenti il suo H1
> 3. `navigation.title` del file `index.md` nella radice, altrimenti il suo H1
> 4. Il nome della cartella (per una cartella `docs` standard, il nome della cartella che la contiene)

## Aprire un file Markdown esterno a ogni radice della documentazione

Se si apre un file Markdown non contenuto in una radice della documentazione, la cartella in cui si trova il file viene visualizzata come radice della documentazione temporanea. In INDEX compaiono i file Markdown della stessa cartella e delle cartelle sottostanti.

- Premere [Cartella superiore] sulla barra degli strumenti per estendere l'ambito alla cartella superiore all'interno dell'area di lavoro.
- In questa visualizzazione non sono disponibili le impostazioni di lingua del progetto né la traduzione in blocco. Per renderle disponibili, inserire un file `lunascape-docs.json` nella cartella e trasformarla così in una radice della documentazione.

## Aprire sempre una radice della documentazione fissa

Impostando `lunascapeDocEditor.rootMode` su `fixed`, viene sempre aperta la radice della documentazione indicata in `lunascapeDocEditor.root`, qualunque sia il file Markdown che si apre.

## Argomenti correlati

- [Radici della documentazione e convenzioni sui file](../04-document-tools/structure.md)
- [Configurazione del progetto](../04-document-tools/project-configuration.md)
- [Impostazioni di VS Code](../08-reference/settings.md)
