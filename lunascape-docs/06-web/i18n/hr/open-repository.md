# Otvaranje repozitorija s GitHuba

U web-verziji repozitorij s GitHuba možete otvoriti i čitati izravno, bez kloniranja. Za javne repozitorije prijava nije potrebna.

## Otvaranje sa zaslona

1. Pritisnite [Otvori dokumente] (ikona mape) na alatnoj traci. Otvara se zaslon „Otvori dokumente“.
2. U lijevom stupcu odaberite mjesto s kojeg želite otvarati.

   | Mjesto | Što se prikazuje |
   |---|---|
   | Sve | Sve navedeno ispod. Nedavno otvoreno prikazuje se prvo |
   | Nedavno otvoreno | Repozitoriji i mape koje ste dosad otvorili |
   | Preporučeno | Priručnici koje stranica preporučuje |
   | GitHub repozitoriji | Kada ste prijavljeni putem GitHuba, repozitoriji koje možete čitati |
   | Ovo računalo | Mape na ovom uređaju |

3. Pritisnite [Otvori] u retku koji želite otvoriti. Upisom u [Filtriraj po nazivu dokumenta ili repozitorija] na vrhu možete suziti popis redaka.

Repozitorij kojeg nema na popisu navedite putem [Unesi owner/repo i otvori] u lijevom stupcu.

> **Savjet**
>
> - Na popisu su GitHub repozitoriji na kojima je instalirana GitHub aplikacija „Lunascape Docs“ i za koje imate dopuštenje za čitanje. Ako repozitorij ne vidite, zamolite njegova vlasnika da doda aplikaciju.

## Provjera lokacije dokumenta

Mala ikona na lijevoj strani alatne trake (oznaka lokacije) pokazuje gdje se nalazi dokument koji trenutačno čitate.

| Ikona | Lokacija |
|---|---|
| Oznaka GitHuba | Čitate s GitHuba. Dokument nije spremljen na ovom uređaju |
| Mapa | Mapa na ovom uređaju |

Pritiskom na ikonu prikazuju se lokacija, stanje i radnje koje odande možete izvesti ([Prikaži na GitHubu], [Kopiraj poveznicu] i dr.).

## Otvaranje putem URL-a

Adresa redom navodi repozitorij i položaj dokumenta. Putanja je položaj unutar repozitorija, pa je redoslijed isti kao u URL-u na GitHubu.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Što navodite | Zapis |
|---|---|
| Samo repozitorij (zadana grana) | `/github/owner/repo` |
| Dokument unutar repozitorija | `/github/owner/repo/docs/01-product/vision.md` |
| Određena grana ili oznaka | Na kraj dodajte `?ref=v1.2.0` |

Kada prijeđete na drugu stranicu, mijenja se i adresa. Pritiskom na [Podijeli ovaj dokument] na alatnoj traci možete nekome dati poveznicu na stranicu koju trenutačno čitate. Možete upotrebljavati i gumbe preglednika [Natrag] i [Naprijed].

Stariji oblik `?source=` i dalje se otvara kao i dosad. Nakon otvaranja adresa se prepisuje u novi oblik.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Napomena**
>
> - Bez prijave vrijedi ograničenje upotrebe GitHub API-ja (60 zahtjeva na sat). Za repozitorije s mnogo dokumenata ili za opetovano čitanje pritisnite [Prijava putem GitHuba].
> - Nazivi grana koji sadrže `/` (npr. `feature/xxx`) mogu se navesti pomoću `?ref=` u gornjem obliku adrese. U obliku `?source=` ne mogu se zapisati.
> - Dokumenti se učitavaju s GitHub dopuštenjima čitatelja. Osobe bez dopuštenja za čitanje ne vide ih.

## Otvaranje dokumenata iz lokalne mape

Pritisnite [Otvori dokumente] na alatnoj traci, a zatim putem [Otvori dokumente iz lokalne mape] u lijevom stupcu odaberite mapu na uređaju. Datoteke se obrađuju unutar preglednika i nikamo se ne šalju. Ova mogućnost radi u preglednicima koji podržavaju odabir mape (Chrome, Edge i dr.).

## Povezane teme

- [Čitanje privatnog repozitorija](private-repository.md)
- [Web-verzija se ne otvara ili prijava ne uspijeva](../07-troubleshooting/web.md)
