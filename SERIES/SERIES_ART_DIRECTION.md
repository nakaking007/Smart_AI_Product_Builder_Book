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
- ทุกหน้ามี Visual Anchor อย่างน้อย 1 จุด โดยเลือกชนิดให้ตรงกับหน้าที่ของเนื้อหา
- Chapter Opener, Workshop, Prompt, Code, Tip, Warning และ Checklist ใช้ Component Style คงที่
- พิสูจน์สีด้วย Digital/Contract Proof ก่อนพิมพ์จริง

งานออกแบบต้องดูเป็นหนังสือเชิงพาณิชย์ ไม่ใช่รายงาน Word และไม่ใช้สีหรือกราฟิกมากจนรบกวนการเรียน

แนวทางหน้าในอนุมัติให้ยึด `SERIES/01_BASIC/INTERIOR_LAYOUT_REFERENCE.md` โดยสร้างใหม่เป็น Master Pages และ Editable Components ไม่วางภาพ Reference ทั้งภาพลงในฉบับพิมพ์

## Full-Color Page System

ทุกหน้าภายในใช้ระบบสี CMYK 4 สี รวมถึง Header, Footer, Section Tab, Caption, Callout และองค์ประกอบนำทาง ไม่จำเป็นต้องพิมพ์พื้นสีเต็มหน้า เพราะทำให้หมึกหนักและอ่านล้า แต่ทุกหน้าต้องมีสีที่ทำหน้าที่จริง

### Menu and Section Tab

- ด้านบนของทุกหน้ามี Ribbon Navigation แสดง PART 1–8 และ Tab เสริมสำหรับ Project, Workshop และ Appendix
- Part ปัจจุบันใช้สีเต็มและขนาดเด่นกว่า ส่วน Part อื่นใช้ Tint
- ขอบนอกยังใช้ Thumb Tab แสดงรหัสบทเพื่อค้นหน้าได้เร็ว
- หน้าเปิดบทใช้ Chapter Band ขนาดใหญ่ ส่วนหน้าปก ภาคผนวก และ Index ใช้รูปแบบเฉพาะที่ยังอยู่ในระบบเดียวกัน
- แถบเมนูต้องอยู่นอกพื้นที่เนื้อหา ไม่ทับข้อความ ภาพ หรือเลขหน้า

สี Ribbon และองค์ประกอบหลักให้ยึด [Book Art Direction & Editorial Design Standard v1.0](../BOOK_ART_DIRECTION_STANDARD_v1.0.md)

### Alternating Typography Color

- Heading 1 ใช้ Navy Blue เป็นหลัก และสลับ Royal Blue/Teal ตามสีประจำภาค
- Heading 2 ใช้สีรองของภาค ส่วน Heading 3 ใช้ Charcoal กับ Accent Rule
- คำสำคัญใช้ Gold Accent อย่างจำกัด ไม่ใช้ทองกับ Body Text ยาว
- สีสลับตาม Semantic Role และ Section Token ห้ามสลับแบบสุ่มรายย่อหน้า
- Body Text ใช้ Charcoal Gray เพื่อความสบายตาและต้องอ่านได้เมื่อพิมพ์ขาวดำ

## One Visual Anchor per Page

ทุกหน้าต้องมีองค์ประกอบภาพอย่างน้อยหนึ่งชนิดจากรายการต่อไปนี้

- Screenshot พร้อม Callout
- Illustration หรือ Hero Artwork
- Diagram หรือ Architecture
- Infographic หรือ Timeline
- Mind Map หรือ Workflow
- ตารางเปรียบเทียบที่ออกแบบเป็นภาพข้อมูล
- Annotated Code Panel
- Prompt, Tip, Warning, Workshop, Checklist หรือ Case Study Box ที่มีไอคอนและข้อมูลจริง

ไม่บังคับให้ใส่ทั้ง Infographic และ Diagram ในหน้าเดียวกัน เพราะทำให้ข้อมูลซ้ำและแน่นเกินไป Diagram ใช้อธิบายความสัมพันธ์หรือ Workflow ส่วน Infographic ใช้สรุปข้อมูลหลายจุดให้มองเห็นภาพรวม

## Visual Frequency

- ทุกหน้า: Visual Anchor อย่างน้อย 1 จุด
- ทุก Step: Screenshot/Mockup หรือผลลัพธ์ที่ตรวจได้
- ทุกหัวข้อแนวคิด: Diagram, Workflow หรือ Mind Map ตามความเหมาะสม
- ทุกบท: Infographic อย่างน้อย 3 ภาพ และ Diagram Suite ตามมาตรฐาน v1.0
- ทุก Workshop: Workflow + Worksheet/Checklist
- ทุกบทโค้ด: Annotated Code + Output Screenshot
- ทุกหน้าสรุปบท: Summary Infographic หรือ Learning Map

## Thai People Illustration Standard

ภาพประกอบที่มีบุคคลให้ใช้คนไทยและบริบทไทยอย่างเป็นธรรมชาติ เช่น ห้องเรียนไทย มหาวิทยาลัย สำนักงาน อปท. ธุรกิจ SME พื้นที่ทำงานร่วมกัน และครอบครัวที่ใช้เทคโนโลยี ภาพต้องร่วมสมัย ไม่ใช้สัญลักษณ์ไทยแบบเหมารวมเพื่อเติมฉาก

- แสดงความหลากหลายด้านวัย เพศ สีผิว ภูมิภาค อาชีพ และความสามารถทางร่างกายอย่างเหมาะสม
- เสื้อผ้า อุปกรณ์ และสถานที่ต้องตรงบริบทงาน ไม่ผสมเครื่องแบบหรือเครื่องหมายราชการผิดประเภท
- ห้ามใช้ตราราชการ โลโก้ หรือเครื่องหมายองค์กรในภาพสร้างใหม่โดยไม่มีสิทธิ์
- ห้ามสร้างภาพบุคคลจริงที่ระบุตัวได้โดยไม่ได้รับอนุญาต
- ภาพถ่ายต้องมี Model Release และ Property Release เมื่อจำเป็น
- ภาพสร้างด้วย AI ต้องบันทึก Prompt, Model/Tool, วันที่สร้าง, ผู้ตรวจ และสถานะสิทธิ์
- หลีกเลี่ยงการใช้วัด ตุ๊กตุ๊ก ชุดไทย หรือธงชาติเป็นสัญลักษณ์ประกอบทุกภาพ เว้นแต่เกี่ยวข้องกับเนื้อหาโดยตรง
- สีผิว ใบหน้า มือ นิ้ว ตัวอักษรไทย และอุปกรณ์ในภาพต้องผ่าน Visual QA ก่อนใช้

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
