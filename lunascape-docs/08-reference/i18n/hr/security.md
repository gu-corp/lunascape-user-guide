# Sigurnost i granice zapisivanja

Granice koje Lunascape Docs održava kako bi zaštitio vaše dokumente i vaš uređaj.

## Prikaz

- HTML generiran iz Markdowna i SVG generiran iz dijagrama pročišćavaju se pomoću DOMPurify 3.4.14 prije prikaza.
- Proizvoljne skripte sadržane u MDX-u nikada se ne izvršavaju.
- KaTeX se izvodi s `trust: false`, `maxSize: 50` i `maxExpand: 1000` te ne vjeruje ni vanjskom HTML-u ni proizvoljnim naredbama.
- Biblioteke za iscrtavanje Markmap, WaveDrom, Svgbob, Vega-Lite i Penrose učitavaju se lokalno, u fiksiranim verzijama, samo kada postoji odgovarajući blok. Upućivanja na vanjske resurse, neobrađeni HTML i izvršivi zapisi nisu dopušteni, a iz generiranog SVG-a uklanjaju se skripte, vanjske slike, `link`, `style` i `foreignObject`.
- Iscrtavanje TikZ-a ne pokreće LaTeX na domaćinu, nego se izvodi redom u WebAssembly TeX radniku s datotečnim sustavom u memoriji. Ograničeni su ulaz, red čekanja, memorija, vrijeme izvođenja (15 sekundi) i SVG izlaz, a naredbe za ulaz/izlaz datoteka se odbijaju.

## Pristup dokumentima i datotekama

- Poveznice u dokumentima i radnje s datotekama ne mogu izaći izvan Korijena dokumentacije.
- Stvaranje, preimenovanje, premještanje i brisanje iz INDEX-a proširenje ponovno provjerava prije primjene — Korijen dokumentacije, verziju INDEX-a, putanju Izvornika, vrstu odredišta, granice simboličkih veza i nespremljene dokumente. Zahtjevi iz zastarjelog izbornika ili iz drugog Korijena dokumentacije ne primjenjuju se.
- Tijekom uređivanja dokumenta ili primjene druge radnje nad INDEX-om, izmjene INDEX-a su onemogućene.
- Stvaranje iz Predloška nakon pretpregleda ponovno provjerava pouzdanost radnog prostora, identitet Korijena dokumentacije, verziju INDEX-a, Standard Pack i generirani sadržaj, odredište te granice simboličkih veza. Postojeća datoteka nikada se ne prepisuje i ne stvara se sadržaj koji se razlikuje od pretpregleda ili čiji raspakirani rezultat prelazi 4 MiB.
- Pri spremanju datoteke s postavkama neposredno prije spremanja provjerava se verzija, a ako se otkrije vanjska promjena, spremanje se prekida.

## Slanje izvan uređaja

- Dokumenti se nikada ne šalju izvan uređaja radi pregledavanja, uređivanja ili Provjere. Provjera dokumenata izvodi se lokalno i determinističkim postupkom.
- Jedino Prijevod (Prijevod ove stranice, skupni Prijevod) šalje dokumente jezičnom modelu, i to nakon što unaprijed prikaže odredište i opseg slanja te samo uz izričito odobrenje. <!-- ai-only -->
- Prijedlozi Prijevoda prikazuju se kao razlike, verzije Izvornika i odredišta Prijevoda ponovno se provjeravaju, a prijedlog se primjenjuje samo kada ga osoba izričito spremi. <!-- ai-only -->
- Alat za Specifikacije namijenjen AI agentima ne vraća sadržaj dokumenata, nazive radnih prostora ni lokalne putanje. <!-- ai-only -->

## Git

- Spremanje samo zapisuje datoteku. Nijedna značajka ne obavlja pripremu (staging) ni urezivanje u Git automatski.
- Postojeće datoteke poput `_meta.json` nikada se ne brišu niti mijenjaju bez obavijesti. Osamljene verzije Prijevoda također se ne brišu niti premještaju automatski.

## Povezane teme

- [Glavne specifikacije](README.md)
- [Korištenje putem AI-ja](ai-agents.md)
