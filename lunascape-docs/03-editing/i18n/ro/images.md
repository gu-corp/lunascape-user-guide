# Ajustarea dimensiunii imaginilor

Imaginile inserate într-un document se încadrează automat în lățimea textului și în înălțimea ecranului. Pentru o imagine care trebuie afișată la o anumită dimensiune, puteți indica lățimea.

## Cum funcționează ajustarea automată

- O imagine Markdown obișnuită (`![descriere](./images/screen.png)`) este micșorată pentru a se încadra în lățimea textului. Nu este niciodată mărită peste dimensiunea originală.
- O captură de ecran înaltă este limitată la 72% din înălțimea ecranului sau la 720px, oricare dintre valori este mai mică.

## Indicarea lățimii în ecranul de editare

1. Apăsați [Editează] și selectați imaginea în afișarea vizuală.
2. Alegeți o lățime din [Lățimea imaginii] de pe bara de instrumente.
3. Apăsați [Salvează].

| Opțiune | Lățime |
|---|---|
| [Automat] | Neindicată (ajustare automată) |
| [Mică (360px)] | 360px |
| [Medie (560px)] | 560px |
| [Mare (760px)] | 760px |
| [Lățimea textului (920px)] | 920px |
| [Personalizată…] | Orice număr întreg între 16 și 4096px |

## Indicarea lățimii în Markdown

Adăugați un atribut `width` numeric etichetei HTML `img`. Aceasta este o scriere care se afișează la fel pe GitHub și în MDX.

```html
<img src="./images/screen.png" alt="Ecranul de setări" width="360" />
```

> **Notă**
>
> - Pentru `width` indicați doar un număr. Nu adăugați `px` sau `%`. Chiar dacă indicați o valoare mai mare decât lățimea textului, afișarea se încadrează în lățimea textului.
> - Imaginile se indică prin calea relativă față de document. Imaginile aflate în afara rădăcinii documentației nu se afișează.

## Subiecte conexe

- [Editarea unui document](README.md)
- [Diagramele, formulele matematice sau imaginile nu se afișează](../07-troubleshooting/rendering.md)
