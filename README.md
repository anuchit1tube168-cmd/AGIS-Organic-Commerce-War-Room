# AGIS Organic Commerce War Room

ระบบทดลองสำหรับทำ Organic Commerce ด้วย AI: คิดสินค้า → ทำคอนเทนต์ → โพสต์ → เก็บผล → หา Winner Product โดยเริ่มจากเครื่องมือที่ใช้งานได้จริงก่อน ไม่ต้องต่อ API หนักตั้งแต่วันแรก

---

## เปิดใช้งานเร็ว

### หน้าเว็บหลักของ repo

```text
https://anuchit1tube168-cmd.github.io/AGIS-Organic-Commerce-War-Room/
```

### Skills Hub

```text
https://anuchit1tube168-cmd.github.io/AGIS-Organic-Commerce-War-Room/skills/
```

### TikTok AI Seller Prompt Skill

```text
https://anuchit1tube168-cmd.github.io/AGIS-Organic-Commerce-War-Room/tiktok-ai-seller-prompt.html
```

หรือเปิดตรง:

```text
https://anuchit1tube168-cmd.github.io/AGIS-Organic-Commerce-War-Room/skills/tiktok-ai-seller-prompt/
```

---

## โมดูลที่มีตอนนี้

| Module | Path | สถานะ | ใช้ทำอะไร |
|---|---|---|---|
| Main War Room | `index.html` | ใช้งานได้ | กรอกสินค้า เจน Hook/Script/Caption เบื้องต้น |
| Skills Hub | `skills/index.html` | ใช้งานได้ | หน้าเลือกสกิลทั้งหมด |
| TikTok AI Seller Prompt | `skills/tiktok-ai-seller-prompt/` | ใช้งานได้ | ถอดสูตรคลิปและสร้างระบบ Prompt/SOP/Agent/Template |

---

## TikTok AI Seller Prompt Skill

สกิลนี้ใช้สำหรับเปลี่ยนลิงก์ TikTok / Reels / Shorts / ข้อความตัวอย่าง ให้กลายเป็นระบบผลิตคอนเทนต์ขายของแบบทำซ้ำได้

ไฟล์หลัก:

```text
skills/tiktok-ai-seller-prompt/
├── index.html
├── SKILL.md
├── README.md
├── prompt-library.md
├── sop-content-war-room.md
├── agent-workflow.md
├── guardrails.md
├── templates/
│   ├── product-brief-template.md
│   ├── daily-production-board.md
│   └── content-calendar-template.csv
└── examples/
    └── sample-output.md
```

---

## วิธีใช้งาน TikTok Skill แบบเร็ว

1. เปิด `skills/tiktok-ai-seller-prompt/`
2. กรอกสินค้า ราคา กลุ่มเป้าหมาย Pain point จุดขาย และข้อห้าม
3. กดสร้าง `Master Prompt` หรือ `Script Pack`
4. Copy Output ไปใช้กับ ChatGPT / Claude / Gemini
5. นำ Script ไปถ่ายคลิป
6. ใช้ `guardrails.md` ตรวจคำเคลมก่อนโพสต์
7. บันทึกผลลง `content-calendar-template.csv`

---

## Prompt เรียกใช้งานสั้น

```text
ใช้สกิล tiktok-ai-seller-prompt กับสินค้านี้ แล้วสร้าง Hook, Script, Caption, CTA, Hashtag, Calendar และ Compliance Check ให้พร้อมใช้งาน
```

---

## Roadmap ถัดไป

- [ ] เพิ่ม Shopee Affiliate Product Research Skill
- [ ] เพิ่ม Facebook/Reels Repurpose Skill
- [ ] เพิ่ม Performance Tracker Dashboard
- [ ] เพิ่ม CSV Import/Export ในหน้าเว็บ
- [ ] เพิ่ม LocalStorage หลายสินค้า
- [ ] เพิ่มระบบจัดอันดับ Winner Product
- [ ] เพิ่ม Codex task checklist สำหรับต่อยอดเป็นแอปจริง

---

## หลักการ repo นี้

แยกทุกสกิลเป็นโมดูล ไม่รวมทุกอย่างไว้ไฟล์เดียว เพราะงานจริงต้องดูแลต่อได้ ไม่ใช่กองเอกสารดิจิทัลที่เปิดแล้วอยากปิด
