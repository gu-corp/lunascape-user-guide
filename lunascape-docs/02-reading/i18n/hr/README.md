# Osnovne radnje

Osnovne radnje od otvaranja dokumenata do dolaska na stranicu koju želite pročitati.

## Otvaranje dokumenata

1. Otvorite repozitorij u VS Code.
2. U paleti naredbi (`⇧⌘P` / `Ctrl+Shift+P`) pokrenite „Lunascape Docs: Otvori preglednik specifikacije”.
   Pronalazi se najbliži Korijen dokumentacije (prema zadanim postavkama mapa `docs`) i prikazuje se njegova početna stranica.

> **Savjet**
>
> - U pregledniku datoteka desnom tipkom miša kliknite Markdown datoteku i odaberite [Lunascape Docs: Otvori u pregledniku specifikacije] da biste počeli od te datoteke.
> - Ako otvorite Markdown datoteku koja ne pripada nijednom Korijenu dokumentacije, njezina se mapa privremeno prikazuje kao Korijen dokumentacije.

## Kretanje između stranica

| Radnja | Način |
|---|---|
| Otvaranje iz sadržaja | Pritisnite naziv dokumenta u INDEX-u s lijeve strane |
| Praćenje poveznice | Pritisnite poveznicu u tekstu. Otvara se u istom prikazu |
| Kretanje kroz povijest | [Natrag] i [Naprijed] na alatnoj traci ili `Alt`+`←` / `Alt`+`→` |
| Povratak na početnu stranicu | [Početna stranica specifikacije] na alatnoj traci |
| Jednu razinu više | [Nadređeni INDEX] na alatnoj traci ili stavka u navigacijskom tragu |
| Kretanje unutar stranice | Pritisnite naslov u odjeljku „Na ovoj stranici” s desne strane |

## Pretraživanje dokumenata

Upišite riječ u polje [Suzi popis dokumenata] iznad INDEX-a i prikazat će se samo dokumenti čiji se nazivi podudaraju. Obrišite unos da biste vratili cijeli popis.

## Osvježavanje sadržaja

Kada spremite Markdown datoteku u uređivaču VS Code, prikaz se ažurira automatski. Nakon izmjena vanjskim alatom pritisnite [Ponovno učitaj] na alatnoj traci.

> **Napomena**
>
> - Vanjske poveznice u tekstu (`https://` i slično) otvaraju se u zadanom pregledniku. Poveznice na datoteke izvan Korijena dokumentacije ne otvaraju se.
> - Dokumenti koje pregledavate obrađuju se na vašem uređaju. Ništa se ne šalje izvan uređaja radi čitanja dokumenta.

## Povezane teme

- [Korištenje INDEX-a](index-panel.md)
- [Promjena Korijena dokumentacije](roots.md)
- [Uređivanje dokumenta](../03-editing/README.md)
