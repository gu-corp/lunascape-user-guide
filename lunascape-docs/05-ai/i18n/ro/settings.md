# Setări AI

Alegeți AI-ul și modelul care primesc lucrarea. Nu se folosește selectorul rapid din VS Code, ci listele derulante din acest ecran.

1. Apăsați [Instrumente pentru documente] → fila [AI] → [Setări AI…].
2. Alegeți [Furnizor].
   Cele care nu pot fi folosite în acest mediu apar ca neselectabile, împreună cu motivul.
3. Alegeți [Model]. Opțiunile diferă de la un furnizor la altul.
4. Închideți ecranul. Alegerea se salvează pentru fiecare utilizator și se folosește și data viitoare.

## Furnizori

| Furnizor | Formă | Metodă de detectare |
|---|---|---|
| Claude Code | De sesiune | Prezența comenzii `claude` |
| Codex | De sesiune | Prezența comenzii `codex` |
| Modelele de limbaj din VS Code | De tip API | Modelele înregistrate în VS Code Language Model API |
| Anthropic API | De tip API | Înregistrarea unei chei API |
| API compatibil OpenAI | De tip API | Înregistrarea unei chei API și a unui punct final |

Un furnizor **de sesiune** citește și scrie el însuși fișierele și rulează el însuși verificarea documentelor. Rezultatele se scriu direct în arborele de lucru și se examinează în diferența Git.

Un furnizor **de tip API** returnează un document în Markdown, iar extensia arată diferența înainte de salvare.

## Înregistrarea unei chei API

Anthropic API și API-urile compatibile OpenAI pot fi folosite după înregistrarea unei chei API.

1. Alegeți furnizorul din [Furnizor]. Apare câmpul pentru cheia API.
2. Introduceți [Cheie API]. Pentru un API compatibil OpenAI, introduceți și [Punct final] (de exemplu `https://api.openai.com/v1`).
3. Apăsați [Salvează]. Se afișează „Cheie înregistrată”.

> **Notă**
>
> - Cheia se salvează în SecretStorage din VS Code și nu se mai afișează. Nu este scrisă nici în `settings.json`, nici în vreun document. O puteți șterge cu [Șterge cheia].
> - Lista de modele se obține de la fiecare serviciu cu cheia înregistrată. Până la obținerea ei se afișează o listă cunoscută.
> - Un furnizor de tip API poate rula doar „Tradu această pagină” și „Corectează această pagină”. Parcurgerea mai multor documente și crearea de documente se fac cu un furnizor de sesiune.

> **Sfat**
>
> Dacă nu este găsit niciun furnizor, instalați Claude Code sau Codex ori înregistrați o cheie API. Redeschideți [Setări AI…] și acesta va fi detectat.

## Subiecte conexe

- [Predarea lucrării către AI](README.md)
- [Lista setărilor VS Code](../08-reference/settings.md)
