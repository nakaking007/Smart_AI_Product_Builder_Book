# Series Art Direction

เอกสารนี้ใช้ร่วมกับ `BOOK_PREMIUM_DECORATION_STANDARD.md`

## ภาพรวม

งานศิลป์เป็น Editorial Design 4 สีแบบ Modern Educational Technology ใช้กริดเดียวกันทั้ง 6 เล่ม องค์ประกอบต้องช่วยการอ่าน ไม่ใช่ตกแต่งเพื่อเติมหน้า

## Commercial Computer Book Standard

Complete Edition ต้องมีคุณภาพเทียบเท่าหนังสือคอมพิวเตอร์ 4 สีที่วางจำหน่ายในร้านหนังสือชั้นนำของไทย โดยใช้เป็นเกณฑ์ด้านความชัดเจน ความสวยงาม และความพร้อมขายเท่านั้น ห้ามคัดลอกปก กริด ไอคอน หรืออัตลักษณ์ของสำนักพิมพ์อื่นโดยตรง

- รูปเล่มแนะนำ: B5 เพื่อรองรับ Screenshot, Code และตารางโดยไม่บีบตัวอักษร
- ระบบสีฉบับพิมพ์: CMYK 4 สี พร้อม ICC Profile ตามโรงพิมพ์
- ภาพ Raster: 300 PPI ที่ขนาดวางจริง
- Diagram/Icon/Logo: Vector เมื่อทำได้
- Screenshot: คมชัด ตัดส่วนเกิน มีหมายเลข Callout และ Caption
- ทุก 2 หน้ามี Visual Anchor อย่างน้อย 1 จุด
- Chapter Opener, Workshop, Prompt, Code, Tip, Warning และ Checklist ใช้ Component Style คงที่
- พิสูจน์สีด้วย Digital/Contract Proof ก่อนพิมพ์จริง

งานออกแบบต้องดูเป็นหนังสือเชิงพาณิชย์ ไม่ใช่รายงาน Word และไม่ใช้สีหรือกราฟิกมากจนรบกวนการเรียน

## Typography

- ภาษาไทย: Sarabun สำหรับ Body และ Heading ที่อ่านง่าย
- Heading 1: Navy Blue, Bold, Gold Rule
- Heading 2: Royal Blue, Semibold
- Body: Charcoal Gray
- Code: ฟอนต์ Monospace ที่รองรับอักขระที่ใช้จริง
- Quote: สีขาวบน Navy Blue หรือ Navy Blue บนพื้น White

## Component Colors

| Component | Color |
| --- | --- |
| Prompt Box | Lavender / Blue Tint |
| Workshop Box | Warm Gold / Orange Tint |
| Checklist Box | Light Green |
| Warning Box | Light Red |
| Case Study Box | Light Gray |
| Tip Box | Light Blue |

## Series Consistency Check

- ตำแหน่งโลโก้ ชื่อชุด เลขเล่ม ผู้เขียน และ Edition ตรงกันทุกปก
- Icon Stroke, Corner Radius, Shadow และ Caption Style ใช้ Token ชุดเดียว
- แต่ละเล่มมี Accent ต่างกันได้ แต่ Navy/Gold เป็นแกนร่วม
- ภาพทุกชิ้นมี Asset ID, Alt Text, Caption, Source/Rights และ Print Spec
- ไม่มี Emoji ปะปนในฉบับพิมพ์เมื่อมีไอคอนเวกเตอร์แทนได้
- PDF ฉบับโรงพิมพ์ผ่าน Font Embed, Image Resolution, Overprint, Transparency และ Bleed Preflight
