# BOOK MASTER SPEC

## Smart AI Product Builder — Version 2.0

**ชื่อรอง:** คู่มือเรียนการใช้ AI ฉบับจับมือทำ
**ผู้เขียน:** ดร.เขมวันต์ บัวบาน

**ราคาปกติ:** ๕๐๐ บาท

**ราคาโปรโมชัน:** ๓๙๙ บาท โดยใช้ Badge แยกและต้องกำหนดเงื่อนไขก่อนจำหน่าย
**การใช้งาน:** หนังสือประกอบการอบรม 2 วัน

## Mission

สร้างหนังสือแบบ How To ที่ผู้อ่านเปิดแล้วทำตามได้จริง เนื้อหาใช้สัดส่วน How To ประมาณ 80% และทฤษฎีเท่าที่จำเป็นประมาณ 20% ทุกบทต้องมีผลงานที่ตรวจสอบได้

## โครงสร้างหลักสูตรแบบ Series

### Basic

เล่มหลัก `Smart AI Product Builder — Complete Edition` เป็นหลักสูตร 2 วัน ประกอบด้วย AI Foundation, Gem, Custom GPT, NotebookLM, Single Web App, Chrome Extension, Google Apps Script, Codex, AI Business, Workshop และ Capstone Project ตามสารบัญที่อนุมัติใน `SERIES/01_BASIC/SUMMARY.md`

### Advanced

1. การสร้าง Chrome Extension
2. การออกแบบและสร้าง Google Apps Script
3. การพัฒนา Chrome Extension ขั้นสูง
4. การใช้ Codex
5. การวิเคราะห์ตลาด การเผยแพร่ และตั้งราคา AI Product

ห้ามสลับ ตัด หรือเพิ่มหัวข้อหลักสูตรโดยไม่ได้รับคำสั่งจากผู้เขียน การตัดสินใจวันที่ 19 กรกฎาคม 2569 กำหนดให้ Complete Edition เป็น Canonical Version ส่วนหนังสือ 6 เล่มเป็นแผน Extended Series ในอนาคต

## องค์ประกอบห้ามตัดของ Complete Edition

- Single Web App Project
- Capstone Project
- Workshop และ Mini Project
- Prompt Library
- ภาคผนวก รวม Cheat Sheet, Templates, Checklists, FAQ, Glossary, References, Index และ Ready-to-Use Example Library

หากขาดรายการใดรายการหนึ่ง ให้ถือว่าต้นฉบับยังไม่ผ่าน Release Gate

## โครงสร้างไฟล์ฉบับจัดพิมพ์

Canonical Source อยู่ใน `SERIES/01_BASIC/` โดยคงชื่อไดเรกทอรีเดิมเพื่อไม่ทำลายลิงก์ ประกอบด้วย

1. `frontmatter/` — ปก ลิขสิทธิ์ คำนิยม คำนำ วิธีใช้ เส้นทางเรียน 2 วัน และสารบัญ
2. `chapters/` — บทที่ 1–32 ครอบคลุม Basic, Advanced, Single Web App, Workshop และ Capstone
3. `appendices/` — Prompt Library, Cheat Sheet, Templates, Checklists, FAQ, Glossary, References และ Index
4. `examples/` — Ready-to-Use Example Library
5. `assets/` — ภาพ ไอคอน Diagram QR และ Artwork
6. `output/` — QA Artifacts และ PDF ฉบับรวมหนึ่งไฟล์

ลำดับไฟล์ Canonical ให้ยึด `SERIES/01_BASIC/SUMMARY.md` ห้ามใช้โครงสร้าง BOOK_SET เดิมเป็นสารบัญฉบับจำหน่าย

## ส่วนประกอบบังคับของบทเรียน

- Hero Banner
- Pain Point
- เป้าหมายบทเรียน
- สิ่งที่ต้องเตรียม
- Menu Map พร้อมวันที่ตรวจสอบหน้าจอ
- Step by Step พร้อม Screenshot Placeholder ทุก Step
- Prompt พร้อมใช้และเกณฑ์ตรวจผล
- ตัวอย่างจริงหรือสถานการณ์จำลองที่ระบุชัดเจน
- Professional Tips
- Common Mistakes
- Case Study อย่างน้อย 1 เรื่อง
- Workshop ที่ลงมือทำจริง
- Mini Project ใช้เวลา 20–30 นาที
- Checklist
- FAQ
- Infographic Placeholder
- QR Code Placeholder
- สรุป แบบฝึกหัด และบทถัดไป

## มาตรฐานตัวอย่างใช้งานจริง

> ทุกหัวข้อที่สอน ต้องมีตัวอย่างใช้งานจริงอย่างน้อย 3 ตัวอย่าง และท้ายเล่มต้องมี Example Library รวมตัวอย่างครบทุกเรื่อง พร้อมอธิบายโครงสร้าง วิธีใช้งาน วิธีปรับแต่ง และแนวทางต่อยอด โดยตัวอย่างทั้งหมดสามารถนำไปใช้งานหรือพัฒนาต่อได้ทันที

