# Operații de bază

Operațiile de bază, de la deschiderea documentelor până la ajungerea la pagina pe care vrei să o citești.

## Deschiderea documentelor

1. Deschide depozitul în VS Code.
2. În paleta de comenzi (`⇧⌘P` / `Ctrl+Shift+P`), execută „Lunascape Docs: Deschide vizualizatorul de specificații”.
   Este găsită cea mai apropiată rădăcină a documentației (implicit folderul `docs`) și se afișează pagina de start.

> **Sfat**
>
> - Fă clic dreapta pe un fișier Markdown în Explorer și alege [Lunascape Docs: Deschide în vizualizatorul de specificații] pentru a porni de la acel fișier.
> - Dacă deschizi un fișier Markdown care nu aparține niciunei rădăcini a documentației, folderul său este afișat ca rădăcină a documentației temporară.

## Deplasarea între pagini

| Operație | Metodă |
|---|---|
| Deschiderea din cuprins | Apasă numele unui document în INDEX, în stânga |
| Urmărirea unei legături | Apasă o legătură din text. Se deschide în aceeași vizualizare |
| Parcurgerea istoricului | [Înapoi] și [Înainte] din bara de instrumente sau `Alt`+`←` / `Alt`+`→` |
| Revenirea la pagina de start | [Pagina principală a documentației] din bara de instrumente |
| Urcarea cu un nivel | [INDEX părinte] din bara de instrumente sau un element din firul de navigare |
| Deplasarea în interiorul paginii | Apasă un titlu în „Pe această pagină”, în dreapta |

## Găsirea unui document

Scrie un cuvânt în [Filtrează documentele], deasupra INDEX-ului, pentru a afișa doar documentele ale căror nume se potrivesc. Șterge textul introdus pentru a reveni la starea inițială.

## Actualizarea la conținutul cel mai recent

Când salvezi un fișier Markdown în editorul VS Code, afișarea se actualizează automat. Dacă ai făcut modificări cu un instrument extern, apasă [Reîncarcă] din bara de instrumente.

> **Notă**
>
> - Legăturile externe din text (`https://` și altele) se deschid în browserul implicit. Legăturile către fișiere aflate în afara rădăcinii documentației nu se deschid.
> - Documentul pe care îl citești este prelucrat pe dispozitivul tău. Pentru citire, documentele nu sunt trimise nicăieri.

## Subiecte conexe

- [Utilizarea INDEX-ului](index-panel.md)
- [Schimbarea rădăcinii documentației](roots.md)
- [Editarea unui document](../03-editing/README.md)
