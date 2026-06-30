# SKILL: ถอดระบบจัดซื้อเวชภัณฑ์ B2B ให้เป็น Prototype ใช้งานจริง

## เป้าหมาย

แปลงเว็บไซต์ต้นแบบแนว B2B medical supply ให้เป็นระบบต้นแบบที่ทดลองใช้งานได้บน GitHub Pages โดยไม่คัดลอกแบรนด์ รูปภาพ ข้อความ หรือข้อมูลเฉพาะของเว็บไซต์ต้นทาง

## ขอบเขตที่ปลอดภัย

ระบบนี้ใช้สำหรับการศึกษา การวางโครงระบบ และการจัดซื้อเวชภัณฑ์ทั่วไปเท่านั้น ก่อนเปิดใช้งานจริงต้องตรวจข้อกำกับทางกฎหมาย ใบอนุญาต ข้อมูลส่วนบุคคล และขั้นตอนอนุมัติภายในองค์กร

## ขั้นตอนถอดโปรเจกต์

1. แยก Business Model
   - กลุ่มลูกค้า: ร้านค้า คลินิก หน่วยงาน หรือองค์กร
   - ประเภทสินค้า: เวชภัณฑ์ทั่วไป อุปกรณ์ดูแลสุขภาพ อุปกรณ์สำนักงานทางการแพทย์
   - รายได้: ราคาส่ง ค่าบริการ ค่าสมาชิก หรือค่าดำเนินการ

2. แยก User Flow
   - สมัครหรือเข้าสู่ระบบ
   - ตรวจสอบข้อมูลผู้ซื้อ
   - ค้นหาและกรองสินค้า
   - เพิ่มสินค้าเข้ารถเข็น
   - สร้างใบสั่งซื้อ
   - แนบหลักฐานหรือเอกสารที่จำเป็น
   - Admin ตรวจสอบ
   - อัปเดตสถานะคำสั่งซื้อ

3. แยก Data Model
   - Products
   - Buyers
   - Orders
   - OrderItems
   - Documents
   - Payments
   - StockLogs
   - Notifications

4. แยกหน้าระบบ
   - Home
   - Catalog
   - Cart
   - Purchase Order
   - Buyer Verify
   - Admin Dashboard
   - Order Tracking
   - Integration Settings

5. แยกระบบเชื่อมต่อ
   - GitHub Pages: frontend
   - Google Sheet: database เริ่มต้น
   - Apps Script Web App: webhook/API
   - LINE OA: แจ้งเตือนผู้ดูแล
   - Firebase หรือ Supabase: auth, database, storage
   - ERP/Inventory API: ใช้เมื่อระบบโตขึ้น

## Prompt ใช้งานซ้ำ

```text
ถอดเว็บไซต์นี้ให้เป็นระบบ B2B medical supply prototype ที่ใช้งานจริงได้บน GitHub Pages โดยไม่คัดลอกแบรนด์ต้นทาง ให้แยก business model, user flow, data model, feature list, integration points, compliance risks, MVP phase, production phase และสร้างไฟล์ index.html พร้อม README.md และ SKILL.md

ระบบต้องมี Marketplace, Search/filter, Cart, Purchase Order, Buyer verification, Admin dashboard, Google Sheet/Apps Script integration plan, LINE OA notification plan และทางเลือก Firebase/Supabase สำหรับระบบโตจริง
```

## Checklist ก่อน production

- [ ] ตรวจข้อกฎหมายและข้อกำกับของสินค้า
- [ ] ตรวจข้อมูลผู้ซื้อและเอกสารที่เกี่ยวข้อง
- [ ] แยกสิทธิ์ buyer/admin/finance/warehouse
- [ ] ทำ privacy notice และ consent
- [ ] บันทึก audit log
- [ ] ห้ามเก็บ secret key ใน frontend
- [ ] ใช้ backend ตรวจสิทธิ์ทุก action
- [ ] มีขั้นตอนสำรองข้อมูล

## Output มาตรฐาน

- index.html สำหรับ demo
- README.md สำหรับคู่มือโปรเจกต์
- SKILL.md สำหรับทำซ้ำ
- โครง Google Sheet หรือ Database
- รายการ API ที่ต้องต่อ
- รายการความเสี่ยงและข้อจำกัด
