# Book Art Direction & Editorial Design Standard v1.0

## Smart AI Product Builder — Complete Edition

**สถานะ:** Design Authority  
**อนุมัติใช้:** 19 กรกฎาคม 2569

เมื่อเอกสารเก่าขัดกับมาตรฐานนี้ ให้ใช้เอกสารนี้เป็นหลัก โดยห้ามตัด Canonical Course Scope

## 1. Design Concept

ภาพรวมต้อง Modern, Premium, Educational, Technology, Professional, Luxury และอ่านง่ายในระดับหนังสือคอมพิวเตอร์เชิงพาณิชย์ ไม่จัดหน้าเหมือนเอกสารราชการ คู่มือ Word, Documentation หรือ Markdown ดิบ

## 2. Part Color System

| Part | เนื้อหา | Color Token | Screen Reference | CMYK Working Value |
| --- | --- | --- | --- | --- |
| 1 | พื้นฐาน AI | PART-GREEN | `#0B6B4F` | C85 M25 Y70 K15 |
| 2 | Gem Builder | PART-ORANGE | `#D85B16` | C0 M70 Y95 K10 |
| 3 | Custom GPT | PART-BLUE | `#1554B8` | C90 M65 Y0 K5 |
| 4 | NotebookLM | PART-PURPLE | `#6C3DB8` | C65 M80 Y0 K0 |
| 5 | Chrome Extension | PART-CYAN | `#137DA8` | C85 M35 Y20 K5 |
| 6 | Google Apps Script | PART-TEAL | `#008579` | C90 M25 Y55 K10 |
| 7 | Codex | PART-RED | `#B52C35` | C20 M90 Y75 K10 |
| 8 | AI Business | PART-GOLD | `#B88912` | C20 M40 Y95 K10 |

ค่า CMYK เป็นค่าเริ่มต้น ต้องปรับจาก ICC Profile, กระดาษ และ Color Proof ของโรงพิมพ์

### Supplementary Tracks

- Single Web App Project: ใช้ Navy + Cyan และแสดงเป็น `PROJECT LAB`
- Workshop/Capstone: ใช้ Orange + Gold และแสดงเป็น `WORKSHOP & PROJECT`
- Appendices: ใช้ Slate + Green และแสดงเป็น `APPENDIX`

## 3. Top Ribbon Navigation

ทุกหน้ามี Ribbon ด้านบนแสดง PART 1–8 โดย Part ปัจจุบันมีขนาดใหญ่กว่า สีเต็ม และตัวอักษรเด่น ส่วน Part อื่นใช้ Tint ที่อ่านได้

- แสดงชื่อย่อเพื่อไม่ให้แน่นเกิน B5
- Project Lab, Workshop/Project และ Appendix ใช้ Tab เสริมท้าย Ribbon
- Ribbon ต้องไม่ชน Trim, Bleed, Header หรือพื้นที่อ่าน
- หน้าเปิดบทสามารถขยาย Ribbon เป็น Chapter Band ได้

## 4. Chapter Hero Page

ทุกบทเริ่มด้วยหน้าเต็ม ประกอบด้วยเลขบทขนาดใหญ่ ชื่อบท Hero Image/Illustration คนไทย Quote, Chapter Icon, Part Color, QR Placeholder และพื้นที่เลขหน้า

## 5. Content Rhythm

ห้ามมีข้อความยาวต่อเนื่องเกิน 1 หน้า ให้สลับ Prose, Image, Diagram, Infographic, Prompt, Workshop, Checklist และ Summary ตามหน้าที่ของเนื้อหา

## 6. Visual Requirement

ทุกหน้ามี Visual Anchor อย่างน้อย 1 จุด ได้แก่ ภาพคนไทย Screenshot, Diagram, Workflow, Mind Map, Architecture, Timeline, Table, Annotated Code, Icon หรือ Callout เชิงข้อมูล

ภาพบุคคลใช้บริบทไทยร่วมสมัย เช่น นักศึกษา ครู บุคลากรภาครัฐ/อปท. ผู้ประกอบการ นักพัฒนา สำนักงานและมหาวิทยาลัยไทย ตาม `SERIES/01_BASIC/THAI_VISUAL_GUIDE.md`

## 7. Infographic Minimum

ทุกบทมี Infographic อย่างน้อย 3 ชิ้น โดยเลือกจาก Workflow, Comparison, Timeline, Roadmap, Mind Map, Architecture หรือ Cycle ห้ามทำซ้ำข้อมูลเพื่อให้ครบจำนวน

## 8. Diagram Suite

ทุกบทมี Diagram Suite ครอบคลุม

1. System Diagram
2. Flow Diagram
3. Architecture Diagram
4. Data Flow
5. Prompt Flow

สามารถรวมหลาย Diagram เป็น Composite Spread ได้ แต่แต่ละ Diagram ต้องมีวัตถุประสงค์ Caption, Alt Text และไฟล์ต้นฉบับที่แก้ไขได้

## 9. Screenshot Standard

