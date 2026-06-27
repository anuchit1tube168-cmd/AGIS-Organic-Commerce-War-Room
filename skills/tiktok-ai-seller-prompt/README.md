# TikTok AI Seller Prompt Skill

สกิลนี้ใช้สำหรับเปลี่ยนลิงก์ TikTok / Reels / Shorts / ข้อความตัวอย่าง ให้กลายเป็นระบบผลิตคอนเทนต์ขายของแบบทำซ้ำได้ ไม่ใช่แค่สรุปคลิป แต่ถอดเป็นสูตร Prompt + Script + SOP + Checklist + Agent Workflow

## ใช้เมื่อไหร่

- ต้องการถอดสูตรจากคลิปไวรัล
- ต้องการทำคอนเทนต์ขายของแบบ Organic
- ต้องการทำ TikTok Shop / Shopee Affiliate / Facebook Reels / YouTube Shorts
- ต้องการแตกไอเดียคลิป 30–100 คลิปต่อสินค้า
- ต้องการให้ AI ช่วยคิด Hook, Script, Caption, CTA และ Hashtag
- ต้องการทำงานเป็น Content War Room แบบมี Agent หลายบทบาท

## โครงสร้างไฟล์

```text
skills/tiktok-ai-seller-prompt/
├── SKILL.md
├── README.md
├── prompt-library.md
├── sop-content-war-room.md
├── agent-workflow.md
├── guardrails.md
├── templates/
│   ├── product-brief-template.md
│   ├── content-calendar-template.csv
│   └── daily-production-board.md
└── examples/
    └── sample-output.md
```

## วิธีใช้แบบเร็ว

1. ใส่ข้อมูลสินค้า 1 ตัวลงใน `templates/product-brief-template.md`
2. ใช้ Prompt จาก `prompt-library.md`
3. วางผลลัพธ์ลง `templates/daily-production-board.md`
4. ตรวจความเสี่ยงด้วย `guardrails.md`
5. วางแผนลงคลิปด้วย `templates/content-calendar-template.csv`

## คำสั่งใช้งานสั้น

```text
ใช้สกิล tiktok-ai-seller-prompt ถอดสูตรจากคลิปนี้ แล้วทำ Prompt + Script + Calendar ให้พร้อมใช้งาน
```

```text
ใช้สกิลนี้กับสินค้า [ชื่อสินค้า] แตกไอเดีย 30 คลิป พร้อม Hook, Script, Caption, CTA
```

```text
ทำ Content War Room รายวันจากสินค้านี้ โดยใช้ Agent Workflow และส่งเป็นตารางผลิตคลิป
```

## Output ที่ควรได้

- สูตรคอนเทนต์จากต้นแบบ
- Prompt ใช้ซ้ำ
- Hook หลายเวอร์ชัน
- Script 15/30/60 วินาที
- Shot list สำหรับถ่ายคลิป
- Caption + CTA + Hashtag
- Checklist ก่อนโพสต์
- ตารางผลิตคอนเทนต์รายวัน

## หลักสำคัญ

ขายให้ดูมีประโยชน์ก่อน อย่าเปิดมาขายแข็งทันที คนดูไม่ได้แพ้สินค้า คนดูแพ้ความน่าเบื่อ

## Version

- Version: 1.0.1
- Owner: AGIS Organic Commerce War Room
- Updated: 2026-06-27
