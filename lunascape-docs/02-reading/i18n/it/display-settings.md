# Modificare le impostazioni di visualizzazione

Da [Impostazioni di visualizzazione] (ingranaggio) nella barra degli strumenti, ogni utente può cambiare l'aspetto dell'INDEX e la visualizzazione del pulsante di modifica.

1. Premere [Impostazioni di visualizzazione] nella barra degli strumenti.
2. Attivare o disattivare le voci da modificare. Le modifiche hanno effetto immediato.
3. Premere di nuovo [Impostazioni di visualizzazione], oppure fare clic fuori dal pannello, per chiuderlo.

## Voci configurabili

| Sezione | Voce | Funzione |
|---|---|---|
| Lingua del documento | (stato attuale) | Mostra la lingua predefinita del progetto e la lingua visualizzata. [Imposta le lingue del progetto…] apre le impostazioni delle lingue del progetto |
| Contenuto | [Nomi dei file] | Mostra i nomi dei file invece dei titoli dei documenti |
| | [Icone dei documenti] | Mostra un'icona accanto a ogni documento |
| | [Icone delle cartelle] | Mostra un'icona accanto a ogni cartella |
| | [Numero di elementi nelle cartelle] | Mostra il numero di documenti contenuti in ogni cartella |
| | [Guide dei livelli] | Mostra le linee guida che indicano i livelli |
| | [Nascondi se c'è un solo documento] | In una radice della documentazione con un solo documento, chiude automaticamente l'INDEX solo la prima volta |
| | [Comprimi i dettagli del documento] | Comprime la tabella di gestione all'inizio del documento nella riga «Informazioni sul documento». Se disattivata, la tabella viene mostrata così com'è |
| | [Densità di visualizzazione] | Sceglie l'interlinea dell'INDEX tra [Normale] e [Compatta] |
| | [Pulsante di modifica] | Mostra [Modifica] in basso a destra nel testo |
| Azioni | [Ripristina i valori predefiniti del progetto] | Elimina tutte le modifiche dell'utente e ripristina le impostazioni del progetto |
| | [Apri le impostazioni dell'estensione] | Apre le impostazioni di Lunascape Docs nella schermata delle impostazioni di VS Code |

> **Suggerimento**
>
> - Le impostazioni di visualizzazione vengono salvate per ogni utente e per ogni radice della documentazione, e non vengono scritte nei file gestiti con Git.
> - Le impostazioni hanno la seguente priorità: «impostazioni di visualizzazione dell'utente → impostazioni di VS Code → `lunascape-docs.json` → valori predefiniti del prodotto». I valori predefiniti comuni al team si stabiliscono con `tree` ed `editor` in `lunascape-docs.json`.

## Cambiare i colori

Premendo il selettore del tema (sole/luna) nella barra degli strumenti si passa dallo sfondo bianco ai colori di VS Code. I colori all'apertura sono determinati dall'impostazione `lunascapeDocEditor.appearance` (`light` oppure `auto`).

## Argomenti correlati

- [Usare l'INDEX](index-panel.md)
- [Impostazioni del progetto](../04-document-tools/project-configuration.md)
- [Elenco delle impostazioni di VS Code](../08-reference/settings.md)
