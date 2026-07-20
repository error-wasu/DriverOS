# DEC-022 — Luther Review 2026-07-16

**สถานะ:** ✅ Approved
**วันที่:** 2026-07-16
**หมายเหตุ:** นี่คือ Decision แรกที่ใช้ ID Scheme แบบ prefix (`DEC-`) ต่อเนื่องจากเลข `021` เดิม (ดู `docs/NAMING_CONVENTION.md`)

## Reason

Luther review งานทั้งหมดของ Sprint 1 จนถึงตอนนี้ พบว่าโครงสร้าง (HQ, Scout, CLAUDE.md, Decision Package Gate) นิ่งพอจะ freeze ได้แล้ว แต่ยังขาดการฟันธงเรื่อง Product Identity (CR-001) และความเสี่ยงที่ทีมเริ่มเน้นสร้างเอกสารมากกว่าเก็บ Evidence จริง

## Approved

| รายการ | สถานะ |
|---|---|
| HQ-001 | ✅ Approved — **Freeze v1** ห้ามแก้โครงสร้างอีก แก้ได้เฉพาะ Bug / Missing Link / Documentation |
| Scout v2 (`research/community/SCOUT_COWORK_BRIEF.md`) | ✅ Approved — **Mature** ห้ามแก้ prompt อีกพักใหญ่ Priority ตอนนี้คือ Collect Evidence ไม่ใช่ Improve Prompt |
| CLAUDE.md | ✅ Approved |
| Decision Package Gate | ✅ Approved |
| ID Scheme (prefix format) | ✅ Approved — ดู `docs/NAMING_CONVENTION.md` |

## Challenge (บันทึกไว้ ยังไม่ implement วันนี้)

1. **HQ ยังไม่ใช่ Operational System** — ตอนนี้เป็นแค่ Documentation (อ่านอย่างเดียว) ยังขาด Execution Status/Tracking loop (อ่าน→Action→Update→Track) → เสนอเป็น **HQ v1.1** ในอนาคต ไม่ใช่ตอนนี้
2. **Scout: Data = 0 คือ Risk อันดับหนึ่ง** — Prompt ดีแล้วแต่ยังไม่มี Evidence จริงเข้ามาเลย
3. **Atlas ห้ามเริ่มสร้าง Belief จนกว่า Scout จะมี Data**
4. **Scribe ต้องรักษากฎเดิม "Document, Don't Design"**

## 🔴 Priority 1 — CR-001

CR-001 (เปลี่ยน JTBD) ถูกยกระดับเป็น **Priority 1 เหนือทุกอย่าง** เพราะเป็น Product Identity ไม่ใช่แค่รายละเอียด — ต้องมี **Decision Session แยกต่างหาก** ไม่ปนกับงานอื่น (ยังไม่ได้จัด — ดู `hq/NEXT_ACTIONS.md`)

## Sprint 01 — Re-Prioritized

| Priority | รายการ |
|---|---|
| P0 | CR-001 (JTBD) |
| P0 | Scout — Collect Evidence |
| P1 | Decision Model |
| P2 | Atlas |
| P3 | Automation |
| P4 | n8n |

## สิ่งที่ Founder ต้องทำ (3 ข้อ)

1. Approve/Reject CR-001 (ผ่าน Decision Session แยก)
2. ให้ Scout เริ่มเก็บข้อมูลจริง — **ไม่แก้ Prompt ไม่แก้ Framework**
3. วิ่ง Grab แล้วบันทึก Decision Cases เพิ่ม

## ห้ามทำ (ย้ำ)

❌ เพิ่ม Persona · ❌ เพิ่ม AI · ❌ เพิ่ม Folder · ❌ เพิ่ม Framework · ❌ เปลี่ยน Vision

## Principle ใหม่ (บันทึกไว้ที่ `research/RESEARCH_PRINCIPLES.md` ด้วย)

> ถ้า Evidence ไม่เพิ่ม แต่ Documentation เพิ่ม แปลว่าเราเริ่มเดินผิดทาง

Sprint หน้าวัดผลด้วย: จำนวน Decision Cases เพิ่ม, จำนวน Community Evidence เพิ่ม, จำนวนบทสัมภาษณ์เพิ่ม — **ไม่ใช่จำนวนไฟล์ Markdown ที่เพิ่ม**

## สิ่งที่เปลี่ยนแปลง (ไฟล์ที่แก้)

- `docs/NAMING_CONVENTION.md` — เพิ่ม ID Scheme
- `decisions/README.md` — resolve ID Scheme note, เพิ่ม index นี้
- `hq/CURRENT_MISSION.md`, `hq/DASHBOARD.md`, `hq/NEXT_ACTIONS.md` — อัปเดต priority ตาม Sprint 01 ใหม่ + เพิ่มรายการ "ห้ามทำ"
- `hq/README.md` — เพิ่มสถานะ Freeze v1
- `research/community/SCOUT_COWORK_BRIEF.md` — mark เป็น Mature/Frozen
- `research/RESEARCH_PRINCIPLES.md` — เพิ่ม Evidence vs Documentation principle
- `CURRENT_BELIEFS.md` — เพิ่ม Belief ID ตาม prefix scheme ใหม่
- `SPRINT_LOG.md` — อัปเดต priority breakdown
