# Smart AI Product Builder Series

ชุดหนังสือภาคปฏิบัติ 6 เล่มสำหรับการเรียน การอบรม และการสร้าง AI Product โดยใช้มาตรฐานงานศิลป์ ระบบเลข และแม่แบบจัดพิมพ์ร่วมกันทั้งชุด

## หนังสือในชุด

1. `01_BASIC` — Smart AI Product Builder BASIC
2. `02_NOTEBOOKLM` — NotebookLM Builder
3. `03_CHROME_EXTENSION` — Chrome Extension Builder
4. `04_GOOGLE_APPS_SCRIPT` — Google Apps Script Builder
5. `05_CODEX_DEVELOPER` — Codex Developer
6. `06_AI_PRODUCT_BUSINESS` — AI Product Business

## หลักการรักษาเนื้อหา

- ไฟล์ `BOOK_SET_*` เดิมเป็น Source Archive ห้ามลบจนกว่าการย้ายเนื้อหาจะผ่าน Content Parity Check
- ทุกเนื้อหาที่นำมาใช้ใหม่ต้องบันทึก Source ID และ Target Chapter ใน `CONTENT_MIGRATION_MAP.md`
- การแยกบททำเพื่อให้อ่านง่ายและอัปเดตได้ ไม่ใช่เพื่อตัดเนื้อหา
- แต่ละเล่มมี Version, Errata, Fact-check Date และ Release Checklist ของตนเอง
- รูปแบบจัดพิมพ์ใช้ `BOOK_PREMIUM_DECORATION_STANDARD.md` เป็นมาตรฐานกลาง

## ผลส่งมอบฉบับจำหน่าย

หนังสือแต่ละเล่มรวมเป็น PDF เพียง 1 ไฟล์ ไม่แยก PDF รายบท รวมทั้งชุดจึงมี PDF หลัก 6 ไฟล์

| เล่ม | ชื่อไฟล์ PDF หลัก |
| --- | --- |
| 1 | `Smart_AI_Product_Builder_BASIC_v1.0.pdf` |
| 2 | `NotebookLM_Builder_v1.0.pdf` |
| 3 | `Chrome_Extension_Builder_v1.0.pdf` |
| 4 | `Google_Apps_Script_Builder_v1.0.pdf` |
| 5 | `Codex_Developer_v1.0.pdf` |
| 6 | `AI_Product_Business_v1.0.pdf` |

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

เริ่มสร้างสถาปัตยกรรม Series เมื่อ 18 กรกฎาคม 2569 โดยเล่ม 1 เป็นลำดับผลิตแรก
