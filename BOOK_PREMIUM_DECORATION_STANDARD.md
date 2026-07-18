# Premium Book Decoration Standard

## หลักการ

ต้นฉบับใช้ Semantic Markdown เพื่อรองรับ GitHub, Pandoc, DOCX, PDF และ EPUB ส่วนรูปแบบพรีเมียม เช่น ไอคอน Bullet, Header, Footer และเส้นคั่น ให้แม่แบบจัดหน้าควบคุมอย่างสม่ำเสมอ ไม่พิมพ์สัญลักษณ์ตกแต่งแทนโครงสร้าง Markdown จน Accessibility เสีย

## Icon System

ใช้ Line Icon หรือ Flat Icon ชุดเดียว เส้นหนาสม่ำเสมอ และใช้ Deep Blue, Emerald Green, Gold Accent

| รหัส | ชื่อไฟล์มาตรฐาน | การใช้งาน |
| --- | --- | --- |
| ICON-CHAPTER-01 | `icon_chapter_01.svg` | เปิดบท |
| ICON-TOOL-01 | `icon_tool_01.svg` | เครื่องมือ |
| ICON-TIP-01 | `icon_tip_01.svg` | เทคนิค |
| ICON-WARNING-01 | `icon_warning_01.svg` | ข้อควรระวัง |
| ICON-WORKSHOP-01 | `icon_workshop_01.svg` | Workshop |
| ICON-PROMPT-01 | `icon_prompt_01.svg` | Prompt Box |
| ICON-CHECKLIST-01 | `icon_checklist_01.svg` | Checklist |
| ICON-CASE-01 | `icon_case_study_01.svg` | Case Study |
| ICON-CODE-01 | `icon_code_01.svg` | Code |
| ICON-QR-01 | `icon_qr_01.svg` | QR Code |
| ICON-QUOTE-01 | `icon_quote_01.svg` | Quote Box |

ทุกไอคอนต้องมี SVG ต้นฉบับ PNG 300 DPI สำรอง ชื่อไฟล์ รหัส Alt Text และหลักฐานสิทธิ์ใช้งาน

## Bullet System

ใน Markdown ใช้ `-` สำหรับรายการและเยื้องระดับตามโครงสร้าง แม่แบบจัดหน้าจะแสดงผลดังนี้

- ระดับ 1: ●
  - ระดับ 2: ◆
    - ระดับ 3: –
- Checklist: `[ ]` แสดง □ และ `[x]` แสดง ✓
- Callout: ★ ประเด็นสำคัญ, ➜ ขั้นตอนถัดไป, ⚠ ข้อควรระวัง, 💡 เทคนิค

ห้ามผสม Emoji หลายสไตล์ในเนื้อหา ให้ใช้ไอคอนเวกเตอร์ของระบบในฉบับพิมพ์

## Numbering System

- บทและหัวข้อฉบับพิมพ์: บทที่ ๑, ๑.๑, ๑.๑.๑
- ขั้นตอนในบทปฏิบัติ: STEP 1, STEP 2, STEP 3
- ภาพ: ภาพที่ ๑.๑
- ตาราง: ตารางที่ ๑.๑
- แผนภาพ: แผนภาพที่ ๑.๑
- Prompt: Prompt ๑.๑
- Workshop: Workshop ๑.๑
- Code: Code ๑.๑
- Checklist: Checklist ๑.๑

เลขอ้างอิงสร้างจาก Metadata ตอน Build เพื่อลดเลขข้ามและ Cross-reference ผิด ต้นฉบับใช้รหัสคงที่ เช่น `[SCREENSHOT-04-03]` แล้วแปลงเป็น Caption ในขั้นจัดหน้า

## Page Number, Header และ Footer

- ส่วนต้นใช้เลขโรมันตัวเล็ก i, ii, iii
- เนื้อหาหลักเริ่มนับใหม่ที่บทแรก
- หน้าคู่: เลขหน้ามุมล่างซ้าย และ Header ชื่อหนังสือ
- หน้าคี่: เลขหน้ามุมล่างขวา และ Header ชื่อบท
- Footer มีเส้นบาง ชื่อหลักสูตร และรหัสบท
- เว้นระยะจาก Trim และไม่วางใน Bleed/Safe Area
- หน้าเปิดบทสามารถตัด Header แต่ยังรักษาการนับหน้า

