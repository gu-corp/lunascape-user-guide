# התקנת התוסף

תוסף ה-VS Code "Lunascape Docs Pro" מופץ כקובץ VSIX. הוא חינמי; "Pro" מציין את המהדורה שמעבירה עבודה ל-AI ומעדכנת את עצמה.

## דרישות

- VS Code 1.90 ואילך
- תכונות שכותבות קבצים — יצירת מסמכים, ארגון ה-INDEX, שמירת הגדרות בדיקה, תרגום — פועלות רק בסביבת עבודה שסימנתם כמהימנה ב-VS Code.

## התקנה

1. השיגו את קובץ ה-VSIX. קישור זה מצביע תמיד על הגרסה הנוכחית.

   [הורדת lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. פתחו את תצוגת התוספים (`⇧⌘X` / `Ctrl+Shift+X`).
3. בחרו [התקנה מקובץ VSIX...] מתפריט ה-`…` בפינה הימנית העליונה, וציינו את הקובץ שהורדתם.

### משורת הפקודה

שורה אחת, אם אתם מעדיפים לא לצאת מהטרמינל. היא מורידה ומתקינה ברצף.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **הערה**
> אם `code` אינו נמצא, הריצו [פקודת מעטפת: התקן את הפקודה 'code' ב-PATH] מלוח הפקודות (`⇧⌘P` / `Ctrl+Shift+P`).

## עדכון

כשמתפרסמת גרסה חדשה יותר, התוסף משיג ומתקין אותה בעצמו. VS Code מציע לטעון מחדש את החלון, ואז אתם עוברים אליה. ההגדרות והמסמכים שלכם נשארים כפי שהם.

הבדיקה מתבצעת פעם ביום. כדי לבדוק מיד, הריצו [Lunascape Docs: בדוק גרסה חדשה יותר] מלוח הפקודות (`⇧⌘P` / `Ctrl+Shift+P`).

ההתנהגות ניתנת לשינוי בהגדרה `lunascapeDocEditor.update.check`.

| הגדרה | התנהגות |
|---|---|
| להתקין גרסה חדשה יותר כשמתפרסמת | ברירת המחדל |
| להודיע, ולתת לי להחליט בכל פעם | מופיעה הודעה, ודבר אינו משתנה עד שתלחצו [עדכון] |
| לא לבדוק | לא קורה דבר |

### כאשר לא ניתן לעדכן

אם מופיעה ההודעה "לא ניתן היה להשיג את העדכון: No Servers", הגרסה המותקנת היא 0.22.18 או ישנה יותר. תכונת העדכון של אותה גרסה נכשלת תמיד בצעד שאחרי ההשגה, ולכן היא אינה יכולה להתחדש בעצמה. התקינו ידנית פעם אחת לפי ההוראות שלמעלה. מכאן ואילך היא תתעדכן בעצמה.

## בדיקת הגרסה

פתחו את "Lunascape Docs Pro" בתצוגת התוספים כדי לראות את הגרסה המותקנת. תזדקקו לה בעת דיווח על תקלה.

## ראו גם

- [יצירת המסמכים הראשונים](first-documents.md)
- [דיווח על תקלה](../07-troubleshooting/report.md)
