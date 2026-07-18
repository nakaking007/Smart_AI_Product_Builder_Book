# Curriculum Outcome Map — Smart AI Product Builder BASIC

## เป้าหมายหลัก

เมื่อจบหลักสูตร 2 วัน ผู้เรียนต้องสาธิต AI Product ชิ้นแรกของตนเองได้ พร้อมไฟล์ต้นฉบับ หลักฐานการทดสอบ เอกสารใช้งาน และแนวทางนำไปใช้จริง

## เส้นทางจากบทเรียนสู่ผลงาน

| ช่วง | บท | ผลงานสะสม | เกณฑ์ผ่าน |
| --- | ---: | --- | --- |
| AI Foundation | 1–3 | Problem Statement + Prompt Pack | ระบุผู้ใช้ ปัญหา Input/Output และตรวจคำตอบได้ |
| Gem Builder | 4–7 | Gem + Knowledge Plan + Test Report | ผ่าน Functional/Safety Tests ที่กำหนด |
| Custom GPT | 8–11 | Custom GPT + Release Checklist | ขอบเขตชัด Knowledge/Actions ปลอดภัย |
| NotebookLM | 12–13 | Source Register + Knowledge Artifact | Citation ตรวจย้อนกลับได้ |
| AI Business | 14 | Persona + Competitor Matrix + Price Card | ราคาอธิบายจากคุณค่าและต้นทุนได้ |
| Single Web App | 15–18 | `index.html` + Browser Test Report | เปิดใช้งาน ฟังก์ชันหลักผ่าน และไม่มี Secret |
| Capstone | 19–20 | AI Product Submission Pack | Demo ได้ README ครบ Rubric ผ่าน |

## Submission Pack ขั้นต่ำ

```text
capstone/
├── README.md
├── product_canvas.md
├── prompts/
├── knowledge/
├── webapp/
│   └── index.html
├── tests/
│   ├── functional_test.md
│   └── safety_test.md
├── market/
│   └── price_card.md
├── screenshots/
└── reflection.md
```

## Rubric ระดับเล่ม

| ด้าน | คะแนน | หลักฐาน |
| --- | ---: | --- |
| แก้ปัญหาผู้ใช้ | 20 | Problem Statement และ User Feedback |
| ทำงานได้จริง | 25 | Demo และ Functional Test |
| Prompt/Knowledge | 15 | Prompt Pack, Sources และ QA |
| UX และความชัดเจน | 15 | User Flow และ Usability Check |
| ความปลอดภัย | 10 | Data/Safety Checklist |
| ตลาดและราคา | 10 | Persona, Value และ Price Card |
| เอกสารส่งมอบ | 5 | README และไฟล์ครบ |
| **รวม** | **100** | ผ่านเมื่อได้อย่างน้อย 70 และไม่มี Critical Safety Failure |

## Critical Safety Failure

- ใส่ API Key, Password หรือข้อมูลส่วนบุคคลจริงไว้ในไฟล์ส่งงาน
- อ้างข้อมูล กฎหมาย หรือแหล่งอ้างอิงที่ตรวจสอบไม่ได้เป็นข้อเท็จจริง
- Web App ทำลายหรือส่งข้อมูลโดยไม่แจ้งผู้ใช้
- แชร์ Knowledge ที่ผู้เรียนไม่มีสิทธิ์ใช้

หากพบรายการใดรายการหนึ่ง ต้องแก้และทดสอบใหม่ก่อนถือว่าจบหลักสูตร แม้คะแนนรวมเกิน 70
