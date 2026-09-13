# Stvaranje dokumenta iz predloška

Na kartici [Stvori] u Alatima za dokumente odaberete predložak, pregledate sadržaj i zatim stvorite novi dokument.

1. Na alatnoj traci pritisnite [Alati za dokumente] i otvorite karticu [Stvori].
2. Pritisnite [Stvori iz predloška] i odaberite predložak.
3. Ispunite polja za unos (naslov, sažetak i slično). Uz obavezna polja piše „Obavezno”.
4. Unesite odredište kao putanju relativnu u odnosu na korijen dokumentacije (primjerice `03-design/api.md`).
5. Pritisnite [Pregled] i provjerite generirani Markdown.
6. Pritisnite [Stvori ovo].
   Dokument se stvara i prikazuje u pregledniku. Zatim se provjerava cijeli korijen dokumentacije.

## Dostupni predlošci

| Predložak | Sadržaj |
|---|---|
| Jednostranični dokument | Kratka specifikacija, bilješka ili samostalan opisni dokument u jednoj datoteci |
| Specifikacija, priručnik, pomoć | Jedna datoteka s općenitom strukturom poglavlja prikladnom za specifikaciju, priručnik ili pomoć |
| Predlošci Standard Packa | Kada je u datoteci `lunascape-docs.json` odabran Standard Pack, dodaju se vrste dokumenata dopuštene tim profilom (specifikacija zahtjeva, projektna dokumentacija i slično) |

> **Napomena**
>
> - Za stvaranje je potreban pouzdani radni prostor.
> - Postojeće se datoteke ne prepisuju. Ako na odredištu već postoji dokument istog naziva, stvaranje nije moguće.
> - Odredište mora imati nastavak `.md` ili `.mdx`. Unutar mape `i18n` (gdje se nalaze prijevodi) nije moguće stvarati dokumente.
> - Nakon izmjene unosa ponovno pritisnite [Pregled] pa tek onda stvorite dokument.

> **Savjet**
>
> U projektu koji još nema mapu s dokumentima prvi skup možete stvoriti naredbom „Lunascape Docs: Stvori dokumentaciju iz predloška” u paleti naredbi. Pogledajte [Stvaranje prvih dokumenata](../01-introduction/first-documents.md).

## Povezane teme

- [Rad s Alatima za dokumente](README.md)
- [Promjena pravila provjere](rules.md)
