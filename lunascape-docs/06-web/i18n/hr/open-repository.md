# Otvaranje repozitorija na GitHubu

U web-verziji dokumente otvarate tako da navedete repozitorij na GitHubu. Za javne repozitorije prijava nije potrebna.

## Otvaranje sa zaslona

1. Otvorite <https://docs.lunascape.org/>.
2. Na alatnoj traci pritisnite [Otvori dokumente] (ikona mape).
3. U polje [Izravno navedi repozitorij] upišite repozitorij i pritisnite [Otvori].
   Kada ste prijavljeni na GitHub, možete birati i s popisa pod [Odaberi među repozitorijima koje možete čitati].

> **Savjet**
>
> - Ikona GitHuba pokraj nje otvara dokument koji trenutačno čitate na stranici github.com. To nije radnja otvaranja dokumenata.

## Otvaranje putem URL-a

Adresa jednostavno nabraja repozitorij i položaj dokumenta. Budući da je putanja položaj unutar repozitorija, redoslijed je isti kao u URL-u na GitHubu.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Što navodite | Oblik zapisa |
|---|---|
| Samo repozitorij (zadana grana) | `/github/owner/repo` |
| Dokument unutar repozitorija | `/github/owner/repo/docs/01-product/vision.md` |
| Grana ili oznaka | na kraj dodajte `?ref=v1.2.0` |

Kada prijeđete na drugu stranicu, mijenja se i adresa. Pritisnete li [Podijeli ovaj dokument] na alatnoj traci, možete nekome proslijediti poveznicu na stranicu koju čitate. Radi i preglednikov [Natrag] i [Naprijed].

I raniji oblik s `?source=` i dalje se otvara kao i dosad. Nakon otvaranja prepisuje se u novi oblik.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Napomena**
>
> - Ako niste prijavljeni, vrijedi ograničenje GitHubova API-ja (60 zahtjeva na sat). Za repozitorije s mnogo dokumenata ili za ponovljeno čitanje upotrijebite [Prijava putem GitHuba].
> - Nazivi grana koji sadrže `/` (na primjer `feature/xxx`) navode se pomoću `?ref=` u gornjem obliku adrese. U obliku s `?source=` ne mogu se zapisati.
> - Dokumenti se učitavaju s GitHub ovlastima samog čitatelja. Osobe bez prava čitanja neće ih vidjeti.

## Otvaranje dokumenata iz lokalne mape

Na alatnoj traci pritisnite [Otvori dokumente], zatim ispod popisa odaberite [Otvori dokumente iz lokalne mape] i odaberite mapu na svojem uređaju. Datoteke se obrađuju unutar preglednika i ne šalju se nikamo izvan njega. Radi u preglednicima koji podržavaju odabir mape (Chrome, Edge i drugi).

## Povezane teme

- [Pregledavanje privatnog repozitorija](private-repository.md)
- [Web-verzija se ne otvara ili prijava ne uspijeva](../07-troubleshooting/web.md)
