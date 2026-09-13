# Citirea în altă limbă

Când un document are traduceri, puteți schimba limba din meniul de limbi (globul) din bara de instrumente.

## Schimbarea limbii

1. Apăsați meniul de limbi din bara de instrumente.
   Se afișează limba paginii curente și motivul pentru care a fost aleasă (calea versiunii traduse, detectarea automată sau limba implicită a proiectului).
2. Alegeți limba în care doriți să citiți.
   Se deschide traducerea aceluiași document. Limba aleasă este reținută, iar următorul document pe care îl deschideți este afișat în acea limbă, dacă există o traducere.

Lista de limbi arată dacă documentul are sau nu o traducere în fiecare limbă.

| Afișare | Semnificație |
|---|---|
| Tradus | Există o traducere și poate fi deschisă |
| Netradus | Limba este acceptată de proiect, dar acest document nu are încă traducere |
| Necesită actualizare | Traducerea există, dar documentul sursă a fost modificat după traducere |

> **Notă**
>
> - Alegerea unei limbi doar deschide o traducere existentă. Nu generează traduceri și nu creează fișiere. Pentru a crea o traducere, folosiți [Creare și gestionare traduceri…] din același meniu.
> - Când se constată că limba paginii curente diferă de limba implicită a proiectului, se afișează un avertisment. Configurația nu este niciodată rescrisă.

## Limba în care se deschide un document

Când deschideți un document, prima limbă de afișare se stabilește în următoarea ordine.

1. Limba pe care ați ales-o anterior în această rădăcină a documentației. Alegerea dumneavoastră este salvată (și alegerea limbii implicite se salvează ca alegere).
2. Limba interfeței din VS Code (în versiunea pentru browser web, setările de limbă ale browserului). Se selectează automat o limbă acceptată care se potrivește. O limbă cu indicativ regional (de exemplu `en-US`) se potrivește și cu limba de bază (`en`).
3. Limba de rezervă a proiectului (`fallbackLocale` din `lunascape-docs.json`).
4. Limba implicită a proiectului.

> **Sfat**
>
> - Când limba a fost selectată automat, limba curentă din meniul de limbi este marcată cu „Selectat automat”. Treceți indicatorul peste marcaj pentru a vedea motivul.
> - `fallbackLocale` este limba arătată cititorilor a căror limbă din mediul de consultare nu se potrivește cu niciuna dintre limbile acceptate. Într-un proiect al cărui document canonic este în japoneză și care are o versiune în engleză, dacă setați `"en"`, cititorilor cu mediul în spaniolă, de exemplu, li se deschide versiunea engleză. Dacă nu este setată, se folosește limba implicită.

## Unde se păstrează traducerile

Documentele în limba implicită rămân unde sunt, iar traducerea se pune în **`i18n/<limbă>/`, în același folder**, sub același nume de fișier.

```text
docs/
  README.md                  ← limba implicită (de exemplu japoneza)
  i18n/en/README.md          ← versiunea sa în engleză
  guide/
    setup.md
    i18n/en/setup.md         ← versiunea sa în engleză
```

> **Notă**
>
> - Recrearea structurii de foldere sub `i18n/` (`i18n/en/guide/setup.md`) nu este recunoscută. Folderul `i18n/` se pune întotdeauna în același folder cu documentul.
> - Traducerile se caută doar în acest singur loc. Dacă puneți traducerea aceluiași document și în `i18n/` din folderul părinte, nu apare niciun conflict de prioritate: acel fișier devine pur și simplu un fișier orfan, care nu apare nici în meniul de limbi, nici în registru (și nu este șters automat). Nu păstrați aceeași traducere în două locuri.

## Citirea în versiunea pentru browser web

Și în versiunea pentru browser web puteți schimba limba la fel, dacă există traduceri. Când doriți să citiți într-o limbă fără traducere, puteți folosi funcția de traducere a paginii din browser. Codul, formulele matematice și diagramele sunt excluse din traducere.

## Subiecte înrudite

- [Predarea unei sarcini către AI](../05-ai/README.md)
- [Sarcini care pot fi predate](../05-ai/tasks.md)
- [Modificarea setărilor de afișare](../02-reading/display-settings.md)
