# הגדרות VS Code

חיפוש "Lunascape Docs" בהגדרות VS Code (`⌘,` / `Ctrl+,`) מאפשר לשנות את הפריטים הבאים. כולם הגדרות אישיות לכל משתמש ואינם נשמרים במסמכי הפרויקט.

## שורש התיעוד

| הגדרה | ערכים | ברירת מחדל | תפקיד |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` בוחר אוטומטית את שורש התיעוד הקרוב ביותר לקובץ ה‑Markdown שנפתח, ואם הקובץ אינו שייך לאף שורש — פותח זמנית את תיקיית האב. `fixed` פותח תמיד את שורש התיעוד שב‑`root` |
| `lunascapeDocEditor.rootDirectoryNames` | מערך של מחרוזות | `["docs"]` | שמות התיקיות שיתגלו אוטומטית כשורש התיעוד במצב `auto`. תיקייה שיש בה `lunascape-docs.json` מתגלה ללא קשר לשמה. כאשר ב‑`lunascape-docs.json` שבראש המאגר קיים `defaultFolder` או `roots`, יש להם עדיפות |
| `lunascapeDocEditor.root` | נתיב | `docs` | שורש התיעוד היחסי לסביבת העבודה, במצב `fixed` או בעת פתיחה מתוך פקודה |
| `lunascapeDocEditor.startPage` | נתיב | `README.md` | דף הפתיחה, יחסית לשורש התיעוד |
| `lunascapeDocEditor.title` | מחרוזת | `Lunascape Docs` | דורס את כותרת לשונית המסמך. אינו משפיע על שם שורש התיעוד בבורר |
| `lunascapeDocEditor.ignoredDirectories` | מערך של מחרוזות | `["99-archive"]` | שמות תיקיות שיוצאו מ‑INDEX |

## תצוגה

| הגדרה | ערכים | ברירת מחדל | תפקיד |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` מציג רקע לבן, `auto` עוקב אחר ערכת הצבעים של VS Code |
| `lunascapeDocEditor.locale` | תג שפה | ללא | שפת המסמך האישית שתוצג בעדיפות כאשר היא זמינה. אינה משנה את שפת המקור של הפרויקט |
| `lunascapeDocEditor.documentMetadata.compact` | ערך בוליאני | `true` | מקפל את טבלת ניהול המסמך שמיד אחרי ה‑H1 לשורת "פרטי המסמך" |
| `lunascapeDocEditor.tree.showFileNames` | ערך בוליאני | `false` | מציג ב‑INDEX את שמות הקבצים במקום שמות המסמכים |
| `lunascapeDocEditor.tree.showDocumentIcons` | ערך בוליאני | `false` | מציג ב‑INDEX סמלי מסמכים |
| `lunascapeDocEditor.tree.showFolderIcons` | ערך בוליאני | `false` | מציג ב‑INDEX סמלי תיקיות |
| `lunascapeDocEditor.tree.showItemCounts` | ערך בוליאני | `false` | מציג ב‑INDEX את מספר הפריטים שמתחת לכל תיקייה |
| `lunascapeDocEditor.tree.showGuides` | ערך בוליאני | `true` | מציג ב‑INDEX קווי הנחיה להיררכיה |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | ריווח השורות ב‑INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | ערך בוליאני | `true` | כאשר קיים מסמך אחד בלבד, סוגר את INDEX בפעם הראשונה |

## עריכה

| הגדרה | ערכים | ברירת מחדל | תפקיד |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | תצוגת העריכה כל עוד לא החלפת תצוגה. לתצוגה שבה השתמשת לאחרונה יש עדיפות |
| `lunascapeDocEditor.editor.showEditButton` | ערך בוליאני | `true` | מציג את [עריכה] בפינה הימנית התחתונה של גוף המסמך |

## תרשימים

| הגדרה | ערכים | ברירת מחדל | תפקיד |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | סביבת הריצה לשרטוט TikZ. `bundled` היא סביבת הריצה המאושרת המצורפת (אינה מצורפת לגרסת ההפצה הנוכחית), `workspace` היא `node-tikzjax` 1.0.5 שמתחת לשורש של סביבת עבודה מהימנה (לפיתוח ולהערכה בלבד), ו‑`disabled` אינו משרטט כלל |

## הגדרות שאינן מומלצות

| הגדרה | מה להשתמש במקומה |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` שב‑`lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` שב‑`lunascape-docs.json` |

אי אפשר לדרוס את שפות הפרויקט באמצעות הגדרות אישיות.

## נושאים קשורים

- [שינוי הגדרות התצוגה](../02-reading/display-settings.md)
- [הגדרות הפרויקט](../04-document-tools/project-configuration.md)
