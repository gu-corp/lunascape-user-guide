# Usare INDEX

INDEX, a sinistra dello schermo, è l'albero delle cartelle e dei documenti presenti nella radice della documentazione.

## Filtrare

1. Digitare una parola in [Filtra i documenti], sopra INDEX.
2. Vengono mostrate solo le voci il cui nome corrisponde. Cancellando il testo si torna alla vista completa.

> **Nota**
>
> Durante il filtraggio non è possibile riordinare le voci per trascinamento.

## Espandere e comprimere le cartelle

- Premere la freccia a sinistra del nome della cartella, oppure il nome di una cartella priva di copertina, per espanderla o comprimerla.
- Le cartelle con una copertina (un `README.md` o un `index.md` con contenuto) aprono tale copertina quando si preme il nome. Per limitarsi a espandere o comprimere, usare [Espandi cartella] / [Comprimi cartella] nel menu della voce.
- Lo stato di espansione delle cartelle viene memorizzato per ciascun utente e non viene scritto nei file gestiti da Git.

## README e la copertina della cartella

`README.md` è il file che descrive il contenuto della cartella.

- Nelle cartelle che hanno un README, premendo il nome della cartella viene mostrato quel README.
- Nelle cartelle senza README viene mostrato il primo documento contenuto al loro interno.
- Il titolo (H1) del README diventa il nome della cartella in INDEX.

Il README non è obbligatorio. Per aggiungerlo in un secondo momento, scegliere [Crea un README] nel menu della cartella (compare solo per le cartelle che non ne hanno uno).

## Mostrare o nascondere INDEX

- L'icona di sinistra tra i comandi delle colonne nella barra degli strumenti mostra o nasconde INDEX. L'icona di destra mostra o nasconde «In questa pagina».
- Quando lo schermo è stretto, INDEX si presenta chiuso. Premendo [Apri INDEX] (le tre linee), a sinistra di [Indietro], INDEX si apre sovrapposto al testo. Si chiude con la [×] all'interno di INDEX, con un clic sullo sfondo, con `Esc` oppure passando a un altro documento. Questa apertura temporanea non modifica l'impostazione usata sugli schermi ampi.
- Nelle radici della documentazione con un solo documento da mostrare, INDEX si chiude automaticamente solo la prima volta. È possibile riaprirlo con l'icona delle colonne. Questo comportamento si disattiva con [Nascondi se c'è un solo documento] in [Impostazioni di visualizzazione].

## Usare il menu della voce

Passando il puntatore su una voce di INDEX compare [⋯]; premendolo, oppure facendo clic con il pulsante destro sulla voce, si apre il menu di quella voce. Le voci sono disposte in quest'ordine.

| Gruppo | Voci |
|---|---|
| Operazioni frequenti | [Espandi cartella] / [Comprimi cartella], [Apri INDEX] (apre la copertina della cartella), [Modifica], [Rinomina il titolo], [Apri in VS Code], [Copia il percorso] |
| Creazione e organizzazione | [Crea un README] (solo per le cartelle senza README), [Nuovo documento], [Nuova cartella], [Duplica], [Rinomina il file] / [Rinomina la cartella], [Sposta su di una posizione], [Sposta giù di una posizione] |
| Eliminazione | [Sposta nel cestino] |

- Per creare un elemento direttamente nella radice della documentazione, premere [⋯] all'estremità destra dell'intestazione di INDEX, oppure fare clic con il pulsante destro su un punto vuoto di INDEX, e scegliere [Nuovo documento] o [Nuova cartella]. Nello stesso menu si trova [Rinomina il documento] e, se la radice della documentazione non ha un README, [Crea un README]. Lo stesso menu si apre facendo clic con il pulsante destro sul nome del documento mostrato nella barra degli strumenti.
- All'interno del menu, `↑` `↓` spostano tra le voci e `Home` `End` portano alla prima e all'ultima. Chiudendo con `Esc`, lo stato attivo torna al punto da cui il menu è stato aperto.

> **Nota**
>
> Le voci di creazione, organizzazione ed eliminazione compaiono solo quando l'area di lavoro è attendibile in VS Code. Non sono inoltre disponibili durante la modifica di un documento o mentre è in corso un'altra operazione su INDEX.

## Cambiare l'aspetto

Da [Impostazioni di visualizzazione] è possibile modificare la visualizzazione dei nomi dei file, le icone dei documenti e delle cartelle, il numero di elementi nelle cartelle, le linee guida dei livelli e la densità di visualizzazione. Per i dettagli, vedere [Modificare le impostazioni di visualizzazione](display-settings.md).

## Argomenti correlati

- [Creare e organizzare documenti e cartelle](../03-editing/organize.md)
- [Modificare l'ordine dei documenti](../03-editing/reorder.md)