## Divider System

| ระดับ | รูปแบบ | สี |
| --- | --- | --- |
| Chapter Divider | เส้นคู่หรือ Icon Divider | Deep Blue + Gold |
| Section Divider | Thin Line | Deep Blue |
| Callout Divider | เส้นสั้นกับไอคอน | Emerald/Gold |
| Appendix Divider | Decorative Line แบบเรียบ | Gray + Blue |

ใช้ Divider เมื่อเปลี่ยนระดับเนื้อหาจริง ไม่ใช้ทุกย่อหน้าหรือใช้เพื่อเติมพื้นที่

## Quality Gate

- ไอคอนทุกตัวมาจากชุดเดียวและมีรหัส
- Bullet ยังเป็นโครงสร้างรายการที่ Screen Reader อ่านได้
- เลขภาพ ตาราง Prompt และ Workshop ไม่ข้าม
- Header/Footer ถูกด้านเมื่อพิมพ์สองหน้า
- ภาพ 300 DPI และสีตามโปรไฟล์โรงพิมพ์
- ไม่มี Placeholder ที่ขาดชื่อ จุดประสงค์ สิ่งที่ต้องปรากฏ หรือ Caption

## Chapter Opening Page

ทุกบทต้องเริ่มด้วยหน้าเปิดบทเต็มหน้าและมี Page Break ก่อนเนื้อหาหลัก โดยประกอบด้วยเลขบทขนาดใหญ่ ชื่อบท คำโปรย Hero Image ไอคอนประจำบท Opening Quote สีประจำบท เส้นตกแต่ง พื้นหลังไล่เฉดอย่างสุภาพ และพื้นที่สำหรับเลขหน้า

- ชื่อบทใช้ Navy Blue ตัวหนา มีเงาอ่อน และมีเส้น Gold Accent หรือ Royal Blue คั่น
- Hero Image ต้องมีรหัสไฟล์ Caption Alt Text อัตราส่วน และคำอธิบาย Artwork
- หน้าเปิดบทไม่วาง Header แต่ยังนับเลขหน้า และสงวนพื้นที่เลขหน้าตามระบบหน้าคู่–หน้าคี่
- Gradient ต้องมี Contrast เพียงพอและไม่รบกวนการอ่าน

## Section Title Design

| ประเภท | รูปแบบมาตรฐาน |
| --- | --- |
| หัวข้อหลัก | Navy Blue ตัวหนา มีเลขหัวข้อและแถบสีหรือเส้นใต้ |
| หัวข้อย่อย | Royal Blue มีไอคอนเล็กและระยะห่างก่อน–หลังชัดเจน |
| Workshop | พื้น Gold Tint มีกรอบและ `ICON-WORKSHOP-01` |
| Prompt | พื้น Purple/Blue Tint กรอบมุมมน `ICON-PROMPT-01` และ Copy Placeholder |
| Warning | พื้น Red Tint และ `ICON-WARNING-01` |

ต้นฉบับ Markdown ใช้ Heading ตามลำดับจริง ห้ามใช้ข้อความตัวหนาแทน Heading การใส่สี กรอบ และไอคอนเป็นหน้าที่ของแม่แบบจัดหน้า

## Callout Box System

| ชนิด | สีพื้น | ไอคอน | จุดประสงค์ |
| --- | --- | --- | --- |
| TIP BOX | ฟ้าอ่อน | `ICON-TIP-01` | เทคนิคที่นำไปใช้ได้ทันที |
| WARNING BOX | แดงอ่อน | `ICON-WARNING-01` | ความเสี่ยงและข้อควรระวัง |
| PROMPT BOX | ม่วงอ่อน | `ICON-PROMPT-01` | Prompt พร้อมปุ่ม Copy Placeholder |
| WORKSHOP BOX | ทองอ่อน | `ICON-WORKSHOP-01` | กิจกรรมลงมือทำและเกณฑ์ส่งงาน |
| CHECKLIST BOX | เขียวอ่อน | `ICON-CHECKLIST-01` | รายการตรวจด้วย Checkbox |
| CASE STUDY BOX | เทาอ่อน | `ICON-CASE-01` | กรณีศึกษาและบทเรียน |
| QUOTE BOX | Navy Blue | `ICON-QUOTE-01` | ข้อความสีขาว เครื่องหมายคำพูดใหญ่ และเงาอ่อน |

