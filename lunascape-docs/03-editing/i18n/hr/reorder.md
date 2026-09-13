# Promjena redoslijeda dokumenata

Redoslijed prikazan u INDEX-u možete promijeniti povlačenjem i ispuštanjem ili tipkovnicom. Promijenjeni redoslijed sprema se u front matter dokumenta kao `navigation.order`.

## Promjena redoslijeda povlačenjem i ispuštanjem

1. Povucite dokument ili mapu u INDEX-u.
2. Ispustite ga ispred ili iza stavke iste razine ili na mapu.
   Unutar iste razine mijenja se redoslijed. Ispuštanjem na drugu mapu stavka se premješta u tu mapu.

## Promjena redoslijeda tipkovnicom ili izbornikom

- Postavite fokus na stavku u INDEX-u i pritisnite `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- U izborniku stavke odaberite [Pomakni prema gore] / [Pomakni prema dolje].

## Što se sprema

- Kod promjene redoslijeda unutar iste razine ažurira se `navigation.order` u front matteru izvornika. Kod mapa upisuje se u datoteku `README.md` te mape. U mapi koja nema `README.md` stvara se `README.md` koji sadrži samo front matter.
- Kod premještanja u drugu mapu izvornik se premješta zajedno s pripadajućim prijevodima. Prije premještanja prikazuje se potvrda jer to može utjecati na relativne poveznice.
- Git staging i commit se ne izvode.

> **Napomena**
>
> - Promjena redoslijeda nije moguća tijekom filtriranja, tijekom uređivanja dokumenta i u radnom prostoru koji nije pouzdan.
> - Poruka „INDEX je ažuriran” znači da je upravo primijenjena druga promjena. Ponovite postupak.
> - Početna stranica ne može se premjestiti u drugu mapu.

> **Savjet**
>
> Ako vrijednosti za `navigation.order` dodjeljujete u koracima od 100, primjerice 100, 200, 300, kasnije je lako umetnuti dokumente između njih. Pojedinosti potražite u [Postavljanje navigacijskih metapodataka](../04-document-tools/navigation-metadata.md).

## Povezane teme

- [Stvaranje i organiziranje dokumenata i mapa](organize.md)
- [Postavljanje navigacijskih metapodataka](../04-document-tools/navigation-metadata.md)
