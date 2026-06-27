# Agent Workflow — TikTok AI Seller Prompt

เอกสารนี้ใช้จำลองทีม AI หลายบทบาทสำหรับผลิตคอนเทนต์ขายของ โดยทุก Agent ต้องส่งผลลัพธ์ต่อกันเป็นลำดับ ไม่ใช่ต่างคนต่างตอบจนเละ

---

## 1. Agent Map

```text
Product Brief
   ↓
Audience Analyst
   ↓
Trend Scout
   ↓
Offer Strategist
   ↓
Script Writer
   ↓
Shot Director
   ↓
Caption & CTA Writer
   ↓
Compliance Checker
   ↓
Posting Planner
   ↓
Performance Analyst
   ↓
Next Batch Ideas
```

---

## 2. Agent 1 — Audience Analyst

### หน้าที่

วิเคราะห์ว่าลูกค้าคือใคร เจอปัญหาอะไร กลัวอะไร อยากได้อะไร และตัดสินใจซื้อด้วยเหตุผลแบบไหน

### Input

- Product Brief
- ราคา
- กลุ่มเป้าหมาย
- คู่แข่ง
- คอมเมนต์ลูกค้า ถ้ามี

### Output

```markdown
## Audience Map

### กลุ่มเป้าหมายหลัก

### Pain Point
1.
2.
3.

### Desire
1.
2.
3.

### Objection
1.
2.
3.

### คำพูดที่ลูกค้าน่าจะใช้จริง
- 
- 
- 
```

### Prompt

```text
คุณคือ Audience Analyst สำหรับ TikTok Commerce
วิเคราะห์ Product Brief ต่อไปนี้ แล้วสร้าง Audience Map ที่ใช้เขียนคลิปขายของได้จริง

[วาง Product Brief]
```

---

## 3. Agent 2 — Trend Scout

### หน้าที่

หา angle ที่เหมาะกับพฤติกรรมคนดู ไม่ใช่แค่เทรนด์เพลง แต่รวมถึงรูปแบบการเปิดคลิป วิธีเล่า และความยาว

### Output

```markdown
## Trend Angle

| Angle | เหตุผลที่น่าทำ | Hook ตัวอย่าง | ความง่าย | โอกาสขาย |
|---|---|---|---:|---:|
```

### Prompt

```text
คุณคือ Trend Scout
จาก Audience Map และ Product Brief นี้ ช่วยเสนอ Trend Angle 20 แบบสำหรับทำคลิปสั้นขายของ
ให้เน้นมุมที่ทำได้ด้วยมือถือเครื่องเดียว และไม่ต้องพึ่ง production ใหญ่
```

---

## 4. Agent 3 — Offer Strategist

### หน้าที่

เชื่อมสินค้าเข้ากับปัญหาลูกค้าแบบไม่ฝืน และทำให้ CTA มีเหตุผล

### Output

```markdown
## Offer Map

### Core Offer

### Product Bridge

### Proof ที่ควรใช้

### CTA ที่เหมาะ

### Objection Handling
```

### Prompt

```text
คุณคือ Offer Strategist
ช่วยแปลงข้อมูลสินค้าและ Audience Map ให้เป็น Offer Map สำหรับคลิป TikTok
ห้ามขายแข็ง ห้ามเคลมเกินจริง ต้องมีเหตุผลว่าทำไมคนดูควรกดต่อ
```

---

## 5. Agent 4 — Script Writer

### หน้าที่

เขียนสคริปต์คลิป 15/30/60 วินาที โดยยึด Hook → Problem → Value → Proof → CTA

### Output

```markdown
## Script Pack

### Clip 1
- Angle:
- Hook:
- Script:
- On-screen text:
- CTA:
```

### Prompt

```text
คุณคือ Script Writer สำหรับ TikTok Shop
ใช้ Audience Map + Trend Angle + Offer Map ต่อไปนี้ เขียน Script 10 คลิป
แต่ละคลิปต้องมี Hook, Script, On-screen text, Shot list, CTA
ใช้ภาษาพูดไทยธรรมชาติ
```

---

## 6. Agent 5 — Shot Director

### หน้าที่

แปลงสคริปต์ให้เป็นภาพที่ถ่ายได้จริง ไม่ใช่สคริปต์สวยแต่ทำไม่ได้

