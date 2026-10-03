# Uređivanje dokumenta

Dokumente možete uređivati izravno u pregledniku. Zaslon za uređivanje ima „vizualni prikaz”, u kojem uređujete ono što vidite, i „prikaz Markdown izvora”; između njih se prebacuje jednim gumbom.

## Početak uređivanja

Pritisnite bilo koju od sljedećih mogućnosti. Sve otvaraju isti zaslon za uređivanje.

- [Uredi] u donjem desnom kutu teksta
- [⋯] (Ostale radnje) u gornjem desnom kutu teksta → [Uredi]
- Izbornik stavke u INDEX-u → [Uredi]

## Uređivanje

1. Uredite tekst izravno.
   Alatna traka na vrhu zaslona za uređivanje nudi format odlomka (tekst, naslovi 1–4, citat, kod), [Podebljano], [Kurziv], [Popis s oznakama], [Numerirani popis], [Poveznica], [Umetni tablicu], [Širina slike], [Poništi] i [Ponovi].
2. Kada želite izravno urediti Markdown izvor, pritisnite [Markdown].
   Ponovnim pritiskom vraćate se na vizualni prikaz. Zadnji korišteni prikaz pamti se i vraća sljedeći put kada pritisnete [Uredi].
3. Pritisnite [Spremi] (spremiti možete i s Ctrl+S / ⌘S).
   Zapisuje se u Markdown datoteku i vraćate se na prikaz za čitanje. Kada želite prekinuti uređivanje i vratiti se na zadnji spremljeni sadržaj, pritisnite [Discard edits].

## Uvijek započni na zaslonu za uređivanje (način rada za uređivanje)

Pritisnite [Edit mode] na alatnoj traci i uključite ga: nakon toga svaki se dokument otvara na zaslonu za uređivanje. Koristite ga kada pišete kao u bilježnici.

- Dok je uključen, pritisak na [Spremi] ne zatvara zaslon za uređivanje. [Discard edits] vraća na zadnji spremljeni sadržaj, a zaslon za uređivanje ostaje otvoren.
- Ponovnim pritiskom isključuje se i vraćate se na prikaz za čitanje. Uključeno/isključeno stanje pamti se za svakog korisnika.
- Ne prikazuje se na korijenu dokumentacije u koji nije moguće pisati (primjerice, GitHub izvor namijenjen samo za čitanje).

## Nespremljene izmjene

Izmjene koje niste spremili automatski se čuvaju na ovom uređaju. Ne gube se ni kada prijeđete na drugi dokument, ni kada zatvorite karticu ili prozor.

- [Unsaved] na zaslonu za uređivanje znači da se tekst razlikuje od zadnjeg spremljenog sadržaja.
- Sljedeći put kada otvorite isti dokument, nastavljate od sačuvanih izmjena i o tome dobivate obavijest. Ako je u međuvremenu izvorni dokument ažuriran, i o tome dobivate obavijest. Pomoću [Discard edits] možete se vratiti na najnoviji sadržaj.
- Sačuvane izmjene nestaju pritiskom na [Spremi] ili [Discard edits]. Budući da nisu spremljene, ne pojavljuju se u Gitu ni među nacrtima.

> **Napomena**
>
> - Spremanje samo zapisuje datoteku. Git staging i commit nikada se ne izvode automatski.
> - Matematički izrazi i dijagrami poput Mermaida, TikZ-a i Vega-Litea u vizualnom se prikazu prikazuju iscrtani. Da biste promijenili njihov sadržaj, prebacite se na [Markdown].
> - Dokumenti koji sadrže sintaksu specifičnu za MDX (komponente, `import` i slično) uređuju se samo u Markdown prikazu, radi očuvanja te sintakse.
> - Front matter (blok omeđen `---` linijama na vrhu) čuva se i kada uređujete u vizualnom prikazu.

> **Savjet**
>
> - [VS Codeで開く] (Otvori u VS Code) otvara datoteku u uobičajenom uređivaču teksta. Spremanjem ondje automatski se ažurira i prikaz u pregledniku.
> - Kada ne želite prikazivati gumb [Uredi], isključite [Gumb za uređivanje] u [Postavke prikaza]. Da biste ga sakrili za cijeli projekt, postavite `editor.showEditButton` na `false` u `lunascape-docs.json`.
> - Zadani prikaz koji se prvi otvara (vizualni / Markdown) možete promijeniti postavkom `lunascapeDocEditor.editor.defaultMode` ili postavkom `editor.defaultMode` u `lunascape-docs.json`.

## Povezane teme

- [Stvaranje i organiziranje dokumenata i mapa](organize.md)
- [Prilagodba veličine slika](images.md)
- [Pisanje matematičkih izraza](math.md)
- [Pisanje dijagrama i grafikona](diagrams.md)
