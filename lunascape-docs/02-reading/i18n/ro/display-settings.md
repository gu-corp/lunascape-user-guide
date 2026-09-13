# Modificarea setărilor de afișare

Din [Setări de afișare] (rotița) de pe bara de instrumente, fiecare utilizator poate schimba modul în care arată INDEX și afișarea butonului de editare.

1. Apăsați [Setări de afișare] pe bara de instrumente.
2. Comutați elementele pe care doriți să le schimbați. Modificările se aplică imediat.
3. Apăsați din nou [Setări de afișare] sau faceți clic în afara panoului pentru a-l închide.

## Elemente disponibile

| Secțiune | Element | Rol |
|---|---|---|
| Limba documentului | (starea curentă) | Afișează limba implicită a proiectului și limba afișată în prezent. Din [Configurați limbile proiectului…] se deschid setările de limbă ale proiectului |
| Conținut | [Nume de fișiere] | Afișează numele fișierelor în locul titlurilor documentelor |
| | [Pictograme pentru documente] | Afișează o pictogramă la elementele de tip document |
| | [Pictograme pentru foldere] | Afișează o pictogramă la elementele de tip folder |
| | [Număr de elemente din folder] | Afișează numărul de documente conținute în folder |
| | [Ghidaje de indentare] | Afișează linii care indică nivelurile de ierarhie |
| | [Ascunde automat dacă există un singur document] | Într-o rădăcină a documentației cu un singur document, închide automat INDEX doar la prima deschidere |
| | [Restrânge informațiile documentului] | Restrânge tabelul de administrare din capul documentului într-un rând „Informații despre document”. Dezactivat, tabelul se afișează ca atare |
| | [Densitate de afișare] | Alegeți spațierea rândurilor din INDEX între [Normal] și [Compact] |
| | [Butonul de editare] | Afișează [Editează] în dreapta jos a textului |
| Acțiuni | [Revino la valorile implicite ale proiectului] | Șterge toate modificările utilizatorului și revine la setările proiectului |
| | [Deschide setările extensiei] | Deschide setările Lunascape Docs în ecranul de setări VS Code |

> **Sfat**
>
> - Setările de afișare se salvează pentru fiecare utilizator și pentru fiecare rădăcină a documentației și nu se scriu în fișierele urmărite de Git.
> - Setările se aplică în ordinea „setările de afișare ale utilizatorului → setările VS Code → `lunascape-docs.json` → valorile implicite ale produsului”. Valorile implicite comune echipei se stabilesc în `tree` și `editor` din `lunascape-docs.json`.

## Schimbarea combinației de culori

Apăsați comutatorul de temă (soare/lună) de pe bara de instrumente pentru a alterna între fundalul alb și combinația de culori a VS Code. Combinația de culori de la deschidere este stabilită de setarea `lunascapeDocEditor.appearance` (`light` sau `auto`).

## Subiecte conexe

- [Utilizarea INDEX](index-panel.md)
- [Configurarea proiectului](../04-document-tools/project-configuration.md)
- [Lista setărilor VS Code](../08-reference/settings.md)
