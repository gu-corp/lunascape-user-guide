# Che cos'è Lunascape Docs

Lunascape Docs è uno strumento che tratta i documenti Markdown contenuti in un repository Git direttamente come un «sito di specifiche». Non servono una compilazione preliminare, un server di documentazione né un database dedicato.

## Che cosa si può fare

| Scopo | Funzioni principali |
|---|---|
| Leggere | INDEX (sommario), collegamenti nel testo, percorso di navigazione, Indietro e Avanti, sommario della pagina, ricerca con filtro |
| Visualizzare | Tabelle, blocchi di codice, adattamento automatico delle immagini, formule KaTeX, diagrammi Mermaid, Vega-Lite, Markmap, WaveDrom e Svgbob, tabelle di gestione del documento in forma compressa |
| Scrivere | Passaggio tra modifica visiva e modifica del sorgente Markdown; creazione, duplicazione, ridenominazione e riordino dall'INDEX |
| Verificare | Controllo dei documenti con docs-lint, verifica di documenti, capitoli e termini obbligatori in base allo Standard Pack, creazione da modelli |
| Tradurre | Generazione di proposte di traduzione per singola pagina o in blocco. Si salvano dopo averle verificate <!-- ai-only --> |
| Usare dall'AI | Uno strumento di specifica di sola lettura che gli agenti di VS Code possono consultare <!-- ai-only --> |

## Ambienti disponibili

| Ambiente | Uso |
|---|---|
| Estensione per VS Code | Lettura, modifica, controllo e traduzione del repository sulla propria macchina. È al centro di questa guida |
| Versione per browser web | Lettura dei documenti su GitHub (pubblici o privati), bozze sul dispositivo, lettura di una cartella locale |
| Estensione per Chromium | Apre la versione per browser web in una scheda del browser |
| Browser Lunascape | È previsto che integri lo stesso modello di documento |

## Principi di base

- **Il Markdown è il documento canonico.** I documenti restano i file Markdown gestiti con Git. Lunascape Docs non li converte né ne conserva una copia in un altro formato.
- **Il salvataggio spetta all'utente.** Le modifiche vengono scritte nel file solo quando si preme [Salva]. Lo staging e il commit in Git non avvengono mai automaticamente.
- **I documenti vengono elaborati sul dispositivo.** Per leggere o modificare un documento non viene inviato nulla all'esterno. Solo per la traduzione il documento viene inviato, dopo aver mostrato in anticipo la destinazione e il contenuto e ottenuto l'approvazione.
- **Le traduzioni si trovano in `i18n/<lingua>/`.** I documenti nella lingua predefinita restano al loro posto; le traduzioni usano lo stesso percorso relativo sotto `i18n/en/` e simili.
- **L'AI si limita a proporre.** Le proposte di traduzione si salvano dopo aver verificato le differenze. I documenti non vengono mai riscritti in silenzio. <!-- ai-only -->

## Argomenti correlati

- [Nome e funzione delle parti dello schermo](screen.md)
- [Installare l'estensione](install.md)
- [Operazioni di base](../02-reading/README.md)
