# تنظیمات VS Code

در تنظیمات VS Code (`⌘,` / `Ctrl+,`) عبارت «Lunascape Docs» را جست‌وجو کنید تا موارد زیر را تغییر دهید. همهٔ این‌ها تنظیمات شخصی هر کاربر هستند و در اسناد پروژه ذخیره نمی‌شوند.

## ریشهٔ مستندات

| تنظیم | مقدار | پیش‌فرض | کارکرد |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` نزدیک‌ترین ریشهٔ مستندات به فایل Markdown بازشده را به‌طور خودکار انتخاب می‌کند و اگر فایل به هیچ ریشه‌ای تعلق نداشته باشد، پوشهٔ والد آن را موقتاً باز می‌کند. `fixed` همیشه ریشهٔ مستنداتِ `root` را باز می‌کند |
| `lunascapeDocEditor.rootDirectoryNames` | آرایه‌ای از رشته‌ها | `["docs"]` | نام پوشه‌هایی که در حالت `auto` به‌عنوان ریشهٔ مستندات به‌طور خودکار کشف می‌شوند. پوشه‌ای که `lunascape-docs.json` دارد، صرف‌نظر از نامش کشف می‌شود. اگر `lunascape-docs.json` در ریشهٔ مخزن دارای `defaultFolder` یا `roots` باشد، آن‌ها اولویت دارند |
| `lunascapeDocEditor.root` | مسیر | `docs` | ریشهٔ مستندات نسبت به فضای کاری، برای حالت `fixed` یا هنگام باز کردن از طریق فرمان |
| `lunascapeDocEditor.startPage` | مسیر | `README.md` | صفحهٔ آغازین، نسبت به ریشهٔ مستندات |
| `lunascapeDocEditor.title` | رشته | `Lunascape Docs` | عنوان زبانهٔ سند را بازنویسی می‌کند. بر نام انتخابی ریشهٔ مستندات اثری ندارد |
| `lunascapeDocEditor.ignoredDirectories` | آرایه‌ای از رشته‌ها | `["99-archive"]` | نام پوشه‌هایی که از INDEX کنار گذاشته می‌شوند |

## نمایش

| تنظیم | مقدار | پیش‌فرض | کارکرد |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` پس‌زمینهٔ سفید است و `auto` از طرح رنگ VS Code پیروی می‌کند |
| `lunascapeDocEditor.locale` | برچسب زبان | ندارد | زبان سندِ شخصی شما که در صورت موجود بودن با اولویت نمایش داده می‌شود. زبان مرجع پروژه را تغییر نمی‌دهد |
| `lunascapeDocEditor.documentMetadata.compact` | بولی | `true` | جدول مدیریت سند را که بلافاصله پس از H1 می‌آید، در سطر «اطلاعات سند» جمع می‌کند |
| `lunascapeDocEditor.tree.showFileNames` | بولی | `false` | در INDEX به‌جای نام سند، نام فایل را نشان می‌دهد |
| `lunascapeDocEditor.tree.showDocumentIcons` | بولی | `false` | نقشک سندها را در INDEX نشان می‌دهد |
| `lunascapeDocEditor.tree.showFolderIcons` | بولی | `false` | نقشک پوشه‌ها را در INDEX نشان می‌دهد |
| `lunascapeDocEditor.tree.showItemCounts` | بولی | `false` | شمار موارد مستقیم زیر هر پوشه را در INDEX نشان می‌دهد |
| `lunascapeDocEditor.tree.showGuides` | بولی | `true` | خطوط راهنمای سلسله‌مراتب را در INDEX نشان می‌دهد |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | فاصلهٔ سطرهای INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | بولی | `true` | وقتی فقط یک سند وجود دارد، INDEX را تنها برای نخستین بار می‌بندد |

## ویرایش

| تنظیم | مقدار | پیش‌فرض | کارکرد |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | نمای ویرایش، تا زمانی که آن را عوض نکرده‌اید. نمایی که آخرین بار به کار رفته است اولویت دارد |
| `lunascapeDocEditor.editor.showEditButton` | بولی | `true` | [ویرایش] را در پایین‌ِ متن نشان می‌دهد |

## نمودار

| تنظیم | مقدار | پیش‌فرض | کارکرد |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | زمان اجرای ترسیم TikZ. `bundled` زمان اجرای تأییدشدهٔ همراه است (در نسخهٔ توزیعی کنونی همراه نیست)، `workspace` از `node-tikzjax` نسخهٔ ۱٫۰٫۵ در ریشهٔ فضای کاری مورد اعتماد استفاده می‌کند (فقط برای توسعه و ارزیابی) و `disabled` چیزی ترسیم نمی‌کند |

## تنظیمات منسوخ

| تنظیم | جایگزین |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` در `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` در `lunascape-docs.json` |

با تنظیمات شخصی نمی‌توان زبان‌های پروژه را بازنویسی کرد.

## موضوعات مرتبط

- [تغییر تنظیمات نمایش](../02-reading/display-settings.md)
- [پیکربندی پروژه](../04-document-tools/project-configuration.md)
