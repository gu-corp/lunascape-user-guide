# Che cosa fa il visualizzatore Web

Il visualizzatore Web di Lunascape Docs è disponibile all'indirizzo <https://docs.lunascape.org/>. Senza installare nulla, puoi leggere i documenti su GitHub come se fossero un sito Web.

## Funzioni

| Funzione | Descrizione |
|---|---|
| Repository pubblici | Apre i documenti di un repository pubblico di GitHub senza accedere |
| Repository privati | Dopo l'accesso con GitHub, apre i repository per cui hai il permesso di lettura |
| Cartelle locali | [Apri i documenti] e poi [Apri i documenti da una cartella locale] apre una cartella sul tuo dispositivo (solo browser compatibili) |
| Lettura | INDEX, collegamenti, cronologia, filtro, sommario della pagina, cambio di lingua e cambio di tema. Come nella versione per VS Code |
| Diagrammi e formule | Mermaid, Vega-Lite, Markmap, WaveDrom, Svgbob, Penrose, formule KaTeX |
| Bozze | Modifica i documenti e conserva le modifiche come bozze sul dispositivo. Nulla viene scritto nel repository |
| Collegamenti diretti alle pagine | Un URL può indicare il repository e la pagina, così una pagina specifica si apre direttamente |

## Differenze rispetto alla versione per VS Code

- Il controllo dei documenti, la creazione da modelli, la generazione di proposte di traduzione e il riordino dall'INDEX non sono disponibili nel visualizzatore Web.
- I diagrammi TikZ non vengono disegnati.
- Le modifiche non vengono scritte nel repository: diventano bozze sul dispositivo. La «richiesta di pubblicazione», che invia le bozze come pull request, è implementata ma non è attiva nel visualizzatore pubblico. Per riportare le modifiche nel repository, usa la versione per VS Code oppure modifica in un clone locale.

## Argomenti correlati

- [Aprire un repository di GitHub](open-repository.md)
- [Leggere un repository privato](private-repository.md)
- [Salvare le bozze](drafts.md)
