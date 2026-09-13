# Salvarea ciornelor

Când editați un document în vizualizatorul Web, modificările nu sunt scrise în depozit. Ele sunt păstrate în browser sub formă de „ciornă”.

## Crearea unei ciorne

1. Deschideți un document și apăsați [Editează] în dreapta jos.
2. Editați și apăsați [Salvează].
   Se afișează „Salvat ca ciornă”, iar modificarea este păstrată în browser.

- Documentele care au o ciornă primesc o insignă în INDEX. Deasupra textului se afișează „Acest document este o ciornă de pe acest dispozitiv (nepublicată)”.
- [Ciorne] din bara de instrumente afișează numărul de ciorne, iar la apăsare deschide lista acestora.

## Renunțarea la o ciornă

- Pentru a renunța la ciorna unui singur document, apăsați [Renunță la ciornă] deasupra textului.
- Pentru a renunța la toate, folosiți lista de ciorne.

## Aplicarea ciornelor în depozit

„Cererea de publicare”, care trimite ciornele sub formă de pull request, este implementată, dar nu este activată în vizualizatorul public. Pentru a modifica depozitul, editați cu extensia VS Code sau într-o clonă locală.

> **Notă**
>
> - Ciornele sunt păstrate în browser (IndexedDB). Ele nu se transferă în alt browser sau pe alt dispozitiv, iar ștergerea datelor de sit le elimină.
> - Dacă documentul din depozit se modifică după ce ați creat ciorna, se afișează „Sursa din amonte a fost actualizată”. Verificați conținutul și decideți dacă renunțați la ciornă sau o păstrați.
> - Dacă editați un folder local deschis din [Deschide documente], modificările sunt scrise direct în fișier, dacă browserul acceptă acest lucru. În caz contrar, ele sunt păstrate doar pe durata sesiunii curente.

## Subiecte conexe

- [Ce puteți face în vizualizatorul Web](README.md)
- [Editarea unui document](../03-editing/README.md)
