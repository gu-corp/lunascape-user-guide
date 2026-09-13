# إعدادات VS Code

ابحث عن «Lunascape Docs» في إعدادات VS Code (`⌘,` / `Ctrl+,`) لتغيير العناصر التالية. جميعها إعدادات خاصة بكل مستخدم ولا تُحفظ في مستندات المشروع.

## جذر التوثيق

| الإعداد | القيم | الافتراضي | الوظيفة |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | يختار `auto` تلقائيًا أقرب جذر توثيق إلى ملف Markdown المفتوح، وإن لم يكن تابعًا لأي جذر فتح المجلد الأصل مؤقتًا. ويفتح `fixed` دائمًا جذر التوثيق المحدّد في `root` |
| `lunascapeDocEditor.rootDirectoryNames` | مصفوفة نصوص | `["docs"]` | أسماء المجلدات التي تُكتشف تلقائيًا كجذور توثيق في وضع `auto`. ويُكتشف المجلد الذي يحتوي على `lunascape-docs.json` بصرف النظر عن اسمه. وإذا وُجد `defaultFolder` أو `roots` في ملف `lunascape-docs.json` الموجود مباشرةً تحت المستودع، فلهما الأولوية |
| `lunascapeDocEditor.root` | مسار | `docs` | جذر التوثيق النسبي إلى مساحة العمل، في وضع `fixed` أو عند الفتح من أمر |
| `lunascapeDocEditor.startPage` | مسار | `README.md` | صفحة البداية النسبية إلى جذر التوثيق |
| `lunascapeDocEditor.title` | نص | `Lunascape Docs` | يستبدل عنوان تبويب المستند. ولا يؤثر في اسم جذر التوثيق المعروض في أداة الاختيار |
| `lunascapeDocEditor.ignoredDirectories` | مصفوفة نصوص | `["99-archive"]` | أسماء المجلدات المستبعدة من INDEX |

## العرض

| الإعداد | القيم | الافتراضي | الوظيفة |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | يستخدم `light` خلفية بيضاء، ويتبع `auto` ألوان VS Code |
| `lunascapeDocEditor.locale` | وسم لغة | لا شيء | لغة المستند الشخصية التي تُعرض بالأولوية عند توفرها. ولا تُغيّر لغة المستند الأصلي في المشروع |
| `lunascapeDocEditor.documentMetadata.compact` | قيمة منطقية | `true` | يطوي جدول إدارة المستند الذي يلي العنوان H1 في سطر «معلومات المستند» |
| `lunascapeDocEditor.tree.showFileNames` | قيمة منطقية | `false` | يعرض أسماء الملفات بدل أسماء المستندات في INDEX |
| `lunascapeDocEditor.tree.showDocumentIcons` | قيمة منطقية | `false` | يعرض أيقونات المستندات في INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | قيمة منطقية | `false` | يعرض أيقونات المجلدات في INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | قيمة منطقية | `false` | يعرض عدد العناصر الموجودة مباشرةً داخل كل مجلد في INDEX |
| `lunascapeDocEditor.tree.showGuides` | قيمة منطقية | `true` | يعرض خطوط دليل المستويات في INDEX |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | تباعد الأسطر في INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | قيمة منطقية | `true` | يغلق INDEX مرة واحدة فقط عندما يوجد مستند واحد فقط |

## التحرير

| الإعداد | القيم | الافتراضي | الوظيفة |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | عرض التحرير المستخدم قبل أي تبديل. وللعرض المستخدم آخر مرة الأولوية |
| `lunascapeDocEditor.editor.showEditButton` | قيمة منطقية | `true` | يعرض [تحرير] أسفل يمين المستند |

## الرسوم التخطيطية

| الإعداد | القيم | الافتراضي | الوظيفة |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | بيئة تشغيل رسم TikZ. يستخدم `bundled` بيئة التشغيل المعتمدة المرفقة (غير مرفقة في الإصدار الموزّع الحالي)، ويستخدم `workspace` حزمة `node-tikzjax` 1.0.5 الموجودة مباشرةً تحت مساحة عمل موثوقة (للتطوير والتقييم فقط)، ولا يرسم `disabled` شيئًا |

## الإعدادات الملغاة

| الإعداد | ما يُستخدم بدلًا منه |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` في `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` في `lunascape-docs.json` |

لا يمكن تجاوز لغات المشروع بالإعدادات الشخصية.

## مواضيع ذات صلة

- [تغيير إعدادات العرض](../02-reading/display-settings.md)
- [إعدادات المشروع](../04-document-tools/project-configuration.md)
