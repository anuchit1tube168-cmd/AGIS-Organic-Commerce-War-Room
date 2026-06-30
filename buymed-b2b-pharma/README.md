# AGIS MedSupply B2B Hub

ต้นแบบระบบ B2B สำหรับร้านยา คลินิก โรงพยาบาล และหน่วยแพทย์ ถอดแนวคิดจาก marketplace ขายส่งเวชภัณฑ์ออนไลน์ แล้วปรับเป็นโครงที่ใช้งานจริงได้บน GitHub Pages โดยไม่คัดลอกแบรนด์หรือทรัพย์สินของเว็บไซต์ต้นทาง

## เปิดใช้งาน

GitHub Pages path:

```text
https://anuchit1tube168-cmd.github.io/AGIS-Organic-Commerce-War-Room/buymed-b2b-pharma/
```

## ฟังก์ชันในต้นแบบ

1. Marketplace ค้นหา/กรองสินค้า
2. Cart และสร้าง PO demo
3. Buyer Verify สำหรับร้านยา/คลินิก/โรงพยาบาล/หน่วยแพทย์
4. สินค้าควบคุมแบบ lock ก่อนอนุมัติ
5. Dashboard จาก localStorage
6. Export order เป็น JSON
7. Integration Stack สำหรับ Google Sheet, Apps Script, LINE OA, Firebase/Supabase, ERP
8. SOP แยก Phase 1 และ Phase 2

## ระบบที่เชื่อมได้จริง

### Phase 1: ฟรีเร็วสุด

- GitHub Pages: Frontend
- Google Sheet: Orders / Products / Buyers
- Apps Script Web App: รับ POST จากหน้าเว็บ
- LINE OA หรือ LINE Messaging API: แจ้งเตือนแอดมินเมื่อมี PO
- Google Drive: เก็บเอกสารแนบ/หลักฐาน

เหมาะกับการทดลองภายในหรือ MVP

### Phase 2: โตจริง

- Firebase Auth หรือ Supabase Auth
- Firestore / Supabase PostgreSQL
- Storage สำหรับใบอนุญาตและหลักฐานโอน
- Role-based access: buyer, pharmacist, admin, finance, warehouse
- Realtime dashboard

เหมาะกับผู้ใช้จำนวนมากขึ้นและต้องมีสิทธิ์แยกตามบทบาท

### Phase 3: องค์กร

- ERP / Inventory API
- Payment proof / payment gateway
- Logistics tracking
- Invoice / Tax invoice
- Audit log
- PDPA consent
- Admin approval workflow

## โครง Google Sheet ที่แนะนำ

### Sheet: Products

| product_id | name | category | price | stock | controlled | status |
|---|---|---|---:|---:|---|---|

### Sheet: Buyers

| buyer_id | shop_name | buyer_type | license_no | phone | line_user_id | verify_status | created_at |
|---|---|---|---|---|---|---|---|

### Sheet: Orders

| order_id | buyer_id | items_json | total | status | payment_status | created_at |
|---|---|---|---:|---|---|---|

## ข้อจำกัดสำคัญ

ระบบนี้เป็นต้นแบบเพื่อการศึกษาและวางระบบ ห้ามใช้ขายยา/สินค้าควบคุมจริงโดยไม่ตรวจข้อกฎหมาย ใบอนุญาต ผู้ประกอบวิชาชีพ และเงื่อนไขแพลตฟอร์ม
