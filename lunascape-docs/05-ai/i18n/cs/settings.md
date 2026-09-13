# Nastavení AI

Vyberte AI a model, kterým předáte svou práci. Tato obrazovka používá vlastní rozevírací seznamy, nikoli rychlý výběr VS Code.

1. Stiskněte [Nástroje dokumentů] → kartu [AI] → [Nastavení AI…].
2. V poli [Poskytovatel] vyberte poskytovatele.
   Poskytovatelé, které toto prostředí nemůže použít, se zobrazí jako nevolitelní i s uvedením důvodu.
3. V poli [Model] vyberte model. Nabídka se liší podle poskytovatele.
4. Zavřete obrazovku. Volba se uloží pro každého uživatele zvlášť a použije se i příště.

## Poskytovatelé

| Poskytovatel | Podoba | Způsob zjištění |
|---|---|---|
| Claude Code | Relace | Přítomnost příkazu `claude` |
| Codex | Relace | Přítomnost příkazu `codex` |
| Jazykové modely VS Code | API | Modely registrované v rozhraní VS Code Language Model API |
| Anthropic API | API | Registrovaný klíč API |
| API kompatibilní s OpenAI | API | Registrovaný klíč API a koncový bod |

Poskytovatel typu **relace** si sám čte a zapisuje soubory a sám spouští kontrolu dokumentu. Výsledky zapisuje přímo do pracovního stromu a prohlížíte si je v rozdílu Git.

Poskytovatel typu **API** vrátí Markdown jednoho dokumentu a rozšíření před uložením ukáže rozdíl.

## Registrace klíče API

Anthropic API a API kompatibilní s OpenAI lze používat po registraci klíče API.

1. V poli [Poskytovatel] vyberte, kam klíč zaregistrovat. Zobrazí se pole pro zadání klíče API.
2. Zadejte [Klíč API]. U API kompatibilního s OpenAI zadejte také [Koncový bod] (například `https://api.openai.com/v1`).
3. Stiskněte [Uložit]. Zobrazí se „Klíč zaregistrován“.

> **Poznámka**
>
> - Klíče se ukládají do úložiště SecretStorage ve VS Code a znovu se nezobrazují. Nezapisují se ani do souboru `settings.json`, ani do dokumentů. Odstranit je lze pomocí [Odstranit klíč].
> - Seznam modelů se získává od jednotlivých služeb pomocí zaregistrovaného klíče. Dokud jej nelze získat, zobrazuje se známý seznam.
> - Poskytovatel typu API umí provést pouze úkony „Přeložit tuto stránku“ a „Zkontrolovat tuto stránku“. Procházení více dokumentů a vytváření dokumentů provádějte poskytovatelem typu relace.

> **Tip**
>
> Pokud se nenajde žádný poskytovatel, nainstalujte Claude Code nebo Codex, případně zaregistrujte klíč API. Po opětovném otevření [Nastavení AI…] bude zjištěn.

## Související témata

- [Předání práce AI](README.md)
- [Přehled nastavení VS Code](../08-reference/settings.md)
