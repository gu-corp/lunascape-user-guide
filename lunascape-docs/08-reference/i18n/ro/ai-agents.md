# Utilizarea din agenți AI

Extensia înregistrează în VS Code Language Model Tool-ul `lunascape_getDocsSpecification`, care are doar drept de citire. Când un agent VS Code compatibil este întrebat despre funcțiile, configurarea sau convențiile de documente ale Lunascape Docs, poate obține prin acest instrument conținutul acestui ajutor (specificația generală).

## Mod de utilizare

Puneți întrebarea în chatul VS Code adăugând `#lunascapeDocs` sau întrebați pur și simplu despre configurarea Lunascape Docs ori despre structura documentelor.

```text
#lunascapeDocs Cum activez traducerea în engleză în lunascape-docs.json?
```

## Argumentele instrumentului

| Argument | Conținut |
|---|---|
| `topic` | Capitolul de obținut: `all`, `usage` (Operații de bază), `structure` (Rădăcina documentației și convențiile de fișiere), `editing` (Editarea unui document), `configuration` (Configurarea proiectului), `security` (Securitatea și limitele de scriere), `ai` (Utilizarea din agenți AI) |
| `locale` | Limba ajutorului (o etichetă de limbă a ajutorului inclus, de exemplu `ja` sau `en`). Dacă este omis, se folosește limba interfeței VS Code, iar în lipsa acesteia se returnează ajutorul în japoneză |

> **Notă**
>
> - Instrumentul nu trimite în exterior conținutul documentelor.
> - Instrumentul nu returnează numele spațiului de lucru și nici căi locale.
> - Instrumentul nu modifică fișiere.
> - Poate fi folosit din agenți VS Code compatibili chiar fără `AGENTS.md`. Nu este partajat automat cu alți clienți AI care nu folosesc API-ul de instrumente al extensiei.

## Subiecte asociate

- [Afișarea acestui ajutor](../02-reading/help.md)
- [Securitatea și limitele de scriere](security.md)
