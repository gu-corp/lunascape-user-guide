# Crearea unui document dintr-un șablon

În fila [Creează] din Instrumente pentru documente alegeți un șablon, previzualizați conținutul și apoi creați un document nou.

1. Apăsați [Instrumente pentru documente] în bara de instrumente și deschideți fila [Creează].
2. Apăsați [Creează dintr-un șablon] și alegeți un șablon.
3. Completați câmpurile de intrare (titlu, rezumat și altele). Câmpurile obligatorii sunt marcate cu „Obligatoriu”.
4. Introduceți destinația ca o cale relativă la rădăcina documentației (de exemplu `03-design/api.md`).
5. Apăsați [Previzualizare] și verificați codul Markdown generat.
6. Apăsați [Creează cu acest conținut].
   Documentul este creat și afișat în vizualizator. În continuare se execută verificarea întregii rădăcini a documentației.

## Șabloane disponibile

| Șablon | Conținut |
|---|---|
| Document de o pagină | O specificație scurtă, notițe sau un document explicativ de sine stătător, într-un singur fișier |
| Specificație, manual, ajutor | Un singur fișier cu o structură generală de capitole, potrivită pentru o specificație, un manual sau un ajutor |
| Șabloanele din Standard Pack | Când în `lunascape-docs.json` este selectat Standard Pack, se adaugă tipurile de documente disponibile în profilul respectiv (documente de cerințe, documente de proiectare și altele) |

> **Notă**
>
> - Crearea necesită un spațiu de lucru de încredere.
> - Fișierele existente nu sunt suprascrise. Dacă la destinație există un document cu același nume, crearea nu este posibilă.
> - Destinația necesită extensia `.md` sau `.mdx`. Nu se poate crea nimic sub `i18n` (locul versiunilor traduse).
> - După ce modificați datele introduse, apăsați din nou [Previzualizare] înainte de a crea documentul.

> **Sfat**
>
> Într-un proiect care nu are încă un folder de documente, puteți crea primul set cu „Lunascape Docs: Creează documentație dintr-un șablon” din paleta de comenzi. Consultați [Crearea primelor documente](../01-introduction/first-documents.md).

## Subiecte asociate

- [Utilizarea Instrumentelor pentru documente](README.md)
- [Modificarea regulilor de verificare](rules.md)
