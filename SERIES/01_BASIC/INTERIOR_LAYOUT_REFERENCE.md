# Interior Layout Reference — Complete Edition

## Reference Asset

- **File:** `assets/images/layout_reference/SAPB_interior_layout_reference_v01.png`
- **Role:** Design reference for interior pages
- **Status:** Approved direction; must be rebuilt as editable layout, not placed as a single raster page
- **Dimensions:** 1024 × 1536 px at 96 DPI
- **SHA-256:** `F9A24D7D05E8B09379F056436620DB06D20C5C2EE3AF68FA2941548218BA72CB`

ไฟล์นี้ใช้เป็นภาพอ้างอิงเท่านั้น ความละเอียดไม่ใช่ไฟล์พิมพ์ และข้อความบางส่วนในภาพเป็น Mockup ต้องพิมพ์ใหม่ด้วย Live Text

## องค์ประกอบที่อนุมัติ

1. แถบเมนูด้านบนแสดง PART 1–8 ด้วยสีประจำ Part และ Highlight Part ปัจจุบัน
2. แถบไอคอนด้านข้างสำหรับสารบัญ ความรู้ เครื่องมือ Workshop, Project, Prompt, Checklist และอ้างอิง
3. หน้าเปิดบทสีเข้ม ใช้เลขบทใหญ่ ชื่อบท Hero Illustration คนไทย และ Quote
4. หน้ารองเปิดบทแสดงสารบัญย่อย สิ่งที่จะได้รับ และภาพผู้เรียนไทย
5. หน้าความรู้พื้นขาว ใช้หัวข้อเขียว กล่องสีอ่อน Diagram และ Tip Box
6. หน้า Step by Step ใช้ Screenshot แนวตั้งพร้อมเลขขั้นตอน
7. หน้า Prompt ใช้กล่องม่วง/ส้มและ Copy Marker
8. หน้า Workshop ใช้หัวแถบส้ม เป้าหมาย ภารกิจ ผลลัพธ์ และแถบ Metadata
9. เลขหน้าวางมุมล่างด้านนอกใน Tab สีประจำ Part
10. หน้าสรุปมี Workflow, Mind Map, Architecture และตัวอย่าง Page Layout

## สิ่งที่ต้องปรับจากภาพอ้างอิง

- เมนูบนต้องรองรับ 11 ภาคโดยไม่ทำให้ตัวอักษรเล็กเกินไป ใช้ชื่อย่อและ Thumb Index เมื่อจำเป็น
- เมนูซ้ายใช้เฉพาะหน้าที่ต้องนำทาง ห้ามเบียดพื้นที่อ่านในหน้าที่มี Code/Table กว้าง
- ภาพบุคคลต้องมีสิทธิ์หรือเป็นภาพสร้างใหม่ที่มี Asset Record
- ภาษาไทยทั้งหมดต้องเป็น Live Text ตรวจคำและฝังฟอนต์
- Screenshot ต้องมาจากหน้าจอจริงที่ตรวจวันที่แล้ว ไม่ใช้ UI สร้างจำลองแทนขั้นตอน
- Diagram ต้องสร้างเป็น Vector และแก้ไขได้
- Color Tokens ต้องใช้ค่า Green/Orange ที่อนุมัติและผ่าน CMYK Proof

## Layout Master Pages

| Master | ใช้กับ | องค์ประกอบหลัก |
| --- | --- | --- |
| M-COVER | ปกหน้า | Title, Subtitle, Hero, Scope, Author |
| M-HALF | หน้ารองปก | ชื่อหนังสือ Edition และผู้จัดทำ |
| M-FRONT | คำนำ/สารบัญ | Menu, Heading, Page Number, Light Visual |
| M-CHAPTER | หน้าเปิดบท | Full-page dark Hero, Large Chapter Number |
| M-CONCEPT | ทฤษฎีเท่าที่จำเป็น | Diagram/Infographic + Short Prose |
| M-STEP | How To | Step Number, Screenshot, Action, Result |
| M-PROMPT | Prompt | Prompt Box, Input, Output, QA |
| M-CODE | Code | Annotated Code + Output Screenshot |
| M-WORKSHOP | Workshop | Task, Deliverable, Time, Rubric |
| M-SUMMARY | สรุปบท | Learning Map, Checklist, Next Chapter |
| M-BACK | ปกหลัง | Value, Audience, Outcome, Author, ISBN/Barcode |

## Approval Gate

- [ ] สร้าง Master Page แยกครบตามตาราง
- [ ] Ribbon สีประจำ Part อ่านได้ในขนาดพิมพ์จริง
- [ ] คนไทยและบริบทไทยถูกต้อง
- [ ] ทุกหน้าเน้น HOW TO และมี Visual Anchor
- [ ] ภาษาไทยเป็น Live Text ไม่ฝังในภาพ
- [ ] Diagram/Infographic เป็น Vector หรือ 300 PPI
- [ ] ไม่มีข้อมูล UI ล้าสมัยหรือ Mockup ปะปนเป็นขั้นตอนจริง