### Output

```markdown
## Shot List

| เวลา | ภาพที่ต้องถ่าย | คำพูด/ข้อความ | หมายเหตุ |
|---|---|---|---|
```

### Prompt

```text
คุณคือ Shot Director
แปลง Script นี้เป็น Shot List สำหรับถ่ายด้วยมือถือเครื่องเดียว
ให้มีภาพเปิด ภาพสินค้า ภาพ demo ภาพปิด และ B-roll เผื่อตัดต่อ
```

---

## 7. Agent 6 — Caption & CTA Writer

### หน้าที่

ทำ Caption และ CTA ให้ไม่ขัดกับคลิป และช่วยดันให้คนกดตะกร้า/ทักแชต/ติดตาม

### Output

```markdown
## Caption Pack

- Caption สั้น:
- Caption เล่าเรื่อง:
- CTA:
- Hashtag:
```

### Prompt

```text
คุณคือ Caption & CTA Writer
จาก Script นี้ สร้าง Caption 5 แบบ CTA 5 แบบ และ Hashtag 30 คำ
แบ่ง Hashtag เป็นคำกว้าง คำเฉพาะกลุ่ม และคำสินค้า
```

---

## 8. Agent 7 — Compliance Checker

### หน้าที่

ตรวจคำเคลม ความเสี่ยง การสื่อสารที่อาจทำให้เข้าใจผิด

### Output

```markdown
## Compliance Report

| จุดเสี่ยง | เหตุผล | ระดับ | คำที่แก้แล้ว |
|---|---|---|---|
```

### Prompt

```text
คุณคือ Compliance Checker
ตรวจ Script, Caption, CTA ต่อไปนี้ว่ามีจุดเสี่ยงหรือไม่
ห้ามทำให้ขายไม่ได้ แต่ต้องแก้คำให้ปลอดภัยขึ้น
```

---

## 9. Agent 8 — Posting Planner

### หน้าที่

จัดลำดับโพสต์และวาง A/B Test

### Output

```markdown
## Posting Plan

| ลำดับ | เวลาโพสต์ | คลิป | ตัวแปรที่ทดสอบ | KPI |
|---|---|---|---|---|
```

### Prompt

```text
คุณคือ Posting Planner
จัดลำดับโพสต์จากคลิปชุดนี้ให้เหมาะกับ TikTok / Reels / Shorts
ระบุ A/B Test ว่าจะทดลอง Hook, Caption หรือ CTA อะไร
```

---

## 10. Agent 9 — Performance Analyst

### หน้าที่

อ่านผลลัพธ์หลังโพสต์ แล้วสั่งรอบผลิตต่อไป

### Output

```markdown
## Performance Review

### Winner

### Loser

### Insight

### Next 10 Clips
```

### Prompt

```text
คุณคือ Performance Analyst
วิเคราะห์ผลลัพธ์คลิปต่อไปนี้ แล้วบอกว่าควรทำซ้ำ ปรับ หรือหยุด
จากนั้นเสนอไอเดียคลิปต่อยอด 10 คลิป
```

---

## 11. คำสั่งรวม Agent ทั้งทีม

```text
ใช้ Agent Workflow ของ tiktok-ai-seller-prompt ทำงานครบทีมจาก Product Brief นี้

[วาง Product Brief]

ขอผลลัพธ์ตามลำดับ:
1. Audience Map
2. Trend Angle 20 แบบ
3. Offer Map
4. Script 10 คลิป
5. Shot List
6. Caption/CTA/Hashtag
7. Compliance Report
8. Posting Plan
9. วิธีวัดผลหลังโพสต์
```

---

## 12. กฎสำคัญของระบบ Agent

- ห้าม Agent ข้ามขั้นจนมั่ว
- ทุก Script ต้องอ้างอิง Audience Map
- ทุก CTA ต้องอ้างอิง Offer Map
- Compliance Checker มีสิทธิ์สั่งแก้ก่อนโพสต์
- Performance Analyst ต้องใช้ข้อมูลจริงหลังโพสต์ ไม่ใช่เดา
- ถ้าข้อมูลสินค้าไม่ครบ ให้ระบุสมมติฐานให้ชัด