ตัวอย่างจะถือว่า “พร้อมใช้” เมื่อมี Input หรือไฟล์ต้นฉบับ ขั้นตอนเปิดใช้งาน ผลลัพธ์ที่คาดหวัง วิธีตรวจสอบ วิธีปรับแต่ง ข้อจำกัด และแนวทางต่อยอดครบ ห้ามใช้ภาพจำลองหรือคำอธิบายแทนไฟล์ทำงานเมื่อหัวข้อนั้นต้องมีโค้ดหรือไฟล์ตัวอย่าง

## กฎการขยายเนื้อหา

หากบทใดสั้นหรือยังไม่เพียงพอสำหรับใช้ประกอบการอบรม ให้ขยายด้วยตัวอย่างจริง Workshop, Case Study, FAQ, Professional Tips, Common Mistakes, ภาพประกอบ และ Prompt เพิ่มเติม จนผู้อ่านทำตามและตรวจผลงานได้

**ห้ามเติมทฤษฎีเพื่อเพิ่มจำนวนหน้า** ทุกส่วนที่เพิ่มต้องช่วยให้ผู้อ่านลงมือทำ แก้ปัญหา หรือตรวจคุณภาพผลงานได้ดีขึ้น

## ภาพและ Prompt

- วาง Visual Anchor อย่างน้อย 1 จุดในทุกหน้าจัดพิมพ์ โดยเลือก Screenshot, Illustration, Diagram, Infographic, Workflow, Table, Annotated Code หรือ Callout เชิงข้อมูลให้เหมาะกับเนื้อหา
- ทุกภาพต้องมีหมายเลข คำบรรยาย อัตราส่วน และ Alt Text
- ทุก Prompt ต้องระบุชื่อ เครื่องมือ ระดับ วัตถุประสงค์ ผลลัพธ์ที่คาดหวัง วิธีตรวจ และข้อควรระวัง
- QR Code สร้างได้เมื่อมี URL ปลายทางที่ตรวจสอบแล้วเท่านั้น

## Quality Gate

บทจะถือว่าเสร็จเมื่อโครงสร้างครบ ทำตามได้จริง ไม่มีข้อมูลลับ แยกข้อมูลจริงกับสถานการณ์จำลอง มีวันที่ตรวจสอบ UI และพร้อมส่งออกเป็น PDF, DOCX และ EPUB โดยไม่ต้องเปลี่ยนโครงสร้างต้นฉบับ

การตกแต่งฉบับพิมพ์ให้ใช้ [Premium Book Decoration Standard](../BOOK_PREMIUM_DECORATION_STANDARD.md) โดยรักษา Semantic Markdown และใช้แม่แบบจัดหน้าควบคุมไอคอน Bullet, Numbering, Header, Footer และ Divider

มาตรฐานดังกล่าวเป็นข้อบังคับสำหรับทุกบท รวมถึงหน้าเปิดบทเต็มหน้า ระบบ Section Title และ Callout, Quote อย่างน้อย 2 จุด, Caption/เลขตาราง, สัดส่วน Page Composition, ชุดสี Navy–Royal Blue–Black–Gold และ Final Art Director Check ก่อนส่งออก

ฉบับพิมพ์ต้องเป็นหนังสือคอมพิวเตอร์ 4 สีระดับวางจำหน่ายในร้านหนังสือ ใช้ CMYK, ภาพ 300 PPI ที่ขนาดจริง, Vector Artwork, B5 Working Grid, Font Embedding, Bleed และ Print Preflight โดยไม่คัดลอกรูปแบบเฉพาะของสำนักพิมพ์อื่น

ทุกหน้าต้องใช้ระบบ Full-Color Page Furniture มีแถบเมนูประจำภาคที่ขอบนอก สีหัวข้อสลับตาม Design Token และ Visual Anchor อย่างน้อย 1 จุด ทั้งนี้ไม่บังคับให้มี Diagram และ Infographic พร้อมกันทุกหน้า เพราะต้องรักษาความชัดเจนและ White Space

Menu Band ใช้ระบบสลับเขียว–ส้มตามเลขบท: บทเลขคี่สีเขียว บทเลขคู่สีส้ม ตัวอักษรสีขาว ส่วนภาพประกอบที่มีบุคคลต้องสะท้อนคนไทยและบริบทไทยร่วมสมัยอย่างถูกต้อง หลากหลาย และมีสิทธิ์ใช้งาน

ข้อมูลเครื่องมือทุกบทต้องตรวจจาก Official Documentation พร้อมวันที่ตรวจสอบ ใช้ภาษาง่ายสำหรับผู้เริ่มต้น และจัดสัดส่วน HOW TO อย่างน้อย 80% ทุกขั้นมี Action, Screenshot/ภาพผลลัพธ์, Expected Result และวิธีแก้เมื่อไม่ผ่าน
