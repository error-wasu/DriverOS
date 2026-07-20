# Next Actions

แต่ละ Action ต้องมี Priority / Owner / Status / Dependencies เสมอ — Blue เป็นผู้ดูแลไฟล์นี้ให้เป็นปัจจุบัน

## Founder

| Action | Priority | Status | Dependencies |
|---|---|---|---|
| จัด **Decision Session แยก** เพื่อฟันธง CR-001 (ไม่ปนกับงานอื่น) | 🔴 P0 | Not Started | — |
| อนุมัติ/ปฏิเสธ CR-001 (JTBD change) ในระหว่าง Decision Session นั้น | 🔴 P0 | Pending | Decision Session ข้างบน |
| รัน Scout Cowork Brief เพื่อเก็บ Community Evidence — **ไม่แก้ Prompt** ไปเก็บข้อมูลจริงเลย | 🔴 P0 | Not Started | Cowork + Claude in Chrome (พร้อมแล้ว) |
| วิ่ง Grab แล้วบันทึก Decision Cases เพิ่ม | 🟠 P1 | Ongoing | `research/field-notes/` |

## Blue

| Action | Priority | Status | Dependencies |
|---|---|---|---|
| ตั้ง cadence ของ Weekly Review รอบแรก | 🟠 High | Not Started | — |
| ดูแล `hq/INBOX.md` ให้ไม่ค้าง | 🟡 Medium | Ongoing | — |

## Scout

| Action | Priority | Status | Dependencies |
|---|---|---|---|
| Execute `research/community/SCOUT_COWORK_BRIEF.md` v2.0 (**Mature/Frozen — ห้ามแก้ prompt อีก**) | 🔴 P0 | Blocked | รอ Founder รัน Cowork |

## Atlas

| Action | Priority | Status | Dependencies |
|---|---|---|---|
| Link Evidence ใหม่จาก Scout เป็น Insight — **ห้ามสร้าง Belief ใหม่จนกว่า Scout จะมี Data** | 🟡 P2 | Blocked | รอผลจาก Scout |

## Scribe

| Action | Priority | Status | Dependencies |
|---|---|---|---|
| ดูแล HQ ให้ตรงกับความจริงของ repo — **HQ Frozen v1: แก้ได้เฉพาะ Bug/Missing Link/Documentation** | 🔴 Critical | Ongoing | `decisions/DEC-022-luther-review-2026-07-16.md` |
| Refactor คำศัพท์ที่ไม่ตรงมาตรฐานเมื่อพบ | 🟡 Medium | Ongoing | `docs/LANGUAGE_GUIDE.md` |
| รักษากฎ **"Document, Don't Design"** — ไม่ตัดสินใจเชิง Product เอง | 🔴 Critical | Ongoing | — |

## Luther

| Action | Priority | Status | Dependencies |
|---|---|---|---|
| Review ผล Scout เมื่อเสร็จ แล้วกำหนด priority ของ Sprint ถัดไป | 🟠 High | Blocked | รอผลจาก Scout |
