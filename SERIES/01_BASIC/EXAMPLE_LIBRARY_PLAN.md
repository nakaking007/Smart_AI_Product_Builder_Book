# ภาคผนวก B — Ready-to-Use Example Library Plan

## เป้าหมาย

รวบรวมตัวอย่างจากทุกหัวข้อที่สอนให้ผู้เรียนเปิดศึกษา คัดลอก ทดลอง แก้ไข และต่อยอดได้จริง ตัวอย่างแต่ละชุดต้องเชื่อมกลับไปยังบทเรียน Prompt และ Workshop ที่เกี่ยวข้อง

## Definition of Ready-to-Use

ทุกตัวอย่างต้องมี

1. ปัญหาและกลุ่มผู้ใช้
2. โครงสร้างหรือ Architecture
3. ไฟล์/ข้อความต้นฉบับครบ
4. วิธีเปิดและใช้งานทีละขั้น
5. ตัวอย่าง Input และ Output
6. วิธีทดสอบและเกณฑ์ผ่าน
7. จุดที่ปรับแต่งได้
8. ข้อจำกัด ความปลอดภัย และข้อมูลส่วนบุคคล
9. แนวทางต่อยอดอย่างน้อย 3 แนวทาง
10. Version, Fact-check Date และ License/Source

## B01 — Gem Examples

| รหัส | ตัวอย่าง | ผลงาน |
| --- | --- | --- |
| GEM-EDU-01 | ผู้ช่วยครู | Instructions, Knowledge Plan, 10 Tests |
| GEM-STU-01 | ผู้ช่วยนักศึกษา | Study Workflow, Starter Library, Safety Rules |
| GEM-GOV-01 | ผู้ช่วยงานราชการ | Scope, Reference Rules, Draft Disclaimer |
| GEM-BIZ-01 | ผู้ช่วยธุรกิจ | Customer Workflow, Output Template, QA |

## B02 — Custom GPT Examples

| รหัส | ตัวอย่าง | ผลงาน |
| --- | --- | --- |
| GPT-WRI-01 | GPT สำหรับเขียนหนังสือ | Instructions, Style Rules, Chapter QA |
| GPT-CRS-01 | GPT สำหรับสร้างหลักสูตร | Outcome Map, Lesson Template, Rubric |
| GPT-MKT-01 | GPT สำหรับการตลาด | Persona Input, Content Workflow, Review Rules |

## B03 — NotebookLM Examples

| รหัส | ตัวอย่าง | ผลงาน |
| --- | --- | --- |
| NBL-MAN-01 | สร้างคู่มือ | Source Register, Questions, Manual Outline |
| NBL-RES-01 | สร้างงานวิจัย | Evidence Matrix, Citation Check, Gap List |
| NBL-POD-01 | สร้าง Podcast | Source Pack, Brief, Audio Review Checklist |

## B04 — Single Web App Examples

ทุกระบบต้องเป็นไฟล์ `index.html` ไฟล์เดียว เปิดใน Browser ได้โดยไม่ต้องติดตั้ง Server เว้นแต่ฟีเจอร์นั้นต้องใช้บริการภายนอกซึ่งต้องระบุชัดเจน

| รหัส | ระบบ | ฟังก์ชันขั้นต่ำ |
| --- | --- | --- |
| WEB-TODO-01 | To-Do | เพิ่ม แก้ สถานะ ลบ และ Local Storage |
| WEB-NOTE-01 | บันทึกโน้ต | ค้นหา Tag แก้ไข และ Export |
| WEB-REG-01 | ลงทะเบียน | Validate, Preview และ CSV Export |
| WEB-QUIZ-01 | แบบทดสอบ | คำถาม คะแนน เฉลย และ Reset |
| WEB-DASH-01 | Dashboard | KPI, Filter และ Chart จากข้อมูลตัวอย่าง |
| WEB-BUD-01 | คำนวณงบประมาณ | รายการ รายรับ/รายจ่าย ยอดรวม และ Export |
| WEB-PRJ-01 | ติดตามโครงการ | Milestone, Status, Progress และ Risk |

## B05 — Prompt Examples

- Prompt สำหรับ Gem อย่างน้อย 10 ชุด
- Prompt สำหรับ Custom GPT อย่างน้อย 10 ชุด
- Prompt สำหรับ NotebookLM อย่างน้อย 10 ชุด
- Prompt สำหรับ HTML อย่างน้อย 10 ชุด
- Prompt สำหรับ CSS อย่างน้อย 10 ชุด
- Prompt สำหรับ JavaScript อย่างน้อย 10 ชุด

ทุก Prompt ระบุวัตถุประสงค์ Input, Prompt ฉบับเต็ม, Expected Output, วิธีตรวจ และวิธีปรับแต่ง

## B06 — AI Product Examples

| รหัส | ตัวอย่าง | ขอบเขตในเล่ม BASIC |
| --- | --- | --- |
| PROD-HTML-01 | เว็บไซต์ไฟล์เดียว | Offline-first Single HTML |
| PROD-CHR-01 | Chrome Extension เบื้องต้น | ตัวอย่างศึกษาและเส้นทางต่อเล่ม 3 |
| PROD-GAS-01 | Google Apps Script เบื้องต้น | ตัวอย่างศึกษาและเส้นทางต่อเล่ม 4 |
| PROD-LAND-01 | Landing Page | Value Proposition, CTA และ Responsive |
| PROD-FORM-01 | แบบฟอร์มออนไลน์ | Validation, Consent และ Export |

ตัวอย่าง Chrome Extension และ Google Apps Script ในเล่ม BASIC เป็นบทนำที่ทำตามได้ แต่ไม่แทนเนื้อหาเชิงลึกในเล่มเฉพาะทาง

## Quality Gate

- [ ] ทุกหัวข้อการสอนมีตัวอย่างจริงอย่างน้อย 3 ตัวอย่าง
- [ ] ไฟล์ตัวอย่างเปิดได้และไม่มี Secret/API Key
- [ ] ตัวอย่าง Web App ผ่าน Browser Test ที่ระบุ
- [ ] Prompt ทุกชุดมีเกณฑ์ตรวจผล
- [ ] ตัวอย่างระบุข้อจำกัดและแนวทางต่อยอด
- [ ] ลิงก์จากบทเรียนมายัง Example ID ถูกต้อง
- [ ] License และ Source ชัดเจน
