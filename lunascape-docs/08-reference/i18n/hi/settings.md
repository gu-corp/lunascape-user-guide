# VS Code सेटिंग्स

VS Code की सेटिंग्स (`⌘,` / `Ctrl+,`) में "Lunascape Docs" खोजने पर आप निम्नलिखित मदों को बदल सकते हैं। ये सभी प्रति-उपयोगकर्ता सेटिंग्स हैं और प्रोजेक्ट के दस्तावेज़ों में सहेजी नहीं जातीं।

## दस्तावेज़ रूट

| सेटिंग | मान | डिफ़ॉल्ट | कार्य |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` खुली हुई Markdown फ़ाइल के सबसे निकट के दस्तावेज़ रूट को अपने आप चुनता है, और यदि वह किसी में न हो तो मूल फ़ोल्डर को अस्थायी रूप से खोलता है। `fixed` हमेशा `root` वाला दस्तावेज़ रूट खोलता है |
| `lunascapeDocEditor.rootDirectoryNames` | स्ट्रिंग की सूची | `["docs"]` | `auto` में दस्तावेज़ रूट के रूप में स्वतः खोजे जाने वाले फ़ोल्डर नाम। जिस फ़ोल्डर में `lunascape-docs.json` हो, वह नाम पर ध्यान दिए बिना खोजा जाता है। रिपॉज़िटरी के सबसे ऊपर मौजूद `lunascape-docs.json` में `defaultFolder` या `roots` होने पर उसे प्राथमिकता मिलती है |
| `lunascapeDocEditor.root` | पथ | `docs` | `fixed` मोड में, या कमांड से खोलते समय, कार्यस्थान के सापेक्ष दस्तावेज़ रूट |
| `lunascapeDocEditor.startPage` | पथ | `README.md` | दस्तावेज़ रूट के सापेक्ष आरंभिक पृष्ठ |
| `lunascapeDocEditor.title` | स्ट्रिंग | `Lunascape Docs` | दस्तावेज़ टैब का शीर्षक बदल देता है। दस्तावेज़ रूट के चयन नाम पर इसका असर नहीं पड़ता |
| `lunascapeDocEditor.ignoredDirectories` | स्ट्रिंग की सूची | `["99-archive"]` | INDEX से बाहर रखे जाने वाले फ़ोल्डर नाम |

## प्रदर्शन

| सेटिंग | मान | डिफ़ॉल्ट | कार्य |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` सफ़ेद पृष्ठभूमि रखता है, `auto` VS Code की रंग-योजना का अनुसरण करता है |
| `lunascapeDocEditor.locale` | भाषा टैग | कोई नहीं | उपलब्ध होने पर प्राथमिकता से दिखाई जाने वाली आपकी निजी दस्तावेज़ की भाषा। यह प्रोजेक्ट की प्रामाणिक भाषा को नहीं बदलती |
| `lunascapeDocEditor.documentMetadata.compact` | बूलियन | `true` | H1 के ठीक बाद की दस्तावेज़ प्रबंधन तालिका को "दस्तावेज़ जानकारी" की पंक्ति में समेट देता है |
| `lunascapeDocEditor.tree.showFileNames` | बूलियन | `false` | INDEX में दस्तावेज़ नाम के बजाय फ़ाइल नाम दिखाता है |
| `lunascapeDocEditor.tree.showDocumentIcons` | बूलियन | `false` | INDEX में दस्तावेज़ आइकन दिखाता है |
| `lunascapeDocEditor.tree.showFolderIcons` | बूलियन | `false` | INDEX में फ़ोल्डर आइकन दिखाता है |
| `lunascapeDocEditor.tree.showItemCounts` | बूलियन | `false` | INDEX में प्रत्येक फ़ोल्डर के सीधे अंतर्गत मदों की संख्या दिखाता है |
| `lunascapeDocEditor.tree.showGuides` | बूलियन | `true` | INDEX में पदानुक्रम की मार्गदर्शक रेखाएँ दिखाता है |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | INDEX की पंक्ति-दूरी |
| `lunascapeDocEditor.tree.autoHideSingleItem` | बूलियन | `true` | दस्तावेज़ केवल एक होने पर INDEX को पहली बार बंद कर देता है |

## संपादन

| सेटिंग | मान | डिफ़ॉल्ट | कार्य |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | जब तक आप बदलते नहीं, तब तक का संपादन दृश्य। अंतिम बार उपयोग किया गया दृश्य प्राथमिकता पाता है |
| `lunascapeDocEditor.editor.showEditButton` | बूलियन | `true` | दस्तावेज़ के नीचे दाईं ओर [संपादित करें] दिखाता है |

## आरेख

| सेटिंग | मान | डिफ़ॉल्ट | कार्य |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | TikZ का रेंडरिंग रनटाइम। `bundled` साथ दिए गए स्वीकृत रनटाइम का उपयोग करता है (वर्तमान वितरित संस्करण में यह शामिल नहीं है), `workspace` विश्वसनीय कार्यस्थान के सीधे अंतर्गत मौजूद `node-tikzjax` 1.0.5 का उपयोग करता है (केवल विकास और मूल्यांकन के लिए), `disabled` कुछ भी नहीं बनाता |

## अनुशंसित नहीं की गईं सेटिंग्स

| सेटिंग | इसके बदले उपयोग करें |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `lunascape-docs.json` में `defaultLocale` |
| `lunascapeDocEditor.locales` | `lunascape-docs.json` में `locales` |

निजी सेटिंग्स से प्रोजेक्ट की भाषाओं को बदला नहीं जा सकता।

## संबंधित विषय

- [दृश्य सेटिंग्स बदलना](../02-reading/display-settings.md)
- [प्रोजेक्ट कॉन्फ़िगरेशन](../04-document-tools/project-configuration.md)
