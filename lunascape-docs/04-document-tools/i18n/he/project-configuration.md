# הגדרות הפרויקט

הקובץ `lunascape-docs.json` שנמצא ישירות תחת שורש התיעוד הוא הגדרת שורש התיעוד המשותפת לצוות. הוא מנוהל ב‑Git.

## יצירה ועריכה של קובץ ההגדרות

- בסרגל הכלים לחצו על [כלי מסמכים] ← לשונית [בדיקה] ← [מקור הכללים והגדרות המסמכים] ← [עריכת הגדרות המסמכים], והקובץ ייפתח ב‑VS Code. אם הקובץ אינו קיים, נוצר באותו רגע קובץ התחלתי.
- לשם הקובץ `lunascape-docs.json` משויך אוטומטית ה‑JSON Schema המצורף, ולכן מוצגים השלמה אוטומטית והסבר לכל פריט. אין צורך לכתוב `$schema`.

## דוגמה להגדרות

```json
{
  "id": "product-docs",
  "title": "תיעוד המוצר",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## הסבר הפריטים

| פריט | תוכן | ברירת מחדל |
|---|---|---|
| `id` | המפתח שתחתיו נשמרות הגדרות התצוגה של כל משתמש. קבעו מזהה קבוע כאשר רוצים לשמור על ההגדרות גם לאחר העברת התיקייה | נתיב התיקייה |
| `title` | השם המוצג בקצה סרגל הכלים וברשימת שורשי התיעוד. אינו משתנה עם החלפת שפת התצוגה | הכותרת של README/index בשורש, ואם אין — שם התיקייה |
| `indexTitle` | הכותרת של INDEX | `INDEX` |
| `startPage` | המסמך שנפתח ראשון (נתיב יחסי לשורש התיעוד) | `README.md` |
| `appearance` | ערכת הצבעים: `light` (בהיר תמיד) או `auto` (עוקב אחר ערכת הנושא של VS Code) | `light` |
| `defaultLocale` | שפת ברירת המחדל (שפת מסמך המקור). מצוינת כתג שפה לפי BCP 47 (‏`ja`, `en`, `zh-Hant` וכדומה). היא מקור התרגום | לא מוגדר (מוסק מהטקסט לצורך התצוגה) |
| `fallbackLocale` | השפה שתוצג תחילה לקוראים ששפת סביבתם אינה תואמת לאף אחת מהשפות הנתמכות. ציינו שפה הכלולה ב‑`locales` | לא מוגדר (נעשה שימוש ב‑`defaultLocale`) |
| `locales` | רשימת השפות הנתמכות. כוללת את `defaultLocale`. הן מופיעות בתפריט השפות ומשמשות כיעדי התרגום | `defaultLocale` בלבד |
| `ignoredDirectories` | שמות תיקיות שיוחרגו מ‑INDEX, מהחיפוש ומהבדיקות. ציון הערך מחליף את ברירת המחדל | `["99-archive"]` |
| `tree` | ערכי ברירת המחדל לתצוגת INDEX. המשתמשים יכולים לעקוף אותם בהגדרות התצוגה | כמו בדוגמה שלמעלה |
| `editor.defaultMode` | תצוגת העריכה כל עוד המשתמש לא החליף בעצמו: `visual` או `source` | `visual` |
| `editor.showEditButton` | האם להציג את [עריכה] בפינה הימנית התחתונה של גוף המסמך | `true` |
| `documentStandards.pack` | ה‑Standard Pack המשמש לבדיקת המסמכים ולתבניות: `builtin:<שם>` או נתיב יחסי לשורש התיעוד | אין |
| `documentStandards.profile` | שם פרופיל המוגדר על ידי ה‑Pack | אין |
| `translation.enabled` | מפעיל יצירת הצעות תרגום ותרגום מרוכז | `true` |
| `translation.contextFiles` | קובצי Markdown של מסמך המקור (נתיב יחסי לשורש התיעוד) הנמסרים בעת התרגום כאסמכתה למונחים ולסגנון | `[]` |
| `translation.maxContextCharacters` | המגבלה על סך התווים של מסמכי האסמכתה (מרבי 1048576) | `49152` |
| `description` | תיאור בשורה אחת של אוסף המסמכים. מוצג בכרטיס שבדף הבית של המאגר. כמו `title`, אפשר לכתוב מחרוזת או אובייקט לפי שפה | אין |

## איך לציין היכן נמצאים המסמכים במאגר

בקובץ `lunascape-docs.json` שהונח ישירות תחת המאגר אפשר לכתוב **מפה של המאגר** במקום הגדרות של אותה תיקייה. כתיבת אחד משלושת הפריטים הבאים הופכת אותו למפה, והתיקייה עצמה אינה נעשית שורש תיעוד.

| פריט | תוכן | ברירת מחדל |
|---|---|---|
| `defaultFolder` | באיזו תיקייה נמצאים המסמכים (נתיב יחסי לתיקייה זו). התיקייה שאליה הוא מצביע אינה זקוקה לקובץ הגדרות | אין (נעשה שימוש ב‑`docs`) |
| `roots` | רשימת אוספי המסמכים כאשר יש כמה מהם (נתיבים יחסיים לתיקייה זו, לפי סדר התצוגה). במקרה זה התיקייה עצמה נעשית דף הבית | אין |
| `excludes` | תיקיות שיוחרגו מגילוי שורשי התיעוד (נתיבים יחסיים לתיקייה זו). מתווספות להחרגות ברירת המחדל כגון `node_modules` | `[]` |
| `home.cards` | האם להציג בדף הבית, מתחת ל‑README, כרטיסים של אוספי המסמכים. אם אתם כותבים את הקישורים בעצמכם ב‑README, קבעו `false` | `true` |

שורש התיעוד נקבע בסדר הבא. מלמעלה למטה, נעשה שימוש בראשון שנמצא.

1. תיקייה שצוינה בהגדרה או בפקודה
2. היעד שאליו מצביעים `defaultFolder` או `roots` שבקובץ `lunascape-docs.json` שמתחת למאגר
3. תיקייה שיש בה `lunascape-docs.json` (אם יש שתיים או יותר תחת הורה משותף, ההורה הזה נעשה דף הבית)
4. תיקיית `docs` (‏`lunascapeDocEditor.rootDirectoryNames`)
5. המאגר עצמו, ישירות

> **טיפ**
>
> אם לא כותבים דבר, פועל סעיף 4, ולכן מאגר רגיל שיש בו `docs/` אחד מתנהג כמו קודם. כתבו `defaultFolder` רק כאשר רוצים ששם התיקייה יהיה `manual`.

### דוגמה למפה

```json
{
  "title": "עזרה של Lunascape",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## סדר העדיפויות של ההגדרות

הפריטים הנוגעים לתצוגה מקבלים עדיפות בסדר הבא.

1. הגדרות התצוגה של המשתמש (החלונית [הגדרות תצוגה])
2. הגדרות VS Code (‏`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. ערכי ברירת המחדל של המוצר

השפות (‏`defaultLocale`, `fallbackLocale`, `locales`) הן היוצא מן הכלל: `lunascape-docs.json` הוא הקובע. אי אפשר לעקוף את שפות הפרויקט באמצעות הגדרות אישיות של VS Code.

> **שימו לב**
>
> אפשר לציין Standard Pack גם בקובץ `docs-lint.config.json` תחת `standard`. אם הוא מופיע בשניהם, `docs-lint.config.json` גובר.

## נושאים קשורים

- [שינוי כללי הבדיקה](rules.md)
- [שינוי הגדרות התצוגה](../02-reading/display-settings.md)
- [רשימת הגדרות VS Code](../08-reference/settings.md)
