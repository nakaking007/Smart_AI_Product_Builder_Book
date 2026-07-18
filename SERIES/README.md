# Smart AI Product Builder Series

พื้นที่วางแผน Smart AI Product Builder โดยปัจจุบันผลิต **Complete Edition เล่มหลักเพียงเล่มเดียว** ส่วนหนังสือเฉพาะทางเล่ม 2–6 เป็น Extended Series สำหรับพิจารณาภายหลัง

## สถานะหนังสือ

1. `01_BASIC` — Smart AI Product Builder Complete Edition — **กำลังผลิต**
2. `02_NOTEBOOKLM` — NotebookLM Builder — **พักไว้**
3. `03_CHROME_EXTENSION` — Chrome Extension Builder — **พักไว้**
4. `04_GOOGLE_APPS_SCRIPT` — Google Apps Script Builder — **พักไว้**
5. `05_CODEX_DEVELOPER` — Codex Developer — **พักไว้**
6. `06_AI_PRODUCT_BUSINESS` — AI Product Business — **พักไว้**

## หลักการรักษาเนื้อหา

- ไฟล์ `BOOK_SET_*` เดิมเป็น Source Archive ห้ามลบจนกว่าการย้ายเนื้อหาจะผ่าน Content Parity Check
- ทุกเนื้อหาที่นำมาใช้ใหม่ต้องบันทึก Source ID และ Target Chapter ใน `CONTENT_MIGRATION_MAP.md`
- การแยกบททำเพื่อให้อ่านง่ายและอัปเดตได้ ไม่ใช่เพื่อตัดเนื้อหา
- แต่ละเล่มมี Version, Errata, Fact-check Date และ Release Checklist ของตนเอง
- รูปแบบจัดพิมพ์ใช้ `BOOK_PREMIUM_DECORATION_STANDARD.md` เป็นมาตรฐานกลาง

## ผลส่งมอบปัจจุบัน

ผลส่งมอบ Canonical ปัจจุบันคือ PDF Complete Edition จำนวน 1 ไฟล์ ไม่แยก PDF รายบท

| สถานะ | ชื่อไฟล์ PDF |
| --- | --- |
| กำลังผลิต | `Smart_AI_Product_Builder_Complete_Edition_v1.0.pdf` |
| อนาคต | PDF เล่ม 2–6 จะกำหนดเมื่อมีคำสั่งเริ่มผลิต |

Markdown, DOCX และไฟล์ภาพเป็น Production Source สำหรับแก้ไข ไม่ใช่ไฟล์อ่านแยกบทที่ส่งให้ลูกค้า

## โครงสร้างมาตรฐานต่อเล่ม

```text
XX_BOOK_NAME/
├── README.md
├── SUMMARY.md
├── BOOK_METADATA.yaml
├── chapters/
├── assets/
│   ├── images/
│   ├── icons/
│   ├── diagrams/
│   └── qr/
├── prompts/
├── workshops/
├── projects/
├── references/
├── layout/
└── output/
    ├── docx/
    ├── pdf/
    └── epub/
```

## สถานะ

Complete Edition ได้รับการยืนยันเป็น Canonical Version เมื่อ 19 กรกฎาคม 2569 และหยุดการผลิต Extended Series ไว้จนกว่าจะมีคำสั่งใหม่