ทุก STEP มี Screenshot หรือภาพผลลัพธ์ พร้อมลูกศร วงกลม หมายเลข Caption, Highlight และวันที่ตรวจสอบ UI หากขั้นตอนเป็น CLI/Code ให้ใช้ Terminal/Output Capture แทน

## 10. Callout System

| Callout | สีพื้น | Icon Role |
| --- | --- | --- |
| Tip | ฟ้าอ่อน | หลอดไฟ |
| Warning | แดงอ่อน | เตือน |
| Note | ม่วงอ่อน | หมุด |
| Workshop | ส้มอ่อน | เครื่องมือ |
| Checklist | เขียวอ่อน | Checkbox |
| Prompt | ม่วงเข้ม ตัวอักษรขาว | AI/Copy |
| Case Study | เทาอ่อน | แฟ้มงาน |

## 11. Quote

ทุกบทมี Opening Quote, Mid Quote และ Closing Quote อย่างน้อยรวม 2 จุด ใช้พื้น Navy ตัวอักษรขาวและตรวจแหล่งที่มา หากไม่มีแหล่งที่มาระบุ “แนวคิดสำคัญ”

## 12. Typography

- Heading: Navy, Bold, Soft Shadow เฉพาะหน้า Hero
- Subheading: สีประจำ Part
- Body: Charcoal Gray
- Caption: Medium Gray
- Quote: White on Navy
- Code: Monospace ที่รองรับอักขระจริง
- ห้ามใช้ Shadow กับ Body Text

## 13. Icon System

ใช้ Material Symbols Rounded เพียงชุดเดียวในฉบับพิมพ์ เว้นแต่โลโก้ผลิตภัณฑ์ที่ได้รับอนุญาต ไอคอนทุกตัวมี Asset ID และ Source/Rights Record

## 14. Bullet System

ต้นฉบับใช้ Semantic Markdown แล้ว Mapping เป็น ●, ◆, ✓, □, ★ และ ➜ ในขั้นจัดหน้า ส่วน Tip, Warning, Target, Workshop และ Note ใช้ไอคอนเวกเตอร์จากชุดเดียว ไม่ใช้ Emoji หลายสไตล์ปะปน

## 15. Table

หัวตาราง Navy ตัวอักษรขาว แถวสลับสีขาว/Tint เส้นบาง มี Caption และเลขตาราง ไอคอนใช้เฉพาะเมื่อช่วยสแกนข้อมูล

## 16. Header and Footer

- หน้าคู่ Header: ชื่อหนังสือ
- หน้าคี่ Header: ชื่อบท
- Footer: เลขหน้า รหัสบท Version, Website และ QR เมื่อมี URL ยืนยันแล้ว

## 17. Page Number

เลขหน้ามีกรอบ เส้นตกแต่ง สีประจำ Part และ Chapter Icon วางขอบนอกของหน้าคู่/หน้าคี่

## 18. White Space

ทุกหน้ามี White Space 10–15% ห้ามลดตัวอักษรหรือช่องไฟเพื่อยัดเนื้อหา

## 19. Chapter Summary Page

ท้ายบทมี Summary, Checklist, Mind Map, Key Takeaways, Next Chapter และ QR Download Placeholder

## 20. Image Prompt Metadata

ทุกภาพมี Prompt, Asset Type, Intended Page, Aspect Ratio, Style, Composition, Lighting, Color Palette, Negative Prompt, Tool/Model, Date, Alt Text, Caption และ Rights Status

## 21. Page Composition Target

ค่าเป้าหมายโดยรวมต่อบทหรือ Spread:

- Text 50%
- Image 30%
- Infographic 10%
- Diagram 10%

ตัวเลขนี้เป็น Editorial Balance ไม่ใช่การบังคับทุกหน้าให้มีสัดส่วนเท่ากัน

## 22. Layout Specification

ทุกบทมี Layout Specification ระบุ Page Type, Page Objective, Text Block, Visual Asset, Callout, Caption, Cross-reference, Menu State และ Page-break Rule ของแต่ละหน้า

## 23. Editable Source Requirement

- Diagram/Infographic เก็บไฟล์ต้นฉบับ SVG, Mermaid, AI หรือรูปแบบแก้ไขได้
- ภาพ Raster ใช้ 300 PPI ที่ขนาดจริง
- ภาษาไทยเป็น Live Text ไม่ฝังในภาพเมื่อเป็นข้อความสาระ
- Artwork จัดหน้าในระบบที่ส่งต่อ InDesign หรือโปรแกรมมืออาชีพได้

## 24. Final Gate

- [ ] ทุกหน้ามี Ribbon และ Visual Anchor
- [ ] ไม่มีหน้าข้อความล้วนเกิน 1 หน้าติดต่อกัน
- [ ] ทุกบทมี Infographic อย่างน้อย 3 ชิ้น
- [ ] Diagram Suite ครบและแก้ไขได้
- [ ] ทุก STEP มี Screenshot/Output Evidence
- [ ] Layout Specification และ Image Prompt ครบ
- [ ] คนไทยและบริบทไทยผ่าน Authenticity/Rights Review
- [ ] CMYK, 300 PPI, Font Embed, Bleed และ Preflight ผ่าน
