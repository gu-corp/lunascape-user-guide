# Utilizarea INDEX

INDEX din partea stângă a ecranului este arborele folderelor și al documentelor din rădăcina documentației.

## Filtrarea

1. Introduceți un cuvânt în [Filtrează documentele], deasupra INDEX.
2. Se afișează doar elementele al căror nume de document se potrivește. Ștergeți textul introdus pentru a reveni la starea inițială.

> **Notă**
>
> Cât timp filtrarea este activă, reordonarea prin glisare și plasare nu este posibilă.

## Extinderea și restrângerea folderelor

- Apăsați săgeata din stânga numelui folderului sau numele unui folder fără pagină de prezentare pentru a-l extinde sau a-l restrânge.
- Un folder care are o pagină de prezentare (un fișier `README.md` sau `index.md` cu conținut) își deschide pagina de prezentare când îi apăsați numele. Pentru a-l doar extinde sau restrânge, folosiți [Extinde folderul] / [Restrânge folderul] din meniul elementului.
- Starea de extindere a folderelor este reținută pentru fiecare utilizator și nu se scrie în fișierele urmărite de Git.

## README și pagina de prezentare a folderului

`README.md` este fișierul care descrie conținutul folderului respectiv.

- Dacă folderul are un README, apăsarea numelui folderului afișează acel README.
- Dacă folderul nu are README, se afișează primul document din interiorul lui.
- Titlul (H1) al fișierului README devine numele folderului afișat în INDEX.

Fișierul README nu este obligatoriu. Pentru a-l adăuga ulterior, alegeți [Creează un README] din meniul elementului pentru folderul respectiv (apare doar la folderele care nu au README).

## Afișarea și ascunderea INDEX

- Pictograma din stânga, din comenzile pentru coloane ale barei de instrumente, afișează sau ascunde INDEX. Pictograma din dreapta afișează sau ascunde „Pe această pagină".
- Când ecranul este îngust, INDEX pornește în stare închisă. Apăsați [Deschide INDEX] (cele trei linii), afișat în stânga butonului [Înapoi], iar INDEX se deschide suprapus peste document. Se închide cu [×] din interiorul INDEX, cu un clic pe fundal, cu `Esc` sau la trecerea la alt document. Această deschidere temporară nu modifică setarea pentru ecranele late.
- Într-o rădăcină a documentației cu un singur document de afișat, INDEX se închide automat doar prima dată. Îl puteți redeschide cu pictograma pentru coloane. Puteți dezactiva acest comportament din [Setări de afișare], cu opțiunea [Ascunde automat dacă există un singur document].

## Utilizarea meniului elementului

Apăsați [⋯], care apare când treceți cu mausul peste un element din INDEX, sau faceți clic dreapta pe element pentru a deschide meniul acelui element. Elementele sunt așezate în ordinea următoare.

| Grup | Elemente |
|---|---|
| Acțiuni frecvente | [Extinde folderul] / [Restrânge folderul], [Deschide INDEX] (deschide pagina de prezentare a folderului), [Editează], [Schimbă titlul], [Deschide în VS Code], [Copiază calea] |
| Creare și organizare | [Creează un README] (doar la folderele fără README), [Document nou], [Folder nou], [Duplică], [Schimbă numele fișierului] / [Schimbă numele folderului], [Mută mai sus], [Mută mai jos] |
| Ștergere | [Mută în coșul de gunoi] |

- Pentru a crea direct în rădăcina documentației, apăsați [⋯] din capătul din dreapta al titlului INDEX sau faceți clic dreapta pe o zonă liberă din INDEX, apoi alegeți [Document nou] sau [Folder nou]. În același meniu se află [Schimbă numele documentului] și, dacă rădăcina documentației nu are README, [Creează un README]. Același meniu se deschide și dacă faceți clic dreapta pe numele documentului afișat în bara de instrumente.
- În meniu vă deplasați cu `↑` `↓`, iar cu `Home` `End` ajungeți la primul și la ultimul element. Dacă îl închideți cu `Esc`, focalizarea revine în locul din care a fost deschis.

> **Notă**
>
> Elementele de creare, organizare și ștergere apar doar dacă spațiul de lucru este de încredere în VS Code. Ele nu sunt disponibile nici în timpul editării unui document, nici cât timp se execută o altă operație în INDEX.

## Schimbarea aspectului

Din [Setări de afișare] puteți modifica afișarea numelor de fișiere, pictogramele documentelor și ale folderelor, numărul de elemente din foldere, liniile de ghidare a ierarhiei și densitatea afișării. Pentru detalii, consultați [Modificarea setărilor de afișare](display-settings.md).

## Subiecte conexe

- [Crearea și organizarea documentelor și a folderelor](../03-editing/organize.md)
- [Modificarea ordinii documentelor](../03-editing/reorder.md)
