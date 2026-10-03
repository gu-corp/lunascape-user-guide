# Otvaranje repozitorija s GitHuba

U web-inačici i u Lunascapeu repozitorij s GitHuba možete otvoriti i čitati izravno, bez dupliciranja. Za javne repozitorije prijava nije potrebna.

## Otvaranje sa zaslona

1. Na alatnoj traci pritisnite [Otvori dokumente] (ikona mape). Otvara se zaslon „Otvori dokumente”.
2. U lijevom stupcu odaberite mjesto s kojeg otvarate.

   | Mjesto | Što se prikazuje |
   |---|---|
   | Sve | Sve stavke iz redaka u nastavku. Nedavno otvorene stavke prikazuju se prve |
   | Nedavno otvoreno | Repozitoriji i mape koje ste dosad otvarali |
   | Preporučeno | Priručnici koje predstavlja web-mjesto |
   | Repozitoriji na GitHubu | Kada ste prijavljeni na GitHub, repozitoriji koje možete čitati |
   | Ovo računalo | Mape na ovom uređaju. U Lunascapeu se ovdje prikazuju i duplicirani repozitoriji |

3. Pritisnite [Otvori] u retku koji želite otvoriti. Ako upišete tekst u polje [Filtriraj po nazivu dokumenta ili repozitorija] na vrhu, popis redaka se sužava.

Repozitorij koji nije na popisu navedite pomoću [Unesi owner/repo i otvori] u lijevom stupcu.

> **Savjet**
>
> - Na popisu se prikazuju repozitoriji s GitHuba na kojima je instalirana GitHub aplikacija „Lunascape Docs” i za koje imate pravo čitanja. Ako repozitorij ne vidite, zamolite njegova vlasnika da doda aplikaciju.

## Utvrđivanje lokacije dokumenta

Mala ikona na lijevoj strani alatne trake (oznaka lokacije) pokazuje gdje se nalazi dokument koji čitate.

| Ikona | Lokacija |
|---|---|
| Oznaka GitHuba | Dokument čitate s GitHuba. Nije spremljen na ovom uređaju |
| Računalo | Mapa na ovom uređaju kojom upravlja Lunascape. Prikazuju se i naziv grane u Gitu te broj promijenjenih datoteka |
| Mapa | Mapa na ovom uređaju |

Pritiskom na ikonu prikazuju se lokacija, stanje i radnje dostupne odande (npr. [Prikaži na GitHubu], [Kopiraj poveznicu]).

## Dupliciranje repozitorija u Lunascapeu

U Lunascapeu repozitorij s GitHuba možete duplicirati na ovaj uređaj te u Gitu uređivati datoteke i izrađivati commitove.

- Na zaslonu „Otvori dokumente” pritisnite [Dupliciraj] u retku repozitorija.
- Dok čitate repozitorij otvoren s GitHuba, pritisnite oznaku lokacije, a zatim [Dupliciraj na ovo računalo]. Kad dupliciranje završi, isti se dokument otvara iz kopije na ovom uređaju.

Duplicirani repozitorij na popisu je označen s „Na ovom računalu”, a [Otvori na ovom računalu] prikazuje se prvo.

## Otvaranje putem URL-a

Adresa redom navodi repozitorij i položaj dokumenta. Putanja je položaj unutar repozitorija, pa je redoslijed isti kao u URL-u na GitHubu.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Što navodite | Oblik |
|---|---|
| Samo repozitorij (zadana grana) | `/github/owner/repo` |
| Dokument unutar repozitorija | `/github/owner/repo/docs/01-product/vision.md` |
| Određenu granu ili oznaku | Na kraj dodajte `?ref=v1.2.0` |

Kad prijeđete na drugu stranicu, mijenja se i adresa. Pritisnite [Podijeli ovaj dokument] na alatnoj traci da biste nekome dali poveznicu na stranicu koju čitate. Možete upotrebljavati i gumbe preglednika [Natrag] i [Naprijed].

Stari oblik `?source=` i dalje se otvara kao i dosad. Nakon otvaranja adresa se prepisuje u novi oblik.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Napomena**
>
> - Bez prijave vrijedi ograničenje korištenja GitHub API-ja (60 zahtjeva na sat). Za repozitorije s mnogo dokumenata ili za opetovano čitanje prijavite se pomoću [Prijava putem GitHuba].
> - Nazive grana koji sadrže `/` (npr. `feature/xxx`) možete navesti parametrom `?ref=` u gore opisanom obliku adrese. U obliku `?source=` to nije moguće.
> - Dokumenti se učitavaju s GitHub dopuštenjima čitatelja. Osobe bez prava čitanja ne vide ih.

## Otvaranje dokumenata iz lokalne mape

Na alatnoj traci pritisnite [Otvori dokumente], u lijevom stupcu pritisnite [Otvori dokumente iz lokalne mape] i odaberite mapu na uređaju. Datoteke se obrađuju unutar preglednika i ne šalju se nikamo. Ova mogućnost radi u preglednicima koji podržavaju odabir mape (Chrome, Edge i dr.).

## Povezane teme

- [Pregledavanje privatnog repozitorija](private-repository.md)
- [Web-inačica se ne otvara ili se ne možete prijaviti](../07-troubleshooting/web.md)
