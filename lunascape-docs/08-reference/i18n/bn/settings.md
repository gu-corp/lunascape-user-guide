# VS Code সেটিংস

VS Code-এর সেটিংসে (`⌘,` / `Ctrl+,`) "Lunascape Docs" খুঁজলে নিচের বিষয়গুলো পরিবর্তন করা যায়। এগুলো সবই ব্যবহারকারীভিত্তিক সেটিংস এবং প্রকল্পের নথিতে সংরক্ষিত হয় না।

## ডকুমেন্টেশন রুট

| সেটিং | মান | ডিফল্ট | কাজ |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` খোলা Markdown নথির সবচেয়ে কাছের ডকুমেন্টেশন রুট নিজে থেকে বেছে নেয়, আর নথিটি কোনো রুটের অন্তর্ভুক্ত না হলে মূল ফোল্ডারটি সাময়িকভাবে খোলে। `fixed` সবসময় `root`-এ থাকা ডকুমেন্টেশন রুট খোলে |
| `lunascapeDocEditor.rootDirectoryNames` | স্ট্রিং-এর অ্যারে | `["docs"]` | `auto` মোডে ডকুমেন্টেশন রুট হিসেবে স্বয়ংক্রিয়ভাবে খুঁজে নেওয়া ফোল্ডারের নাম। যে ফোল্ডারে `lunascape-docs.json` আছে, নাম নির্বিশেষে সেটি খুঁজে নেওয়া হয়। রিপোজিটরির সরাসরি নিচে থাকা `lunascape-docs.json`-এ `defaultFolder` বা `roots` থাকলে সেটিই অগ্রাধিকার পায় |
| `lunascapeDocEditor.root` | পাথ | `docs` | `fixed` মোডে, অথবা কমান্ড থেকে খোলার সময় ব্যবহৃত, ওয়ার্কস্পেস-সাপেক্ষ ডকুমেন্টেশন রুট |
| `lunascapeDocEditor.startPage` | পাথ | `README.md` | ডকুমেন্টেশন রুট-সাপেক্ষ শুরুর পৃষ্ঠা |
| `lunascapeDocEditor.title` | স্ট্রিং | `Lunascape Docs` | নথির ট্যাবের শিরোনাম প্রতিস্থাপন করে। ডকুমেন্টেশন রুট নির্বাচনের নামে এর প্রভাব পড়ে না |
| `lunascapeDocEditor.ignoredDirectories` | স্ট্রিং-এর অ্যারে | `["99-archive"]` | INDEX থেকে বাদ দেওয়া ফোল্ডারের নাম |

## প্রদর্শন

| সেটিং | মান | ডিফল্ট | কাজ |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` সাদা পটভূমি ব্যবহার করে, `auto` VS Code-এর রঙবিন্যাস অনুসরণ করে |
| `lunascapeDocEditor.locale` | ভাষা ট্যাগ | নেই | সুলভ হলে অগ্রাধিকার দিয়ে দেখানো হবে এমন আপনার ব্যক্তিগত নথির ভাষা। এটি প্রকল্পের মূল নথির ভাষা বদলায় না |
| `lunascapeDocEditor.documentMetadata.compact` | বুলিয়ান | `true` | H1-এর ঠিক পরের নথি-ব্যবস্থাপনা টেবিলটিকে "নথির তথ্য" সারিতে গুটিয়ে রাখে |
| `lunascapeDocEditor.tree.showFileNames` | বুলিয়ান | `false` | INDEX-এ নথির নামের বদলে ফাইলের নাম দেখায় |
| `lunascapeDocEditor.tree.showDocumentIcons` | বুলিয়ান | `false` | INDEX-এ নথির আইকন দেখায় |
| `lunascapeDocEditor.tree.showFolderIcons` | বুলিয়ান | `false` | INDEX-এ ফোল্ডারের আইকন দেখায় |
| `lunascapeDocEditor.tree.showItemCounts` | বুলিয়ান | `false` | INDEX-এ প্রতিটি ফোল্ডারের সরাসরি নিচের আইটেমের সংখ্যা দেখায় |
| `lunascapeDocEditor.tree.showGuides` | বুলিয়ান | `true` | INDEX-এ স্তরবিন্যাসের নির্দেশক রেখা দেখায় |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | INDEX-এর সারির ব্যবধান |
| `lunascapeDocEditor.tree.autoHideSingleItem` | বুলিয়ান | `true` | নথি মাত্র একটি হলে INDEX শুধু প্রথমবার বন্ধ করে |

## সম্পাদনা

| সেটিং | মান | ডিফল্ট | কাজ |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | এখনো বদল না করা পর্যন্ত ব্যবহৃত সম্পাদনার প্রদর্শন। সবশেষে ব্যবহৃত প্রদর্শনই অগ্রাধিকার পায় |
| `lunascapeDocEditor.editor.showEditButton` | বুলিয়ান | `true` | নথির নিচে ডান দিকে [সম্পাদনা] দেখায় |

## চিত্র

| সেটিং | মান | ডিফল্ট | কাজ |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | TikZ-এর রেন্ডারিং রানটাইম। `bundled` সঙ্গে দেওয়া অনুমোদিত রানটাইম ব্যবহার করে (বর্তমান বিতরণ সংস্করণে এটি অন্তর্ভুক্ত নেই), `workspace` বিশ্বস্ত ওয়ার্কস্পেসের সরাসরি নিচে থাকা `node-tikzjax` 1.0.5 ব্যবহার করে (শুধু উন্নয়ন ও মূল্যায়নের জন্য), `disabled` কিছুই আঁকে না |

## অনুমোদিত নয় এমন সেটিংস

| সেটিং | এর বদলে যা ব্যবহার করবেন |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `lunascape-docs.json`-এর `defaultLocale` |
| `lunascapeDocEditor.locales` | `lunascape-docs.json`-এর `locales` |

ব্যক্তিগত সেটিংস দিয়ে প্রকল্পের ভাষা প্রতিস্থাপন করা যায় না।

## সম্পর্কিত বিষয়

- [প্রদর্শন সেটিংস পরিবর্তন করা](../02-reading/display-settings.md)
- [প্রকল্পের কনফিগারেশন](../04-document-tools/project-configuration.md)
