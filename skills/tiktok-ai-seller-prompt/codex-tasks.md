# Codex Tasks — TikTok AI Seller Prompt Skill

ไฟล์นี้คือรายการงานสำหรับให้ Codex หรือ AI Engineer ต่อยอดจากหน้า HTML ปัจจุบันไปเป็น mini app ที่ใช้งานจริงขึ้น

---

## Phase 1 — Harden Current Tool

### Task 1.1 — ตรวจโครงสร้างไฟล์

```text
ตรวจโครงสร้าง skills/tiktok-ai-seller-prompt ทั้งหมด
ยืนยันว่า index.html, SKILL.md, README.md, prompt-library.md, sop-content-war-room.md, agent-workflow.md, guardrails.md, templates และ examples ยังอยู่ครบ
ห้ามลบไฟล์เอกสารเดิม
```

### Task 1.2 — ปรับ UI มือถือ

```text
ปรับ index.html ให้ใช้งานบนมือถือจอเล็กได้ดีขึ้น
ตรวจ input, textarea, button, output box ไม่ล้นจอ
ห้ามใช้ framework เพิ่ม
ใช้ HTML/CSS/JavaScript เดิมเท่านั้น
```

### Task 1.3 — เพิ่ม Print Mode

```text
เพิ่มปุ่ม Print Report ใน index.html
เมื่อกดแล้วให้พิมพ์เฉพาะ Output ที่สร้างไว้
เพิ่ม CSS @media print ให้พื้นหลังขาว ตัวหนังสือดำ อ่านง่าย
```

---

## Phase 2 — Multi Product LocalStorage

### Task 2.1 — บันทึก Product Brief หลายตัว

```text
เพิ่มระบบ Save Product Brief ลง localStorage
ผู้ใช้สามารถตั้งชื่อสินค้า กด Save แล้วเรียกกลับมาแก้ได้
แสดงรายการสินค้าที่บันทึกไว้ด้านล่างฟอร์ม
```

### Task 2.2 — Import / Export JSON

```text
เพิ่มปุ่ม Export JSON และ Import JSON
Export ต้องรวม Product Brief ทั้งหมดที่บันทึกใน localStorage
Import ต้องตรวจ JSON ก่อนบันทึก ถ้าไฟล์ผิดให้แจ้ง error เป็นภาษาไทย
```

### Task 2.3 — Clear เฉพาะสินค้า

```text
เพิ่มปุ่มลบ Product Brief รายตัว
ห้ามล้าง localStorage ทั้งหมดโดยไม่ถามยืนยัน
```

---

## Phase 3 — Content Board

### Task 3.1 — สร้างตารางไอเดียคลิป

```text
เพิ่ม Content Idea Board ใน index.html
ช่องที่ต้องมี:
- clip_id
- product
- content_pillar
- hook
- script_status
- shoot_status
- edit_status
- post_status
- notes
```

### Task 3.2 — Export CSV

```text
เพิ่ม Export CSV สำหรับ Content Idea Board
ชื่อไฟล์: tiktok-content-board-YYYYMMDD.csv
ต้องรองรับภาษาไทย UTF-8 BOM เพื่อเปิดใน Excel แล้วไม่เพี้ยน
```

### Task 3.3 — Import CSV

```text
เพิ่ม Import CSV สำหรับ Content Idea Board
ถ้า column ไม่ครบ ให้แจ้งว่าขาด column ใด
```

---

## Phase 4 — Performance Tracker

### Task 4.1 — เพิ่มฟอร์มบันทึกผลคลิป

```text
เพิ่ม Performance Tracker ใน index.html
ช่องที่ต้องมี:
- clip_id
- platform
- views_24h
- avg_watch_time
- completion_rate
- likes
- comments
- shares
- cart_clicks
- orders
- revenue
```

### Task 4.2 — คำนวณ Winner Score

```text
เพิ่มสูตร winner_score จากค่าต่อไปนี้:
views_24h, completion_rate, shares, cart_clicks, orders, revenue
ให้ normalize แบบง่าย และแสดงคะแนน 0-100
```

### Task 4.3 — สรุป Winner

```text
แสดง Top 5 คลิปตาม winner_score
พร้อมคำแนะนำ next_action:
- ทำซ้ำ
- เปลี่ยน Hook
- เปลี่ยน CTA
- หยุดแนวนี้
```

---

## Phase 5 — Prompt Engine Upgrade

### Task 5.1 — เพิ่ม Content Pillar Selector

```text
เพิ่ม checkbox เลือก content_pillar:
Problem, How-to, Review, Compare, FAQ, Storytelling, Trend Adaptation
เมื่อสร้าง Prompt ให้ใช้เฉพาะ pillar ที่เลือก
```

### Task 5.2 — เพิ่ม Risk Level Selector

```text
เพิ่ม selector ระดับความเสี่ยงสินค้า:
Low, Medium, High
ถ้า High ให้ Prompt บังคับ Compliance Check เข้มขึ้น
```

### Task 5.3 — เพิ่ม Platform Preset

```text
เพิ่ม preset สำหรับ TikTok Shop, Shopee Video, Facebook Reels, YouTube Shorts
แต่ละ platform ให้ปรับความยาวคลิป CTA และ Caption style ต่างกัน
```

---

## Phase 6 — Professional Report

### Task 6.1 — สร้างหน้า Report

```text
เพิ่มปุ่ม Generate Report
สร้างรายงาน Markdown จาก Product Brief + Prompt Output + Content Plan + Performance Summary
```

### Task 6.2 — Export Report เป็น .md

```text
เพิ่ม Download Report .md
ชื่อไฟล์: tiktok-seller-report-YYYYMMDD.md
```

### Task 6.3 — Print Report

```text
ปรับ Print Report ให้เหมาะกับ A4
หัวข้อชัดเจน ตารางไม่ล้นหน้า
```

---

## Phase 7 — Quality Rules

ทุก task ต้องรักษากฎนี้:

- ห้ามเพิ่ม dependency ภายนอก
- ห้ามใช้ API key
- ห้ามส่งข้อมูลออกนอก browser
- ใช้ localStorage เท่านั้นในระยะ MVP
- ภาษาไทยต้องไม่เพี้ยน
- Mobile first
- Copy/Download ต้องใช้งานได้จริง
- แยก logic ให้ชัด ไม่เขียนมั่วจน index.html แก้ต่อไม่ได้

---

## Done Definition

งานถือว่าเสร็จเมื่อ:

- เปิดผ่าน GitHub Pages ได้
- ใช้งานบนมือถือได้
- Save/Load product ได้
- Export/Import ได้
- สร้าง Prompt ได้
- บันทึก Performance ได้
- คำนวณ Winner Score ได้
- Print/Download Report ได้
- ไม่มี error ใน console ตอนใช้งานพื้นฐาน
