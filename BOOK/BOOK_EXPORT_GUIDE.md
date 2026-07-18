# Book Export Guide

## Source of Truth

ไฟล์ Markdown ใน chapters เป็นแหล่งข้อมูลหลัก ห้ามแก้เฉพาะ DOCX หรือ PDF แล้วปล่อยให้ Markdown ไม่ตรงกัน

## Output ที่ต้องการ

1. Markdown
2. DOCX
3. PDF
4. HTML
5. EPUB

## DOCX

- ใช้ Style จริงสำหรับ Heading, Body, List, Quote และ Code
- ใช้ A5, Mirror Margins, Gutter และ Section Break
- ใช้ Running Header สลับหน้าคี่–หน้าคู่
- อัปเดตสารบัญและเลขหน้าก่อนส่งออก

## PDF

- ตรวจขนาดหน้า A5
- ตรวจฟอนต์ รูป ตาราง และลิงก์
- ตรวจทุกหน้าจากภาพ Render
- Interior ที่ไม่มีภาพตกขอบไม่จำเป็นต้องมี Bleed
- ปกหรือหน้าตกขอบต้องใช้ Bleed และ Crop Mark ตามโรงพิมพ์
- ภาพ Raster ใช้ 300 PPI ที่ขนาดจริง

## HTML

- ใช้ Semantic Heading
- มี Alt Text
- Code เลื่อนแนวนอนหรือ Wrap ได้
- รองรับหน้าจอมือถือ
- CSS สำหรับพิมพ์ใช้ขนาด A5

## EPUB

- ใช้ EPUB แบบ Reflowable สำหรับเนื้อหา
- ไม่ใช้ Layout ตายตัวโดยไม่มีเหตุผล
- ตรวจสารบัญ การนำทาง Alt Text และฟอนต์

## Preflight

- ตรวจลิงก์ภายใน
- ตรวจ Missing Asset
- ตรวจ Heading Level
- ตรวจ Metadata
- ตรวจจำนวนหน้าและขนาดกระดาษ
- เปิดทดสอบอย่างน้อยสองโปรแกรมเมื่อเป็นไฟล์ส่งโรงพิมพ์

