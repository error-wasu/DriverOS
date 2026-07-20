# DriverOS — Product Discovery

> 🔄 **อัปเดต 2026-07-15:** กรอบความคิดของเฟสนี้เปลี่ยนจาก "Product Discovery" (หา Feature) เป็น **"Behavior Discovery"** (หาว่ามนุษย์ตัดสินใจอย่างไร) — ดูเหตุผลที่ `decisions/019-behavior-discovery-reframe.md` ชื่อโฟลเดอร์/Gate ยังคงเดิมเพื่อไม่ให้ลิงก์พัง

โฟลเดอร์นี้เก็บเอกสารทั้งหมดของขั้นตอน **Product Discovery** ก่อนเข้าสู่ Development

> ⚠️ **กฎสำคัญ:** ห้ามเขียนโค้ด ห้ามออกแบบ Database Schema ห้ามออกแบบ API ในเฟสนี้
> ทุกอย่างในโฟลเดอร์นี้คือ Documentation, Research และ Design Artifacts เท่านั้น

> 📌 **เอกสารเพิ่มเติมนอก product/:** `/WHY_DRIVEROS_EXISTS.md`, `/FOUNDER_LOG.md`, `/AI_WORKFLOW.md`, `/decisions/`, `/research/`

## Roadmap ปัจจุบัน

```
Vision ✅        (Gate 1 — Approved)
   ↓
Research ✅      (รวมอยู่ใน Vision/Gate 1)
   ↓
User Journey 🟡  (Gate 2 — Draft, ยังไม่ส่งขออนุมัติ)  ← อยู่ตรงนี้
   ↓
Wireframe ⬜     (Gate 3 — Not Started)
   ↓
Feature List ⬜  (หลัง Gate 3)
   ↓
PRD ⬜           (Gate 4)
   ↓
Database / API / Development  (ยังไม่เริ่ม จนกว่า Gate 4 จะผ่าน)
```

## โครงสร้างโฟลเดอร์

```
product/
├── README.md                    ← ไฟล์นี้
├── PROCESS_GATES.md             ← กฎ Approval Gate ทั้ง 4 ด่าน
├── STANDARDS.md                 ← มาตรฐานการเขียนเอกสารในโปรเจกต์
├── discovery/
│   ├── gate-1-vision/           ← Vision & Research (Approved)
│   ├── gate-2-user-journey/     ← User Journey Map (Pending)
│   ├── gate-3-wireframe/        ← Wireframe (ยังไม่เริ่ม)
│   └── gate-4-prd/              ← PRD (ยังไม่เริ่ม)
└── templates/
    ├── user-journey-template.md
    ├── gate-approval-template.md
    └── adr-template.md
```

## บทบาทที่เกี่ยวข้องกับเฟสนี้

- **Founder** — Product Owner, ตัดสินใจ Approve/Reject แต่ละ Gate
- **Claude (Senior Product Designer)** — ทำ Gate 2–3 (User Journey, Wireframe)
- **Claude (Scribe — Documentation & Knowledge Architect)** — ดูแลโครงสร้างเอกสาร, Template, มาตรฐาน, จัดระเบียบ Repository

## สถานะล่าสุด

| Gate | สถานะ | ไฟล์หลัก |
|---|---|---|
| 1. Vision | ✅ Approved | `discovery/gate-1-vision/` |
| 2. User Journey | 🟡 Draft | `discovery/gate-2-user-journey/DriverOS_User_Journey_Map_v1.md` |
| 3. Wireframe | ⬜ Not Started | — |
| 4. PRD | ⬜ Not Started | — |
