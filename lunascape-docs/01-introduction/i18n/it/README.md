# Che cos'è Lunascape Docs

Lunascape Docs è uno strumento che permette di usare i documenti Markdown di un repository Git, così come sono, come un «sito di specifiche». Non servono una build preliminare, un server per la documentazione né un database dedicato.

## Cosa si può fare

| Obiettivo | Funzioni principali |
|---|---|
| Leggere | INDEX (indice), link nel testo, percorso di navigazione, Indietro/Avanti, indice della pagina, ricerca con filtro |
| Visualizzare | Tabelle, blocchi di codice, adattamento automatico delle immagini, formule KaTeX, diagrammi Mermaid, Vega-Lite, Markmap, WaveDrom e Svgbob, visualizzazione compressa delle tabelle di gestione del documento |
| Scrivere | Passaggio tra modifica visuale e modifica del sorgente Markdown; creazione, duplicazione, ridenominazione e riordino dall'INDEX |
| Verificare | Controllo dei documenti con docs-lint, verifica di documenti, capitoli e termini obbligatori in base allo Standard Pack, creazione da modello |
| Tradurre | Generazione di proposte di traduzione per singola pagina o in blocco; salvataggio dopo la revisione <!-- ai-only --> |
| Usare con l'IA | Strumento di specifiche in sola lettura che gli agenti di VS Code possono consultare <!-- ai-only --> |

## Ambienti disponibili

| Ambiente | Uso |
|---|---|
| Estensione per VS Code | Lettura, modifica, controllo e traduzione del repository sul proprio computer. È l'argomento principale di questa guida |
| Versione per browser web | Lettura di documenti su GitHub (pubblici e privati), bozze sul dispositivo, lettura di cartelle locali |
| Estensione per Chromium | Apre la versione per browser web in una scheda del browser |

## Principi di base

- **Il Markdown è il documento canonico.** I documenti restano file Markdown gestiti con Git. Lunascape Docs non li converte né li conserva in un altro formato.
- **Il salvataggio spetta all'utente.** Le modifiche vengono scritte nel file solo quando si preme [Salva]. Lo staging e il commit di Git non vengono mai eseguiti automaticamente.
- **I documenti vengono elaborati sul dispositivo.** Per leggere o modificare un documento non viene inviato nulla all'esterno. Solo per la traduzione, la destinazione e il contenuto vengono mostrati in anticipo e l'invio avviene dopo l'approvazione.
- **Le traduzioni si trovano in `i18n/<lingua>/`.** I documenti nella lingua predefinita restano dove sono; le traduzioni usano lo stesso percorso relativo sotto `i18n/en/` e cartelle simili.
- **L'IA si limita a proporre.** Le proposte di traduzione si salvano dopo aver controllato le differenze. I documenti non vengono mai riscritti senza avviso. <!-- ai-only -->

## Argomenti correlati

- [Nomi e funzioni delle parti dello schermo](screen.md)
- [Installare l'estensione](install.md)
- [Operazioni di base](../02-reading/README.md)
