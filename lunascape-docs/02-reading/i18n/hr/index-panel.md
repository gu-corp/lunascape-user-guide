# Korištenje INDEX-a

INDEX s lijeve strane zaslona stablo je mapa i dokumenata u korijenu dokumentacije.

## Suzite popis

1. U polje [Suzi popis dokumenata] iznad INDEX-a upišite riječ.
2. Prikazuju se samo stavke čiji naziv odgovara. Izbrišete li unos, prikaz se vraća na prvobitan.

> **Napomena**
>
> Dok je popis sužen, promjena redoslijeda povlačenjem i ispuštanjem nije moguća.

## Proširite i sažmite mape

- Pritisnite strelicu lijevo od naziva mape ili naziv mape bez naslovnice da biste je proširili ili saželi.
- Mapa koja ima naslovnicu (`README.md` ili `index.md` s tekstom) otvara tu stranicu kada pritisnete njezin naziv. Za samo proširivanje ili sažimanje upotrijebite [Proširi mapu] / [Sažmi mapu] u izborniku stavke.
- Stanje proširenosti mapa pamti se za svakog korisnika i ne upisuje se u datoteke pod Git nadzorom.

## README i naslovnica mape

`README.md` je datoteka koja opisuje sadržaj svoje mape.

- Pritisnete li naziv mape koja ima README, prikazuje se taj README.
- Mapa koja ga nema prikazuje prvi dokument u sebi.
- Naslov (H1) datoteke README postaje naziv te mape u INDEX-u.

README nije obavezan. Da biste ga dodali naknadno, u izborniku stavke mape odaberite [Stvori README] (prikazuje se samo za mape koje ga nemaju).

## Prikažite ili sakrijte INDEX

- Lijeva ikona u prikazu stupaca na alatnoj traci prikazuje ili skriva INDEX. Desna ikona prikazuje ili skriva „Na ovoj stranici”.
- Na uskom zaslonu INDEX je na početku zatvoren. Pritisnete li [Otvori INDEX] (tri crte) lijevo od [Natrag], INDEX se otvara preko teksta dokumenta. Zatvorite ga pomoću [×] unutar INDEX-a, klikom na pozadinu, tipkom `Esc` ili prelaskom na drugi dokument. To privremeno otvaranje ne mijenja postavku za široke zaslone.
- U korijenu dokumentacije u kojem se prikazuje samo jedan dokument INDEX se automatski zatvara, i to samo prvi put. Ponovno ga otvorite ikonom u prikazu stupaca. To ponašanje možete isključiti opcijom [Sakrij kada postoji samo jedan dokument] u [Postavke prikaza].

## Koristite izbornik stavke

Izbornik stavke otvorite pomoću [⋯] koji se pojavi kada mišem prijeđete preko stavke u INDEX-u ili desnim klikom na stavku. Stavke su poredane ovim redoslijedom.

| Grupa | Stavke |
|---|---|
| Česte radnje | [Proširi mapu] / [Sažmi mapu], [Otvori INDEX] (otvara naslovnicu mape), [Uredi], [Promijeni naslov], [Otvori u VS Code], [Kopiraj putanju] |
| Stvaranje i organizacija | [Stvori README] (samo za mape koje ga nemaju), [Novi dokument], [Nova mapa], [Dupliciraj], [Promijeni naziv datoteke] / [Promijeni naziv mape], [Pomakni prema gore], [Pomakni prema dolje] |
| Brisanje | [Premjesti u smeće] |

- Za stvaranje izravno u korijenu dokumentacije pritisnite [⋯] na desnom kraju naslova INDEX-a ili desnom tipkom kliknite prazan dio INDEX-a pa odaberite [Novi dokument] ili [Nova mapa]. U istom su izborniku [Promijeni naziv dokumenta] i, ako korijen dokumentacije nema README, [Stvori README]. Isti se izbornik otvara i desnim klikom na naziv dokumenta na alatnoj traci.
- Unutar izbornika tipkama `↑` `↓` prelazite između stavki, a tipkama `Home` `End` na prvu i posljednju. Zatvorite li ga tipkom `Esc`, fokus se vraća na mjesto s kojeg je otvoren.

> **Napomena**
>
> Stavke za stvaranje, organizaciju i brisanje prikazuju se samo ako je radni prostor u VS Codeu pouzdan. Nisu dostupne ni tijekom uređivanja dokumenta ni dok je u tijeku druga radnja u INDEX-u.

## Promijenite izgled

U [Postavke prikaza] možete promijeniti prikaz naziva datoteka, ikone dokumenata i mapa, broj stavki u mapi, crte hijerarhije i gustoću prikaza. Pojedinosti potražite u [Promjena postavki prikaza](display-settings.md).

## Povezane teme

- [Stvaranje i organizacija dokumenata i mapa](../03-editing/organize.md)
- [Promjena redoslijeda dokumenata](../03-editing/reorder.md)