Callout ทุกกล่องต้องมีชื่อ ประโยชน์ต่อผู้อ่าน และเนื้อหาจริง ห้ามใช้กล่องเพื่อเติมพื้นที่

## Quote Design

ทุกบทต้องมี Quote อย่างน้อย 2 จุด และควรใช้ครบ 3 บทบาทเมื่อเนื้อหาเอื้ออำนวย

1. Opening Quote: ขนาดใหญ่ สีน้ำเงินหรือสีขาวบนพื้นเข้ม ระบุชื่อผู้กล่าว หรือ “แนวคิดสำคัญ”
2. Mid-Chapter Quote: ใช้แบ่งช่วงเนื้อหา มีเส้นตกแต่งซ้าย–ขวาและตัวอักษรหนา
3. Closing Quote: สรุปแนวคิดท้ายบท วางกึ่งกลางและมี White Space รอบข้อความ

คำกล่าวที่ระบุชื่อบุคคลต้องตรวจสอบแหล่งอ้างอิง หากตรวจสอบไม่ได้ให้ใช้คำว่า “แนวคิดสำคัญ” และห้ามสร้างคำอ้างอิงปลอม

## Table Design

- ทุกตารางมี Caption และเลขตารางตามบท
- Header ใช้ Navy Blue และตัวอักษรสีขาว
- แถวข้อมูลสลับ Light Blue กับ White เส้นตารางบาง
- ใช้มุมมนเมื่อระบบส่งออกรองรับ
- หลีกเลี่ยงตารางกว้างเกิน Trim Size; หากข้อมูลมากให้แยกตารางหรือเปลี่ยนเป็นแนวตั้ง
- Header ต้องทำซ้ำเมื่อข้ามหน้า และห้ามปล่อยแถวหัวตารางค้างท้ายหน้า

## Page Composition

เป้าหมายสัดส่วนต่อหน้าจัดพิมพ์โดยประมาณคือ ข้อความ 55–65% ภาพหรือกราฟิก 25–35% และ White Space 10–15%

- ห้ามมีหน้าที่เต็มด้วยข้อความต่อเนื่องเกิน 2 หน้า
- วาง Visual Anchor อย่างน้อย 1 จุดในทุกหน้า
- หลีกเลี่ยง Orphan, Widow, หัวข้อค้างท้ายหน้า และภาพแยกจาก Caption
- หน้าปฏิบัติการต้องจัด STEP ภาพ และคำอธิบายให้อยู่ใกล้กัน
- หากองค์ประกอบแน่นเกินไป ให้เพิ่มหน้า ไม่ย่ออักษรจนอ่านยาก

### แถบเมนูประจำหน้า

- ทุกหน้ามี Section Tab หรือ Menu Band แบบ 4 สี ยกเว้นหน้าว่างตามหลักการพิมพ์และหน้าที่โรงพิมพ์กำหนด
- หน้าคู่แสดงแถบที่ขอบซ้าย หน้าคี่แสดงที่ขอบขวา
- แถบระบุภาค บท รหัสบท และสีประจำภาค
- สีตัวอักษรหัวข้อสลับตาม Design Token ของภาค ไม่สลับแบบสุ่ม
- Menu Band ต้องไม่รุก Safe Area และไม่ชน Header, Footer หรือ Thumb Index
- Ribbon ใช้สีประจำ PART 1–8 ตาม `BOOK_ART_DIRECTION_STANDARD_v1.0.md` และ Highlight Part ปัจจุบัน

### กฎภาพประกอบรายหน้า

