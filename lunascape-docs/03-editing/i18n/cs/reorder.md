# Změna pořadí dokumentů

Pořadí zobrazené v INDEX lze změnit přetažením myší nebo z klávesnice. Nové pořadí se uloží do front matter dokumentu jako `navigation.order`.

## Změna pořadí přetažením

1. Přetáhněte dokument nebo složku v INDEX.
2. Upusťte jej před nebo za sousední položku, případně na složku.
   V rámci jedné úrovně se změní pořadí. Upuštěním na jinou složku se položka přesune do této složky.

## Změna pořadí klávesnicí nebo z nabídky

- Zaměřte položku v INDEX a stiskněte `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- V nabídce položky zvolte [Posunout nahoru] / [Posunout dolů].

## Co se ukládá

- Při změně pořadí v rámci jedné úrovně se aktualizuje `navigation.order` ve front matter originálu. U složky se zapisuje do souboru `README.md` dané složky; pokud složka žádný nemá, vytvoří se `README.md` obsahující pouze front matter.
- Při přesunu do jiné složky se originál přesune společně s příslušnými překlady. Před přesunem se zobrazí dotaz na potvrzení, protože může dojít k ovlivnění relativních odkazů.
- Příprava změn do Gitu (staging) ani potvrzení (commit) se neprovádí.

> **Poznámka**
>
> - Pořadí nelze měnit během filtrování, při úpravách dokumentu a v nedůvěryhodném pracovním prostoru.
> - Zpráva „INDEX byl aktualizován“ znamená, že právě byla uplatněna jiná změna.操作 zopakujte.
> - Úvodní stránku nelze přesunout do jiné složky.

> **Tip**
>
> Když hodnotám `navigation.order` přidělíte kroky po 100, například 100, 200, 300, můžete později snadno vkládat dokumenty mezi ně. Podrobnosti najdete v části [Nastavení navigačních metadat](../04-document-tools/navigation-metadata.md).

## Související témata

- [Vytváření a uspořádání dokumentů a složek](organize.md)
- [Nastavení navigačních metadat](../04-document-tools/navigation-metadata.md)
