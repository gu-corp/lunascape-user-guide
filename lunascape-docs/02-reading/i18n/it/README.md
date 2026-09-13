# Operazioni di base

Le operazioni di base, dall'apertura dei documenti fino alla pagina che si desidera leggere.

## Aprire i documenti

1. Aprire il repository in VS Code.
2. Nella tavolozza dei comandi (`⇧⌘P` / `Ctrl+Shift+P`), eseguire «Lunascape Docs: apri il visualizzatore delle specifiche».
   Viene individuata la radice della documentazione più vicina (per impostazione predefinita la cartella `docs`) e ne viene mostrata la pagina iniziale.

> **Suggerimento**
>
> - Nell'Esplora risorse, fare clic con il pulsante destro su un file Markdown e scegliere [Lunascape Docs: apri nel visualizzatore delle specifiche] per partire da quel file.
> - Aprendo un file Markdown che non appartiene ad alcuna radice della documentazione, la sua cartella viene mostrata come radice della documentazione temporanea.

## Spostarsi tra le pagine

| Operazione | Modo |
|---|---|
| Aprire dal sommario | Premere il nome di un documento nell'INDEX a sinistra |
| Seguire un collegamento | Premere un collegamento nel testo. Si apre nella stessa schermata |
| Ripercorrere la cronologia | [Indietro] e [Avanti] nella barra degli strumenti, oppure `Alt`+`←` / `Alt`+`→` |
| Tornare alla pagina iniziale | [Pagina iniziale della documentazione] nella barra degli strumenti |
| Salire di un livello | [INDEX superiore] nella barra degli strumenti, oppure una voce del percorso di navigazione |
| Spostarsi all'interno della pagina | Premere un titolo in «In questa pagina» a destra |

## Cercare un documento

Digitando una parola in [Filtra i documenti], sopra l'INDEX, vengono mostrati solo i documenti il cui nome corrisponde. Cancellando il testo si torna alla visualizzazione precedente.

## Aggiornare al contenuto più recente

Quando si salva un file Markdown nell'editor di VS Code, la visualizzazione si aggiorna automaticamente. Dopo aver modificato i file con uno strumento esterno, premere [Ricarica] nella barra degli strumenti.

> **Nota**
>
> - I collegamenti esterni presenti nel testo (`https://` e simili) si aprono nel browser predefinito. I collegamenti a file esterni alla radice della documentazione non vengono aperti.
> - I documenti consultati vengono elaborati sul dispositivo. Per la lettura, nessun documento viene inviato all'esterno.

## Argomenti correlati

- [Usare l'INDEX](index-panel.md)
- [Cambiare radice della documentazione](roots.md)
- [Modificare un documento](../03-editing/README.md)
