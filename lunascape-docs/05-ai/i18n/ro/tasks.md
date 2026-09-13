# Lucrări care pot fi predate

Se alege din [Lucrare], în fila [AI]. Pentru fiecare lucrare se schimbă instrucțiunea predată și verificarea de după.

| Lucrare | Conținut | Ce este necesar | Tip API |
|---|---|---|---|
| Tradu această pagină | Traduce documentul afișat în limba aleasă | Documentul vizat deschis, limba țintă | Da |
| Tradu tot ce este netradus | Traduce, pe rând, documentele netraduse și cele care necesită actualizare în limba aleasă | Limba țintă | Doar tip sesiune |
| Corectează această pagină | Verifică și corectează terminologia, stilul și structura pe capitole cerută de standardul documentelor | Documentul vizat deschis | Da |
| Creează un document nou | Creează un document nou după standardul documentelor și șabloanele sale | Un subiect (opțional) | Doar tip sesiune |

## Ce conține instrucțiunea

| Nr. | Conținut |
|---|---|
| 1 | Poziția rădăcinii documentației, cu indicația de a nu modifica nimic în afara ei |
| 2 | Limba implicită (documentul canonic) și locul traducerilor (folderul `i18n/<limbă>/` din același folder cu documentul) |
| 3 | Faptul că `navigation.order` aparține numai documentului canonic și că o traducere poate suprascrie doar `navigation.title` |
| 4 | Faptul că ID-urile de cerințe, linkurile, codul, Mermaid, TeX și structura front matter nu se modifică |
| 5 | Standardul documentelor și glosarul (`terminology` din `docs-lint.config.json`) |
| 6 | La final, să ruleze verificarea documentelor, să raporteze fișierele modificate și să nu efectueze operații Git |

> **Sfat**
>
> Documentele vizate de „Tradu tot ce este netradus" provin din registru, cel mult 200 de documente la o rulare. Dacă sunt mai multe, rulați din nou.

## Subiecte conexe

- [Predarea lucrărilor către AI](README.md)
- [Registrul și înregistrările sale](ledger.md)
