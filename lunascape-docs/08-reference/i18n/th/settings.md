# การตั้งค่า VS Code

ค้นหา "Lunascape Docs" ในการตั้งค่าของ VS Code (`⌘,` / `Ctrl+,`) เพื่อเปลี่ยนรายการต่อไปนี้ ทั้งหมดเป็นการตั้งค่าเฉพาะผู้ใช้ และจะไม่ถูกบันทึกลงในเอกสารของโครงการ

## รากเอกสาร

| การตั้งค่า | ค่า | ค่าเริ่มต้น | หน้าที่ |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` จะเลือกรากเอกสารที่ใกล้ที่สุดกับไฟล์ Markdown ที่เปิดโดยอัตโนมัติ และถ้าไฟล์นั้นไม่อยู่ในรากเอกสารใดเลย จะเปิดโฟลเดอร์แม่ไว้ชั่วคราว ส่วน `fixed` จะเปิดรากเอกสารที่ระบุใน `root` เสมอ |
| `lunascapeDocEditor.rootDirectoryNames` | อาร์เรย์ของสตริง | `["docs"]` | ชื่อโฟลเดอร์ที่จะค้นพบเป็นรากเอกสารโดยอัตโนมัติในโหมด `auto` โฟลเดอร์ที่มี `lunascape-docs.json` จะถูกค้นพบไม่ว่าชื่อใดก็ตาม หากใน `lunascape-docs.json` ที่อยู่ใต้ที่เก็บโดยตรงมี `defaultFolder` หรือ `roots` ค่าดังกล่าวจะมาก่อน |
| `lunascapeDocEditor.root` | เส้นทาง | `docs` | รากเอกสารแบบสัมพัทธ์กับพื้นที่ทำงาน สำหรับโหมด `fixed` หรือเมื่อเปิดจากคำสั่ง |
| `lunascapeDocEditor.startPage` | เส้นทาง | `README.md` | หน้าเริ่มต้นแบบสัมพัทธ์กับรากเอกสาร |
| `lunascapeDocEditor.title` | สตริง | `Lunascape Docs` | เขียนทับชื่อแท็บเอกสาร ไม่มีผลต่อชื่อที่ใช้เลือกรากเอกสาร |
| `lunascapeDocEditor.ignoredDirectories` | อาร์เรย์ของสตริง | `["99-archive"]` | ชื่อโฟลเดอร์ที่จะไม่แสดงใน INDEX |

## การแสดงผล

| การตั้งค่า | ค่า | ค่าเริ่มต้น | หน้าที่ |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` ใช้พื้นหลังสีขาว ส่วน `auto` จะตามชุดสีของ VS Code |
| `lunascapeDocEditor.locale` | แท็กภาษา | ไม่มี | ภาษาของเอกสารส่วนตัวที่จะแสดงก่อนเมื่อมีให้ใช้ ไม่เปลี่ยนภาษาต้นฉบับของโครงการ |
| `lunascapeDocEditor.documentMetadata.compact` | บูลีน | `true` | ย่อตารางจัดการเอกสารที่อยู่ถัดจาก H1 ให้เหลือบรรทัด "ข้อมูลเอกสาร" |
| `lunascapeDocEditor.tree.showFileNames` | บูลีน | `false` | แสดงชื่อไฟล์แทนชื่อเอกสารใน INDEX |
| `lunascapeDocEditor.tree.showDocumentIcons` | บูลีน | `false` | แสดงไอคอนเอกสารใน INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | บูลีน | `false` | แสดงไอคอนโฟลเดอร์ใน INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | บูลีน | `false` | แสดงจำนวนรายการที่อยู่ใต้โฟลเดอร์โดยตรงใน INDEX |
| `lunascapeDocEditor.tree.showGuides` | บูลีน | `true` | แสดงเส้นนำสายตาของลำดับชั้นใน INDEX |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | ระยะห่างระหว่างบรรทัดของ INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | บูลีน | `true` | ปิด INDEX เฉพาะครั้งแรก เมื่อมีเอกสารเพียงรายการเดียว |

## การแก้ไข

| การตั้งค่า | ค่า | ค่าเริ่มต้น | หน้าที่ |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | มุมมองการแก้ไขที่ใช้เมื่อยังไม่ได้สลับ มุมมองที่ใช้ล่าสุดจะมาก่อน |
| `lunascapeDocEditor.editor.showEditButton` | บูลีน | `true` | แสดง [แก้ไข] ที่มุมขวาล่างของเนื้อหา |

## แผนภาพ

| การตั้งค่า | ค่า | ค่าเริ่มต้น | หน้าที่ |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | รันไทม์สำหรับวาด TikZ โดย `bundled` คือรันไทม์ที่ผ่านการรับรองซึ่งมาพร้อมกับตัวโปรแกรม (ไม่ได้รวมมาในรุ่นที่เผยแพร่ปัจจุบัน) `workspace` คือ `node-tikzjax` 1.0.5 ที่อยู่ใต้พื้นที่ทำงานที่เชื่อถือได้โดยตรง (สำหรับการพัฒนาและประเมินผลเท่านั้น) ส่วน `disabled` จะไม่วาด |

## การตั้งค่าที่เลิกใช้แล้ว

| การตั้งค่า | ใช้สิ่งนี้แทน |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` ใน `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` ใน `lunascape-docs.json` |

การตั้งค่าส่วนตัวไม่สามารถเขียนทับภาษาของโครงการได้

## หัวข้อที่เกี่ยวข้อง

- [การเปลี่ยนการตั้งค่าการแสดงผล](../02-reading/display-settings.md)
- [การตั้งค่าโครงการ](../04-document-tools/project-configuration.md)
