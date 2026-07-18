# Content Migration Map

ไฟล์นี้ใช้ป้องกันเนื้อหาหายระหว่างเปลี่ยนจาก BOOK_SET เป็น Series

| Source | เนื้อหาเดิม | Target | สถานะ |
| --- | --- | --- | --- |
| `BOOK_SET_01/00_ปก.md` | ปกหนังสือรวม | ปกเล่ม 1 และ Series Cover System | รอแยก |
| `BOOK_SET_01/01_คำนำ.md` | คำนำ | เล่ม 1 ส่วนหน้า: คำนำ | รอขยาย |
| `BOOK_SET_01/02_วิธีใช้หนังสือ.md` | วิธีใช้ | เล่ม 1 ส่วนหน้า: วิธีใช้หนังสือ | รอขยาย |
| `BOOK_SET_01/03_สารบัญ.md` | สารบัญเล่มรวม | สารบัญเล่ม 1 และแผนผัง Series | รอปรับ |
| `BOOK_SET_01/04_การสร้าง_Gem.md` | Gem แบบรวม | เล่ม 1 บท 4–7 | รอแยกและขยาย |
| `BOOK_SET_02/05_การสร้าง_Custom_GPT.md` | Custom GPT แบบรวม | เล่ม 1 บท 8–11 | รอแยกและขยาย |
| `BOOK_SET_02/06_การวิเคราะห์ตลาดและตั้งราคา.md` | ตลาดและราคา | เล่ม 1 บท 14 และเล่ม 6 | รอแยก |
| `BOOK_SET_02/07_การใช้_NotebookLM.md` | NotebookLM แบบรวม | เล่ม 1 บท 12–13 และเล่ม 2 บท 1–20 | รอแยกและขยาย |
| `BOOK_SET_02/08_Workshop_Basic.md` | Workshop Basic | เล่ม 1 บท 19 | รอปรับ |
| `BOOK_SET_02/09_Project_Basic.md` | Project Basic | เล่ม 1 บท 20 | รอปรับ |
| `chapters/01_AI_Foundation.md` | AI Foundation | เล่ม 1 บท 1–3 | รอคัดเลือกโดยไม่ทับการแก้ไขของผู้ใช้ |
| เนื้อหาใหม่ | Single Web App | เล่ม 1 บท 15–18 และ Example Library B04 | ต้องสร้างใหม่ |
| `chapters/09_Chrome_Extension.md` | Chrome Extension | Complete Edition บท 19–22 | รอคัดเลือกและตรวจเอกสารทางการ |
| `chapters/07_Google_Apps_Script.md` | Google Apps Script | Complete Edition บท 23–25 | รอคัดเลือกและตรวจเอกสารทางการ |
| `chapters/08_GAS_Project_Generator.md` | GAS Project Generator | Complete Edition Example Library | รอทดสอบก่อนย้าย |
| `chapters/10_Codex.md` | Codex | Complete Edition บท 26–28 | รอคัดเลือกและตรวจเอกสารทางการ |
| เนื้อหาตลาด/การเผยแพร่เดิม | AI Product Business ขั้นสูง | Complete Edition บท 29–30 | รอรวมและตัดซ้ำ |
| Workshop และโครงงานเดิม | Workshop/Capstone | Complete Edition บท 31–32 | รอรวม Rubric และ Test Evidence |

## กติกา Content Parity

- สถานะ “ย้ายแล้ว” ต้องมี Target File จริง
- ห้ามลบ Source จนกว่าจะเทียบหัวข้อ Prompt Workshop ภาพ และ References ครบ
- เนื้อหาซ้ำได้ระหว่างช่วงย้าย แต่ห้ามนับซ้ำในรายงานฉบับจำหน่าย
- เมื่อแก้ข้อเท็จจริงใน Target ให้บันทึกเหตุผลและวันที่ตรวจสอบ ไม่ย้อนแก้ Source Archive
- เนื้อหา Extended Series เล่ม 2–6 พักไว้ ไม่ย้ายหรือผลิตจนกว่าจะมีคำสั่งใหม่
