# I documenti non vengono visualizzati

## Viene mostrato «Nessuna cartella Markdown o docs da aprire»

- L'area di lavoro non ha una cartella `docs`, oppure usa un nome diverso.
  - Inserisci un file `lunascape-docs.json` in quella cartella: verrà riconosciuta come radice della documentazione indipendentemente dal nome.
  - In alternativa, aggiungi il nome della cartella all'impostazione `lunascapeDocEditor.rootDirectoryNames`.
- Se non ci sono ancora documenti, creali con «Lunascape Docs: Crea documentazione da modello».
- Puoi anche aprire un file Markdown nell'editor ed eseguire «Lunascape Docs: Apri nel visualizzatore di specifiche».

## Un documento non compare nell'INDEX

- Verifica che l'estensione sia `.md`, `.markdown` o `.mdx`.
- Le cartelle seguenti non vengono mostrate: le cartelle che iniziano con `.`, `node_modules` e le cartelle indicate in `ignoredDirectories` (per impostazione predefinita `99-archive`).
- Le traduzioni che si trovano sotto `i18n/` non compaiono singolarmente nell'INDEX. Passa a esse dal menu delle lingue.
- Se un file appena aggiunto non compare, premi [Ricarica].
- Potresti stare guardando un'altra radice della documentazione. Controlla il nome della radice all'estrema sinistra della barra degli strumenti.

## Premendo una cartella non viene mostrato nulla

Il file `README.md` di quella cartella è un «descrittore di sola configurazione», con il front matter ma senza corpo del testo. Apri la cartella nell'INDEX e scegli un documento al suo interno.

## Si apre una radice della documentazione non prevista

- Se l'impostazione `lunascapeDocEditor.rootMode` è `fixed`, si apre sempre la radice indicata in `lunascapeDocEditor.root`.
- Con `auto` viene scelta la radice della documentazione più vicina al file Markdown aperto. Puoi cambiarla con il menu a discesa all'estrema sinistra della barra degli strumenti.

## Il nome della radice della documentazione è diverso da quello previsto

Il nome viene determinato in quest'ordine: `title` in `lunascape-docs.json` → `navigation.title` del `README.md` della radice → il suo H1 → `index.md` → il nome della cartella. Per fissarlo, imposta `title`.

## L'INDEX è scomparso

- In una radice della documentazione con un solo documento, l'INDEX si chiude automaticamente la prima volta. Puoi riaprirlo con l'icona delle colonne nella barra degli strumenti. Puoi disattivare questo comportamento con [Nascondi se c'è un solo documento] in [Impostazioni di visualizzazione].
- Quando lo schermo è stretto, aprilo con [Apri INDEX] (le tre linee) a sinistra di [Indietro].

## Un collegamento non si apre

- «Destinazione del collegamento non trovata»: il file di destinazione non esiste. Puoi verificare i collegamenti interni con [Controllo] negli Strumenti documento.
- «Collegamento non sicuro o non supportato: non è stato aperto»: i collegamenti che puntano fuori dalla radice della documentazione, o a schemi diversi da `https://` e `mailto:`, non vengono aperti.

## Viene mostrata una lingua diversa da quella prevista

- Nel menu delle lingue puoi vedere la lingua della pagina visualizzata e il motivo per cui è stata scelta.
- L'ultima lingua dell'interfaccia scelta viene memorizzata. Seleziona di nuovo la lingua predefinita dal menu delle lingue.
- Se è impostata l'impostazione personale `lunascapeDocEditor.locale`, viene data la precedenza alla traduzione in quella lingua.

## Argomenti correlati

- [Cambiare radice della documentazione](../02-reading/roots.md)
- [Radici della documentazione e convenzioni sui file](../04-document-tools/structure.md)
