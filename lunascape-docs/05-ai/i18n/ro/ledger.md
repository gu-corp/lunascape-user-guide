# Registrul și înregistrările

Registrul din partea de sus a filei [AI] arată starea traducerii pentru fiecare limbă acceptată. Vă este util și fără AI: arată ce lipsește.

| Afișare | Semnificație |
|---|---|
| Netradus | Numărul de documente care nu au încă o traducere |
| Necesită actualizare | Numărul de documente care au o traducere, dar al căror document canonic este mai nou decât înregistrarea |
| Tradus | Numărul de traduceri care urmează documentul canonic |

Registrul se calculează parcurgând rădăcina documentației. Nu intervine nici AI, nici un model lingvistic.

## Actualizarea înregistrărilor traducerii

Pentru a stabili starea „necesită actualizare”, este nevoie de o înregistrare a documentului canonic și a traducerii din momentul traducerii. Un AI de tip sesiune scrie fișierele direct, așa că înregistrarea nu se creează automat.

1. După ce traducerea s-a încheiat și ați verificat conținutul, apăsați [Actualizează înregistrările traducerii].
2. Traducerile fără înregistrare sunt înregistrate ca fiind corespunzătoare documentului canonic actual.

Sesiunile Claude Code și salvările de tip API creează înregistrarea automat (sesiunii i se indică să folosească instrumentul MCP `record_translation_freshness`). Butonul vă este necesar atunci când ați tradus cu Codex sau din chatul VS Code.

De atunci înainte, dacă modificați documentul canonic, traducerea sa este afișată ca „necesită actualizare”.

> **Notă**
>
> - Traducerile care au deja o înregistrare nu sunt suprascrise, pentru a nu șterge o stare „necesită actualizare” existentă.
> - Înregistrările se salvează în `.lunascape-docs/translation-freshness.json`. Se salvează doar calea relativă, limba, hash-ul conținutului și data și ora, niciodată textul documentului.

## Subiecte conexe

- [Lucrările care pot fi predate](tasks.md)
- [Citirea în altă limbă](../02-reading/languages.md)
