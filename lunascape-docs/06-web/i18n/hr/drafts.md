# Spremanje skica

Kada dokument uređujete u Web pregledniku, promjene se ne zapisuju u repozitorij, nego se spremaju unutar preglednika kao „skica”.

## Izrada skice

1. Otvorite dokument i pritisnite [Uredi] u donjem desnom kutu.
2. Uredite dokument i pritisnite [Spremi].
   Prikazuje se poruka „Spremljeno kao skica” i promjena se pohranjuje u pregledniku.

- Dokumenti sa skicom označeni su značkom u INDEX-u. Iznad teksta prikazuje se poruka „Ovaj dokument je skica na ovom uređaju (nije objavljen)”.
- [Skice] na alatnoj traci prikazuje broj skica, a pritiskom se otvara popis skica.

## Odbacivanje skice

- Da biste odbacili skicu pojedinog dokumenta, pritisnite [Odbaci skicu] iznad teksta.
- Da biste odbacili sve skice, poslužite se popisom skica.

## Prijenos u repozitorij

„Zahtjev za objavu”, koji skice šalje kao Pull Request, implementiran je, ali nije omogućen u javnom pregledniku. Za promjene u repozitoriju uredite dokument u VS Code verziji ili u lokalnoj kopiji.

> **Napomena**
>
> - Skice se spremaju u pregledniku (IndexedDB). Ne prenose se u drugi preglednik ni na drugi uređaj. Brisanjem podataka web-mjesta u pregledniku brišu se i skice.
> - Ako se dokument u repozitoriju promijeni nakon što ste izradili skicu, prikazuje se poruka „Izvor je ažuriran”. Provjerite sadržaj pa odlučite hoćete li skicu odbaciti ili je zadržati.
> - Ako uređujete lokalnu mapu otvorenu preko [Otvori dokumente], promjene se spremaju izravno u datoteku ako to preglednik podržava. U preglednicima koji to ne podržavaju promjene se čuvaju samo tijekom te sesije.

## Povezane teme

- [Što omogućuje Web verzija](README.md)
- [Uređivanje dokumenta](../03-editing/README.md)
