# DriverOS — Product Discovery Approval Gates

> 🔄 ตั้งแต่ 2026-07-15 กรอบความคิดของ Gate เหล่านี้คือ **Behavior Discovery** ไม่ใช่แค่การหา Feature (ดู `decisions/019-behavior-discovery-reframe.md`) — เกณฑ์การผ่านแต่ละ Gate ด้านล่างยังใช้ได้เหมือนเดิม เพียงแต่ต้องตีความผ่านเลนส์ "เข้าใจพฤติกรรม/การตัดสินใจของคนขับ" เป็นหลัก

เอกสารนี้กำหนดกฎการผ่านแต่ละขั้นของ Product Discovery ก่อนเข้าสู่ Development
**หลักการ:** ไม่มี Gate ไหนผ่านได้โดยไม่มีการอนุมัติจาก Founder อย่างชัดเจน

---

## Gate 1 — Vision ✅ Approved

**เป้าหมาย:** นิยามปัญหา, กลุ่มผู้ใช้, และเหตุผลที่ DriverOS ควรมีอยู่
**Output:** เอกสาร Vision + Research สรุปตลาด/ผู้ใช้
**เกณฑ์ผ่าน Gate:** Founder ยืนยันว่าปัญหาที่ระบุคือปัญหาจริงที่คุ้มค่าจะแก้

---

## Gate 2 — User Journey 🟡 Pending

**เป้าหมาย:** เข้าใจพฤติกรรมจริงของผู้ใช้แบบ As-Is ก่อนออกแบบ To-Be
**Output:**
- As-Is Journey Map (พฤติกรรมปัจจุบันโดยไม่มี DriverOS)
- Pain Points ที่ Validate แล้วจากผู้ใช้จริง
- To-Be Journey แนวคิดเบื้องต้น (ยังไม่ใช่ UI)
- การตัดสินใจสถาปัตยกรรมเชิงแนวคิด (เช่น interaction model)

**เกณฑ์ผ่าน Gate:**
- Founder ยืนยันว่า Journey ตรงกับพฤติกรรมจริง ไม่ใช่การเดาของทีม
- ไม่มีสมมติฐานสำคัญที่ยังไม่ผ่านการตรวจสอบ (unvalidated assumption)

**ห้ามทำในเฟสนี้:** ออกแบบหน้าจอ, เขียน user flow แบบละเอียด, เขียนโค้ด

---

## Gate 3 — Wireframe ⬜ Not Started

**เป้าหมาย:** แปลง To-Be Journey เป็น Low-Fidelity Wireframe
**Output:**
- User Flow (ลำดับการใช้งานแบบละเอียด)
- Information Architecture
- Low-Fi Wireframe ของแต่ละหน้าจอ/notification
- Feature Prioritization เบื้องต้น

**เกณฑ์ผ่าน Gate:** Founder ในฐานะผู้ใช้จริงรู้สึกว่า "นี่แหละแอปที่อยากใช้" (ไม่ใช่แค่ผ่านทาง logic)

**ห้ามทำในเฟสนี้:** High-fidelity UI, โค้ด, Database Schema

---

## Gate 4 — PRD ⬜ Not Started

**เป้าหมาย:** สรุป Requirement ที่พร้อมส่งต่อให้ทีม Engineering
**Output:** Product Requirement Document ฉบับสมบูรณ์ (Feature spec, Success metrics, Edge cases, Non-functional requirements)

**เกณฑ์ผ่าน Gate:** Founder อนุมัติ PRD → เริ่ม Database Design และ Development ได้

---

## สถานะเอกสารในแต่ละ Gate

| สถานะ | ความหมาย | Implement ได้ไหม |
|---|---|---|
| 🟡 Draft | กำลังร่าง ยังไม่ส่งขออนุมัติ | ❌ ห้ามเด็ดขาด |
| 🟠 Pending Approval | ส่งให้ Founder พิจารณาแล้ว รอผล | ❌ ห้ามเด็ดขาด |
| ✅ Approved | Founder อนุมัติแล้ว | เปิด Gate ถัดไปได้เท่านั้น (ไม่ได้แปลว่า implement code) |
| ❌ Rejected | ต้องแก้ไขใหม่ | ❌ |

**กฎเหล็ก:** ไม่ว่าเอกสารจะอยู่สถานะไหนก็ตาม ห้ามเขียนโค้ด ห้ามออกแบบ Database ห้ามออกแบบ API จนกว่าจะผ่าน **Gate 4 (PRD)** แบบ Approved เท่านั้น

## กติกาการอนุมัติ (ทุก Gate)

1. ใช้ `templates/gate-approval-template.md` บันทึกการอนุมัติทุกครั้ง
2. Gate ที่ผ่านแล้วห้ามแก้ย้อนหลังโดยไม่เปิด Change Request ใหม่
3. ห้ามข้าม Gate แม้จะรู้สึกว่า "เร่งได้" — ทุก Gate มีไว้ป้องกันการสร้างของที่ผิดตั้งแต่ต้น
