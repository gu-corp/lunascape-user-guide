# Podešavanje veličine slika

Slike u dokumentu automatski se prilagođavaju širini teksta i visini zaslona. Za sliku koja se treba prikazati u određenoj veličini možete zadati širinu.

## Kako radi automatsko prilagođavanje

- Obična Markdown slika (`![opis](./images/screen.png)`) smanjuje se tako da stane u širinu teksta. Nikada se ne povećava iznad izvorne veličine.
- Visoka snimka zaslona ograničena je na 72 % visine zaslona ili 720px, ovisno o tome što je manje.

## Zadavanje širine u uređivaču

1. Pritisnite [Uredi] i odaberite sliku u vizualnom prikazu.
2. U alatnoj traci odaberite širinu u [Širina slike].
3. Pritisnite [Spremi].

| Mogućnost | Širina |
|---|---|
| [Automatski] | Nije zadano (automatsko prilagođavanje) |
| [Mala (360px)] | 360px |
| [Srednja (560px)] | 560px |
| [Velika (760px)] | 760px |
| [Širina teksta (920px)] | 920px |
| [Prilagođeno…] | Bilo koji cijeli broj od 16 do 4096px |

## Zadavanje širine u Markdownu

HTML oznaci `img` zadajte brojčanu vrijednost `width`. Taj se zapis jednako prikazuje i na GitHubu i u MDX-u.

```html
<img src="./images/screen.png" alt="Zaslon s postavkama" width="360" />
```

> **Napomena**
>
> - U `width` se upisuje samo broj, bez `px` ili `%`. Vrijednost veća od širine teksta pri prikazu se ipak uklapa u širinu teksta.
> - Putanje slika navode se relativno u odnosu na dokument. Slike izvan korijena dokumentacije ne prikazuju se.

## Povezane teme

- [Uređivanje dokumenta](README.md)
- [Dijagrami, matematički izrazi ili slike ne prikazuju se](../07-troubleshooting/rendering.md)