- ทุกหน้าต้องมีภาพ Screenshot, Illustration, Diagram, Infographic, Table, Annotated Code หรือ Callout เชิงข้อมูลอย่างน้อย 1 จุด
- Diagram และ Infographic ต้องช่วยให้เข้าใจ ไม่ใช้เป็นลายตกแต่ง
- ห้ามใช้ภาพซ้ำเพื่อให้ผ่านจำนวน
- ห้ามขยายภาพความละเอียดต่ำหรือสร้าง Caption ที่ไม่สัมพันธ์กับภาพ
- หากเนื้อหาไม่เหมาะกับภาพใหญ่ ให้ใช้ไอคอนนำทาง ตารางย่อ หรือ Callout ที่มีข้อมูลจริง
- ภาพประกอบบุคคลใช้คนไทยในบริบทจริงของการศึกษา ราชการ ธุรกิจ และเทคโนโลยีอย่างเหมาะสม ไม่ใช้ภาพเหมารวมหรือเครื่องหมายองค์กรโดยไม่มีสิทธิ์

## Luxury Visual Style

ภาพรวมต้องเป็น Premium, Modern, Professional, Four-color Editorial Design สำหรับ Educational Technology

| บทบาทสี | สีแนะนำ |
| --- | --- |
| Primary | Navy Blue |
| Secondary | Royal Blue |
| Body/Contrast | Black |
| Accent | Gold |
| Neutral | Light Gray และ White |

หลีกเลี่ยงสีฉูดฉาดหลายสี ไอคอนคนละสไตล์ เงาหนัก Gradient ที่ลดความชัด และเอฟเฟกต์ที่ดูราคาถูก

### มาตรฐานหนังสือคอมพิวเตอร์ 4 สีเชิงพาณิชย์

- ใช้ B5 เป็น Working Trim Size จนกว่าโรงพิมพ์ยืนยันขนาดสุดท้าย
- ใช้ CMYK 4 สีและ ICC Profile ตามสเปกโรงพิมพ์
- ภาพ 300 PPI ที่ขนาดใช้งานจริง; ห้ามขยายภาพความละเอียดต่ำแล้วอ้างว่าเป็น 300 PPI
- Screenshot ต้องอ่านเมนูได้ มี Callout Number และไม่บิดสัดส่วน
- Code Block ต้องอ่านได้ ไม่ตัดบรรทัดสำคัญ และมีคำอธิบายก่อน/หลัง
- ใช้ Paper White และ Ink Coverage ให้เหมาะกับกระดาษจริง
- ตรวจ Soft Proof และ Printed Proof ก่อนอนุมัติพิมพ์จำนวนมาก
- ใช้หนังสือคอมพิวเตอร์ในร้านค้าปลีกเป็น Quality Benchmark แต่ห้ามเลียนแบบ Trade Dress ของสำนักพิมพ์ใด

## Final Art Director Check

- [ ] มีหน้าเปิดบทเต็มหน้าและ Hero Image ที่อธิบายครบ
- [ ] มีไอคอนประจำบทจากชุดมาตรฐาน
- [ ] ระบบเลขหัวข้อ ภาพ ตาราง แผนภาพ Prompt Workshop Code และ Checklist ต่อเนื่อง
- [ ] Header, Footer และเลขหน้าถูกด้าน
- [ ] มี Quote อย่างน้อย 2 จุดและตรวจที่มาแล้ว
- [ ] มี Callout Box ที่สัมพันธ์กับเนื้อหา
- [ ] มี Infographic และ Diagram พร้อม Caption/Alt Text
- [ ] มี Divider ตามระดับ ไม่ใช้ตกแต่งเกินจำเป็น
- [ ] White Space เพียงพอและไม่มีข้อความแน่นเกิน 2 หน้าต่อเนื่อง
- [ ] ทุกหน้ามี Visual Anchor และ Section Tab ตาม Page Type
- [ ] ใช้ Navy Blue, Royal Blue, Black, Gold, Light Gray และ White สม่ำเสมอ
- [ ] ภาพรวมเหมาะกับงานพิมพ์ 4 สี
- [ ] พร้อมนำเข้า Adobe InDesign, PageMaker, Photoshop หรือ Illustrator โดยไม่แก้โครงสร้างเนื้อหา
