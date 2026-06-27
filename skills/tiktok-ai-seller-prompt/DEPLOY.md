# Deploy & Usage Guide — TikTok AI Seller Prompt Skill

คู่มือนี้ใช้สำหรับเปิดหน้าเว็บสกิลบน GitHub Pages และใช้งานกับ ChatGPT / Claude / Gemini / Codex

---

## 1. URL ที่ควรใช้

### ทางลัดจาก root

```text
https://anuchit1tube168-cmd.github.io/AGIS-Organic-Commerce-War-Room/tiktok-ai-seller-prompt.html
```

### เปิดตรงเข้าโฟลเดอร์สกิล

```text
https://anuchit1tube168-cmd.github.io/AGIS-Organic-Commerce-War-Room/skills/tiktok-ai-seller-prompt/
```

### Skills Hub

```text
https://anuchit1tube168-cmd.github.io/AGIS-Organic-Commerce-War-Room/skills/
```

---

## 2. วิธีเช็กว่า GitHub Pages เปิดอยู่ไหม

เข้า GitHub repo แล้วไปที่:

```text
Settings → Pages
```

ตั้งค่า:

```text
Source: Deploy from a branch
Branch: main
Folder: /root
```

ถ้าตั้งถูก หน้าเว็บจะเปิดจาก URL รูปแบบนี้:

```text
https://USERNAME.github.io/REPOSITORY_NAME/
```

ของ repo นี้คือ:

```text
https://anuchit1tube168-cmd.github.io/AGIS-Organic-Commerce-War-Room/
```

---

## 3. วิธีใช้หน้าเว็บ

1. เปิดหน้า `tiktok-ai-seller-prompt.html`
2. กรอกข้อมูลสินค้า
3. เลือก Platform เช่น TikTok Shop / Shopee Video / Facebook Reels
4. เลือกโทนภาษาและ CTA
5. กด `สร้าง Master Prompt`, `สร้าง Script Pack` หรือ `สร้าง Calendar`
6. กด `Copy Output`
7. เอาไปวางใน ChatGPT / Claude / Gemini เพื่อให้ AI แตกงานต่อ
8. ตรวจความเสี่ยงด้วย `guardrails.md`
9. ถ่ายคลิปและบันทึกผล

---

## 4. วิธีใช้กับ Codex / GitHub

ใช้คำสั่งนี้เมื่อต้องการให้ Codex ต่อระบบ:

```text
ใน repo AGIS-Organic-Commerce-War-Room ให้พัฒนาโมดูล skills/tiktok-ai-seller-prompt ต่อจากไฟล์ที่มีอยู่
เป้าหมายคือเพิ่มระบบจัดการสินค้าหลายตัว, บันทึก LocalStorage, Export CSV, Import CSV, และ Performance Tracker
ห้ามแก้โครงสร้างไฟล์หลักโดยไม่จำเป็น
ให้คง SKILL.md, README, SOP, Agent Workflow, Guardrails และ Templates แยกกัน
```

---

## 5. Checklist หลัง Deploy

- [ ] เปิดหน้า root ได้
- [ ] เปิด Skills Hub ได้
- [ ] เปิด TikTok Skill ได้
- [ ] ปุ่ม Generate ใช้งานได้
- [ ] ปุ่ม Copy Output ใช้งานได้
- [ ] ปุ่ม Download .txt ใช้งานได้
- [ ] เปิดบนมือถือแล้วไม่แตก
- [ ] README มีลิงก์ครบ
- [ ] ไม่ทับหน้าเว็บหลักเดิม

---

## 6. ถ้าเปิดแล้วไม่อัปเดต

ให้ลอง:

```text
?fresh=20260627
```

ตัวอย่าง:

```text
https://anuchit1tube168-cmd.github.io/AGIS-Organic-Commerce-War-Room/tiktok-ai-seller-prompt.html?fresh=20260627
```

หรือรอ GitHub Pages build ใหม่สักครู่ แล้ว refresh แบบ hard reload

---

## 7. งานต่อยอดที่แนะนำ

1. เพิ่มระบบบันทึกหลาย Product Brief ใน LocalStorage
2. เพิ่ม Export/Import CSV
3. เพิ่มตาราง Performance Tracker
4. เพิ่มระบบ Winner Product Score
5. เพิ่มระบบเลือก Content Pillar
6. เพิ่ม Prompt สำหรับ TikTok Shop Affiliate โดยเฉพาะ
7. เพิ่มหน้า Print Report สำหรับส่งทีม
