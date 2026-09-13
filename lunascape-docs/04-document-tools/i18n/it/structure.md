# Radici della documentazione e convenzioni per i file

Le regole che Lunascape Docs segue per trovare i documenti e comporre l'INDEX. Il file system è di per sé la fonte autorevole, quindi non serve alcun registro né configurazione di build.

## Radice della documentazione

- La cartella `docs` più vicina, oppure una cartella che contiene `lunascape-docs.json`, diventa la radice della documentazione.
- Con un `lunascape-docs.json`, la cartella non deve necessariamente chiamarsi `docs`.
- Aprire un file Markdown che non appartiene ad alcuna radice della documentazione mostra la sua cartella come radice della documentazione temporanea.

## File mostrati nell'INDEX

- Vengono mostrati i file `.md`, `.markdown` e `.mdx`. I nuovi file compaiono sempre, anche senza front matter o informazioni di navigazione.
- Le cartelle che iniziano con `.`, `node_modules` e le cartelle indicate in `ignoredDirectories` (per impostazione predefinita `99-archive`) non vengono mostrate.
- Tutto ciò che si trova sotto `i18n/` è trattato come traduzione e non è elencato separatamente nell'INDEX.

## Copertina della cartella

- Un `README.md` (o `index.md` in assenza di README) con corpo di testo è la copertina della sua cartella. Premendo il nome della cartella nell'INDEX si apre la copertina.
- Un `README.md` composto solo dal front matter, senza corpo, è un «descrittore di sola configurazione» e non viene mostrato come pagina. Usalo quando una cartella deve avere solo un titolo o un ordine.
- Quando esistono sia `README.md` sia `index.md`, ha la precedenza `README.md`.

## Lingua predefinita e traduzioni

- I documenti nella lingua predefinita (canonici) restano al loro posto.
- Una traduzione va in una cartella `i18n/<lingua>/` accanto al documento, con lo stesso nome di file. Ricreare la struttura delle cartelle sotto `i18n/` non viene riconosciuto.
- Questa è l'unica posizione da cui una traduzione viene risolta. Lo stesso file collocato altrove è un file isolato che nessun documento rivendica come propria traduzione.

```text
docs/
  lunascape-docs.json
  README.md                  ← copertina della radice (pagina iniziale)
  i18n/en/README.md          ← la sua versione inglese
  01-product/
    README.md                ← copertina della cartella
    requirements.md
    i18n/en/README.md        ← le versioni inglesi dei due documenti sopra
    i18n/en/requirements.md
  99-archive/                ← esclusa dall'INDEX per impostazione predefinita
```

## Informazioni su `_meta.json`

Il `_meta.json` di Nextra non viene usato per la navigazione. I file esistenti non vengono né modificati né eliminati. In futuro solo una funzione esplicita di importazione/esportazione se ne occuperà.

## Argomenti correlati

- [Impostare le informazioni di navigazione](navigation-metadata.md)
- [Configurazione del progetto](project-configuration.md)
- [Cambiare radice della documentazione](../02-reading/roots.md)
