# Pubblicare i propri documenti sul Web

Puoi pubblicare i documenti del tuo repository come sito Web su GitHub Pages o su qualsiasi hosting statico. Esistono due modi. Questa procedura è rivolta agli sviluppatori che possono clonare il repository di Lunascape Docs e usare `npm`.

## Metodo 1: collocare i due file del visualizzatore

Si distribuisce soltanto il visualizzatore (`index.html` e `lsdoc.js`) e i documenti vengono caricati da GitHub. I documenti non fanno parte del sito, quindi il metodo è sicuro anche per i repository privati (i lettori accedono con GitHub).

1. Esegui il comando seguente nel repository di Lunascape Docs.

   ```sh
   npm run build:viewer
   ```

   In `dist/viewer/` vengono generati `index.html` e `lsdoc.js`.
2. Colloca i due file in `docs/` del repository che vuoi pubblicare.
3. Attiva GitHub Pages.

La radice della documentazione da mostrare viene determinata in quest'ordine.

1. L'impostazione `source` all'interno di `index.html`
2. `repository` indicato nel file `lunascape-docs.json` nella stessa cartella
3. La deduzione dall'URL `*.github.io` e dalla struttura dei rami

## Metodo 2: esportare un sito statico che include i documenti

Si esportano insieme il visualizzatore e i file dei documenti e si pubblica il risultato così com'è.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Vengono prodotti il visualizzatore completo, i documenti sotto `docs/`, il file di elenco `lunascape-docs-manifest.json` e `.nojekyll`. Per pubblicare, colloca la cartella di destinazione su S3 o su GitHub Pages. Per un esempio di pubblicazione automatica con GitHub Actions, consulta `examples/workflows/publish-docs-pages.yml` nel repository.

> **Nota**
>
> - **Non esportare i documenti di un repository privato su GitHub Pages.** Al di fuori di Enterprise Cloud, GitHub Pages è consultabile da chiunque. Se ti serve una pubblicazione riservata, usa il metodo 1 e fai accedere i lettori con GitHub.
> - Aprire `index.html` direttamente con `file://` non funziona, perché il browser impedisce il caricamento dei file adiacenti e l'esecuzione dei moduli ES. Per verificare in locale, usa la versione per VS Code oppure un server HTTP.
> - Le librerie di disegno per TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob e Penrose vengono caricate al momento della visualizzazione. Nel sito esportato colloca anche la cartella `vendor/`.

## Argomenti correlati

- [Che cosa puoi fare nella versione Web](README.md)
- [Consultare un repository privato](private-repository.md)
