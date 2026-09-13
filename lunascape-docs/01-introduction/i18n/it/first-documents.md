# Creare i primi documenti

In un progetto che non ha ancora una cartella della documentazione, puoi creare un primo gruppo di documenti dalla palette dei comandi.

1. Apri la cartella del progetto in VS Code e imposta l'area di lavoro come attendibile.
2. Nella palette dei comandi (`⇧⌘P` / `Ctrl+Shift+P`) esegui «Lunascape Docs: Crea documentazione da modello».
   Se l'area di lavoro contiene più cartelle, scegli quella in cui creare i documenti.
3. Scegli la struttura da creare.
   - [Documento a pagina singola]: solo `README.md`, la struttura minima. Adatta a una specifica breve, ad appunti o a un documento esplicativo autonomo.
   - [Set di documentazione]: crea una pagina iniziale e le pagine di accesso a `specification/` (specifiche), `manual/` (manuale) e `help/` (guida).
4. Inserisci il titolo della documentazione. Viene usato per il README e per i titoli dei singoli documenti.
5. Inserisci la cartella della documentazione da creare. Il percorso è relativo all'area di lavoro e per impostazione predefinita è `docs`.
6. Controlla l'elenco dei file che verranno creati e premi [Crea].
   Al termine della creazione, il nuovo `README.md` si apre nel visualizzatore.

> **Nota**
>
> - I file esistenti non vengono mai sovrascritti. Se anche uno solo dei file da creare esiste già, l'operazione si interrompe senza creare nulla.
> - La creazione non è possibile in un'area di lavoro non attendibile.

> **Suggerimento**
>
> - Se hai già una cartella della documentazione, questa procedura non serve: passa a [Operazioni di base](../02-reading/README.md).
> - Quando i documenti aumentano, puoi aggiungerli uno alla volta scegliendo un modello nella scheda [Crea] degli Strumenti documento.

## Argomenti correlati

- [Creare un documento da un modello](../04-document-tools/templates.md)
- [Radici della documentazione e convenzioni sui file](../04-document-tools/structure.md)
