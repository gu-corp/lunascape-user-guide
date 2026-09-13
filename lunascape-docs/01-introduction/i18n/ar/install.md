# تثبيت الامتداد

يُوزَّع امتداد VS Code «Lunascape Docs Pro» على هيئة ملف VSIX. وهو مجاني؛ وتشير كلمة «Pro» إلى الإصدار الذي يُسلّم العمل إلى الذكاء الاصطناعي ويُحدّث نفسه بنفسه.

## متطلبات التشغيل

- VS Code 1.90 أو أحدث
- الميزات التي تكتب الملفات — إنشاء المستندات، وتنظيم INDEX، وحفظ إعدادات الفحص، والترجمة — لا تعمل إلا في مساحة عمل موثوقة قمت بتعيينها كذلك في VS Code.

## التثبيت

1. احصل على ملف VSIX. يشير هذا الرابط دائمًا إلى أحدث إصدار.

   [تنزيل lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. افتح عرض الامتدادات (`⇧⌘X` / `Ctrl+Shift+X`).
3. اختر [التثبيت من VSIX...] من قائمة `…` في أعلى اليمين، ثم حدّد الملف الذي نزّلته.

### من سطر الأوامر

سطر واحد، إن كنت تفضّل عدم مغادرة الطرفية. يقوم بالتنزيل والتثبيت معًا.

macOS / Linux:

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell):

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **ملاحظة**
> إذا لم يُعثر على `code`، فنفّذ [أمر الصدفة: تثبيت الأمر 'code' في PATH] من لوحة الأوامر (`⇧⌘P` / `Ctrl+Shift+P`).

## التحديث

عند نشر إصدار أحدث، يجلبه الامتداد ويثبّته بنفسه. يعرض VS Code إعادة تحميل النافذة، وعندئذٍ تبدأ باستخدامه. وتبقى إعداداتك ومستنداتك كما هي.

يتحقق مرة واحدة في اليوم. للتحقق الآن، نفّذ [Lunascape Docs: التحقق من وجود إصدار أحدث] من لوحة الأوامر (`⇧⌘P` / `Ctrl+Shift+P`).

يغيّر الإعداد `lunascapeDocEditor.update.check` ما يحدث.

| الإعداد | ما يحدث |
|---|---|
| تثبيت إصدار أحدث عند نشره | الافتراضي |
| أخبرني، ودعني أقرر في كل مرة | يظهر إشعار، ولا يتغيّر شيء حتى تضغط [تحديث] |
| عدم التحقق | لا يحدث شيء |

### عندما يتعذّر التحديث

ظهور «تعذّر جلب التحديث: No Servers» يعني أن الإصدار المثبَّت هو 0.22.18 أو أقدم. إذ يفشل مسار التحديث فيه عند الخطوة الأخيرة في كل مرة، فلا يمكنه الانتقال بنفسه إلى إصدار أحدث. ثبّته يدويًا مرة واحدة كما هو موضّح أعلاه؛ وبعد ذلك يحدّث نفسه بنفسه.

## التحقق من الإصدار

افتح «Lunascape Docs Pro» في عرض الامتدادات لترى الإصدار المثبَّت. ستحتاج إليه عند الإبلاغ عن مشكلة.

## مواضيع ذات صلة

- [إنشاء مستنداتك الأولى](first-documents.md)
- [الإبلاغ عن مشكلة](../07-troubleshooting/report.md)
