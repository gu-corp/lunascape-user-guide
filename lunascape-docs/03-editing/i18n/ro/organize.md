# Crearea și organizarea documentelor și folderelor

Din meniul de element al INDEX puteți crea, duplica, redenumi și șterge documente și foldere. Introducerea datelor se face într-o fereastră mică din vizualizator, fără a întrerupe lectura.

> **Notă**
>
> Aceste acțiuni sunt disponibile numai când spațiul de lucru este de încredere în VS Code. Ele nu pot fi executate în timpul editării unui document, în timpul procesării altei operații sau când elementul vizat are modificări nesalvate.

## Crearea unui document sau folder

1. Deschideți meniul de element ([⋯] sau clic dreapta) al folderului de destinație.
   Pentru a crea direct sub rădăcina documentației, folosiți [⋯] din capătul din dreapta al titlului INDEX sau faceți clic dreapta pe o zonă goală din INDEX.
2. Alegeți [Document nou] sau [Folder nou].
3. Introduceți un nume și apăsați [Creează].
   Numele unui document necesită o extensie Markdown (`.md`, `.markdown`, `.mdx` și altele).

Documentele noi sunt create ca documente în limba implicită (documente canonice).

## Duplicarea unui document

1. Deschideți meniul de element al documentului și alegeți [Duplică].
2. Introduceți un nume nou și apăsați [Creează].

Se duplică doar documentul canonic. Traducerile nu sunt duplicate.

## Schimbarea titlului

Schimbă titlul documentului (H1). Numele fișierului rămâne neschimbat.

1. Deschideți meniul de element al unui document sau folder și alegeți [Schimbă titlul].
2. Introduceți noul titlu pe un singur rând și apăsați [Modifică].

În cazul unui folder, se schimbă titlul din `README.md` al acelui folder. Când limba afișată este o traducere, se schimbă titlul documentului din acea limbă.

## Schimbarea numelui documentației

Schimbă numele documentației afișat în bara de instrumente (numele rădăcinii documentației).

1. Faceți clic dreapta pe numele documentației din bara de instrumente. Meniul se deschide și din [⋯] aflat în capătul din dreapta al titlului INDEX.
2. Alegeți [Schimbă numele documentului] și introduceți un nume nou.

Cât timp nu este configurat nimic, se afișează numele folderului ca atare.

Numele modificat este scris în **locul care furnizează în prezent numele documentației**, astfel încât un titlu vizibil să nu ajungă niciodată ignorat.

| Starea actuală | Unde se scrie |
|---|---|
| `lunascape-docs.json` conține un nume | Se actualizează `lunascape-docs.json` |
| Nu există nume, dar rădăcina documentației are un README | Se rescrie titlul (H1) din README |
| Niciuna dintre acestea | Se creează `lunascape-docs.json` și numele se salvează acolo |

Mesajul afișat după modificare arată unde s-a scris numele.

> **Sfat**
>
> Numele documentației se stabilește în această ordine: numele din `lunascape-docs.json`, apoi titlul din README-ul rădăcinii documentației, apoi numele folderului.

## Schimbarea numelui unui fișier sau folder

1. Deschideți meniul de element și alegeți [Schimbă numele fișierului] sau [Schimbă numele folderului].
2. Introduceți noul nume și apăsați [Modifică].

Traducerile corespunzătoare (aceeași cale sub `i18n/<limbă>/`) sunt redenumite împreună.

## Ștergerea

1. Deschideți meniul de element și alegeți [Mută în coșul de gunoi].
2. Verificați conținutul mesajului de confirmare și aprobați mutarea.

Elementul este mutat în coșul de gunoi al sistemului de operare, deci poate fi restaurat dacă este nevoie. Traducerile nu sunt șterse și rămân pe loc.

## Nume care nu pot fi folosite

- Nume care încep cu `.` (nu ar apărea în INDEX)
- `i18n` (rezervat pentru fișierele de traducere)
- Nume rezervate de Windows (`CON`, `PRN` și altele)
- Nume care se termină cu un punct sau cu un spațiu
- Nume care conțin caractere de control sau caractere nepermise în numele de fișiere
- Nume care există deja în același folder (inclusiv nume care diferă doar prin literele mari și mici)

> **Notă**
>
> Pagina de pornire (de obicei `README.md` din rădăcină) nu poate fi redenumită sau mutată. Modificați mai întâi `startPage` din `lunascape-docs.json`.

## Subiecte conexe

- [Schimbarea ordinii documentelor](reorder.md)
- [Utilizarea INDEX](../02-reading/index-panel.md)
