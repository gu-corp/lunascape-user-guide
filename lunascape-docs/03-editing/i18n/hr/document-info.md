# Prikazivanje podataka o dokumentu

„Tablica upravljanja dokumentom" na vrhu dokumenta (ID dokumenta, verzija, datum ažuriranja, status i slično) pri čitanju se sažima u mali redak „Podaci o dokumentu". Sam Markdown ostaje obična tablica, pa se jednako čita i na GitHubu.

## Uvjeti za prikaz

Neposredno iza naslova (H1) postavite ovakvu tablicu s dva stupca.

```markdown
# Definicija funkcionalnih zahtjeva

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Uvjet je da tablica sadrži redak s ID-om dokumenta i više stavki upravljanja.
- Prepoznaje se i tablica postavljena ispod naslova `## 文書管理` ili `## Document information`.
- Tablice usred teksta i uobičajene tablice „stavka/sadržaj" ne pretvaraju se.

## Način prikaza

- Pri čitanju se sitnim slovima prikazuju samo status i datum ažuriranja.
- Pritisnite redak da biste prikazali sve stavke.
- Pri ispisu prikazuju se sve stavke.
- Na zaslonu za uređivanje tablica se prikazuje kao obična tablica i može se tako uređivati.

> **Savjet**
>
> Ako želite da se podaci uvijek prikazuju kao tablica, bez sažimanja, isključite [Sažmi podatke o dokumentu] u [Postavke prikaza].

## Povezane teme

- [Uređivanje dokumenta](README.md)
- [Promjena postavki prikaza](../02-reading/display-settings.md)
