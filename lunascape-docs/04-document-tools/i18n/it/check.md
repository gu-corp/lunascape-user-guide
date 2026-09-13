# Controllare i documenti

Con docs-lint è possibile verificare la struttura dei titoli, i collegamenti interrotti, l'assenza di documenti o capitoli obbligatori, le incoerenze terminologiche e la corrispondenza degli ID dei requisiti. Il controllo riguarda sempre l'intera radice della documentazione.

## Eseguire un controllo

1. Nella barra degli strumenti premere [Strumenti documento] e aprire la scheda [Controllo].
2. Premere [Controlla la radice della documentazione].
   Il controllo si può avviare anche con «Lunascape Docs: Controlla la radice della documentazione» dalla palette dei comandi.
3. Esaminare l'elenco dei risultati.

## Leggere i risultati

- Con [Questo documento] / [Tutti], sopra l'elenco, si cambia l'ambito di ciò che viene mostrato. L'ambito del controllo resta comunque l'intera radice della documentazione.
- Le segnalazioni hanno quattro livelli: «errore», «avviso», «informazione» e «suggerimento». In [Strumenti documento], nella barra degli strumenti, è indicato il numero di errori e di avvisi.
- Premendo una segnalazione si apre, nell'editor di VS Code, il punto corrispondente del sorgente Markdown.
- Le segnalazioni che riguardano l'intera radice della documentazione (per esempio un documento di test mancante) compaiono come voci «intera radice della documentazione» e non hanno una posizione.
- Le stesse segnalazioni compaiono anche nel pannello «Problemi» di VS Code.

## Elementi controllati

Premendo [Rivedi e modifica le regole] si apre l'elenco dei controlli attivi con lo scopo di ciascuno. I principali sono i seguenti.

| Elemento | Contenuto |
|---|---|
| Struttura dei titoli | Verifica che ci sia un solo H1 e che i livelli dei titoli non saltino |
| Collegamenti interni | Verifica che i documenti collegati esistano e non escano dalla radice della documentazione |
| Linguaggio dei blocchi di codice | Verifica che nei blocchi di codice sia indicato il nome del linguaggio |
| Cartelle e documenti necessari | Verifica che siano presenti le cartelle e i documenti richiesti dal profilo dello Standard Pack |
| Capitoli necessari nel documento | Verifica che ogni tipo di documento abbia i capitoli richiesti |
| Uniformità terminologica | Rileva le espressioni da evitare e invita a uniformarsi ai termini consigliati |
| Denominazione e duplicati degli ID dei requisiti | Verifica che gli ID dei requisiti seguano la regola di denominazione e non siano definiti due volte |
| Coerenza dei riferimenti agli ID dei requisiti | Verifica che gli ID dei requisiti citati da progettazione, test e tabelle di stato esistano davvero |
| Corrispondenza tra requisiti e test | Verifica che gli ID dei requisiti siano citati nei documenti di test |

Gli elementi attivi dipendono dallo Standard Pack e dal profilo scelti in `lunascape-docs.json` e da `docs-lint.config.json`.

> **Nota**
>
> - Quando si modifica un documento o un'impostazione, il risultato precedente passa allo stato «da riverificare». Nulla viene considerato superato automaticamente: premere di nuovo [Controlla la radice della documentazione].
> - Le modifiche non salvate non rientrano nel controllo. Salvare prima di procedere.
> - Il controllo viene eseguito in locale e in modo deterministico. I risultati delle valutazioni dell'AI e delle traduzioni non si mescolano mai ai risultati del controllo.

## Argomenti correlati

- [Modificare le regole di controllo](rules.md)
- [Configurazione del progetto](project-configuration.md)
- [Controllo, creazione o traduzione non funzionano](../07-troubleshooting/tools.md)
