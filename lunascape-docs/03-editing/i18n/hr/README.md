# Uređivanje dokumenta

Dokumente možete uređivati izravno u pregledniku. Zaslon za uređivanje ima vizualni prikaz, u kojem uređujete ono što vidite, i prikaz Markdown izvora; jedan gumb prebacuje između njih.

## Početak uređivanja

Pritisnite bilo što od sljedećeg. Sve otvara isti zaslon za uređivanje.

- [Uredi] u donjem desnom kutu teksta
- [⋯] (Ostale radnje) u gornjem desnom kutu teksta → [Uredi]
- Izbornik stavke u INDEX-u → [Uredi]

## Uređivanje

1. Uredite tekst izravno.
   Alatna traka pri vrhu zaslona za uređivanje nudi format odlomka (tekst, naslovi 1–4, citat, kôd), [Podebljano], [Kurziv], [Popis s oznakama], [Numerirani popis], [Poveznica], [Umetni tablicu], [Širina slike], [Poništi] i [Ponovi].
2. Kada želite izravno urediti Markdown izvor, pritisnite [Markdown].
   Ponovnim pritiskom vraćate se na vizualni prikaz. Posljednji upotrijebljeni prikaz pamti se i vraća sljedeći put kada pritisnete [Uredi].
3. Pritisnite [Spremi].
   Zapisuje se u datoteku Markdown i preglednik se vraća na prikaz za čitanje. Ako želite odustati, pritisnite [Odustani].

> **Napomena**
>
> - Spremanje samo zapisuje u datoteku. Pripremanje i urezivanje u Git ne izvode se automatski.
> - Matematički izrazi i dijagrami poput Mermaid, TikZ i Vega-Lite u vizualnom se prikazu prikazuju iscrtani. Za promjenu njihova sadržaja prijeđite na [Markdown].
> - Dokumenti koji sadrže sintaksu svojstvenu MDX-u (komponente, `import` i slično) uređuju se samo u prikazu Markdown, kako bi se ta sintaksa sačuvala.
> - Front matter (postavke na početku omeđene s `---`) čuva se i kada uređujete u vizualnom prikazu.

> **Savjet**
>
> - Pritiskom na [Otvori u VS Code] datoteku otvarate u običnom uređivaču teksta. Kada spremite u uređivaču teksta, prikaz u pregledniku automatski se ažurira.
> - Ako ne želite prikazivati gumb [Uredi], isključite [Gumb za uređivanje] u [Postavke prikaza]. Za skrivanje u cijelom projektu postavite `editor.showEditButton` u `lunascape-docs.json` na `false`.
> - Zadani prikaz pri prvom otvaranju (vizualni ili Markdown) mijenja se postavkom `lunascapeDocEditor.editor.defaultMode` ili postavkom `editor.defaultMode` u `lunascape-docs.json`.

## Povezane teme

- [Stvaranje i organiziranje dokumenata i mapa](organize.md)
- [Prilagodba veličine slika](images.md)
- [Pisanje matematičkih izraza](math.md)
- [Crtanje dijagrama i grafikona](diagrams.md)
