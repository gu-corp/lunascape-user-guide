# Predarea lucrului către o inteligență artificială

Lunascape Docs nu apelează un model lingvistic. Pregătește **contextul, instrumentele și verificările**, iar traducerea, corectura și redactarea rămân în sarcina inteligenței artificiale pe care o folosiți.

## Ideea

| Ce pune la dispoziție produsul | Conținut |
|---|---|
| Context | Convențiile documentației (unde se află traducerile, front matter, standardul documentelor, glosarul) și locul documentului vizat |
| Instrumente de lucru | Registrul traducerilor netraduse și al celor care necesită actualizare, citirea și scrierea documentelor, crearea dintr-un șablon |
| Verificări ulterioare | Verificarea cu docs-lint, diferența de acoperire și de prospețime |

Instrucțiunea nu cuprinde textul documentului: inteligența artificială citește singură fișierele, le scrie singură și le verifică singură.

## Predarea lucrului

1. Apăsați [Instrumente pentru documente] din bara de instrumente și deschideți fila [AI].
2. Alegeți lucrarea pe care doriți să o predați din [Lucrare].
3. Completați câmpurile necesare (limba țintă, subiectul).
4. Apăsați [Predă această lucrare].
   Se deschide un terminal VS Code, iar inteligența artificială aleasă preia instrucțiunea și începe lucrul.

> **Sfat**
>
> O sesiune Claude Code este însoțită de instrumentele de lucru (serverul MCP `lunascape-docs`). Sesiunea poate obține singură lista celor netraduse și a celor care necesită actualizare, poate rula docs-lint și poate înregistra prospețimea după traducere.

## Verificarea rezultatului

| Forma furnizorului | Unde ajunge rezultatul |
|---|---|
| De tip sesiune (Claude Code, Codex) | Scrie direct în arborele de lucru. **Verificați în diferența Git** |
| De tip API (modelele lingvistice din VS Code, Anthropic, compatibile OpenAI) | Returnează câte o propunere pe document. Verificați cu [Deschide diferența] și scrieți cu [Salvează] |

### Verificarea unei propuneri de tip API

Când rulați cu un furnizor de tip API, propunerea ajunge în fila [AI].

1. Apăsați [Deschide diferența] și comparați cu conținutul actual.
2. Dacă este în regulă, apăsați [Salvează]. În cazul unei traduceri se înregistrează și prospețimea. Dacă renunțați, apăsați [Renunță].
   Pentru a opri generarea la jumătate, apăsați [Oprește].

> **Notă**
>
> - Lunascape Docs nu efectuează niciodată operații de staging sau commit în Git. Verificați întotdeauna modificările în diferență.
> - Într-un spațiu de lucru în care nu aveți încredere și la afișarea temporară a unui folder din afara rădăcinii documentației, lucrul nu poate fi predat.

## Subiecte înrudite

- [Lucrările care pot fi predate](tasks.md)
- [Setări AI](settings.md)
- [Registrul și înregistrările](ledger.md)
