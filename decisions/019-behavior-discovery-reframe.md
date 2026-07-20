# Decision #019 — Reframe: Product Discovery → Behavior Discovery

**วันที่:** 2026-07-15
**สถานะ:** Proposed
**Priority:** 🔴 Critical

## บริบท

จนถึงตอนนี้ DriverOS ใช้กรอบ "Product Discovery" (ค้นหาว่าจะสร้าง Feature อะไร) แต่จากงานวิจัยที่ผ่านมา (Gate 2, Founder Sessions) พบว่าสิ่งที่ทีมกำลังทำจริงๆ คือการค้นหาว่า **มนุษย์ (คนขับ) ตัดสินใจอย่างไร** — ไม่ใช่การหา feature

## การตัดสินใจ

เปลี่ยนชื่อกรอบการทำงานจาก **Product Discovery** เป็น **Behavior Discovery**

- ชื่อโฟลเดอร์ `product/discovery/` และ Gate 1-4 **ยังคงเดิม** (ไม่ rename path เพื่อไม่ให้ลิงก์ที่มีอยู่พัง)
- เปลี่ยนเฉพาะ **กรอบความคิด/หัวเอกสาร** ให้สะท้อนว่านี่คือการวิจัยพฤติกรรม ไม่ใช่การหา feature list

## เหตุผล

- DriverOS ศึกษา **Decision** มากกว่า **Pain**
- Decision Model กำลังกลายเป็นแกนกลางของ Product (ดู `research/decision-model.md`)
- DriverOS ไม่ใช่ AI ที่ตัดสินใจแทนคนขับ แต่คือระบบที่เติมข้อมูลที่คนขับยังไม่มี เพื่อให้เขาตัดสินใจได้ดีขึ้น

## สิ่งที่เปลี่ยนแปลง

- `product/README.md`, `product/PROCESS_GATES.md` — เพิ่ม callout อธิบายกรอบใหม่
- Founder Research → เปลี่ยนรูปแบบเป็น **Field Notes** (ดู `research/field-notes/`)
- เพิ่มไฟล์ใหม่: `research/decision-model.md`, `research/RESEARCH_QUESTIONS.md`, `research/spatial-behavior.md`, `research/RESEARCH_PRINCIPLES.md`, `/CURRENT_BELIEFS.md`
- `PROBLEM_LOG.md` — ปรับ status บางรายการจาก Validated เป็น Emerging Evidence ให้สอดคล้องกับหลัก "Founder Observation != Market Truth"

## ยังไม่ทำ (นอกขอบเขต)

Wireframe, Flutter, OCR, GPS, Database, API
