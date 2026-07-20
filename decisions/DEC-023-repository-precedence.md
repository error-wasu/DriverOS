# DEC-023 — Repository Precedence Rule

**สถานะ:** ✅ Approved
**วันที่:** 2026-07-17
**เกี่ยวข้องกับ:** `decisions/DEC-022-luther-review-2026-07-16.md`, `00_DRIVEROS_CONTEXT.md`

## Reason

Luther ส่ง HANDOFF 001 ที่มี Background/Vision เขียนทับกรอบเดิมโดยไม่ตั้งใจ ("DriverOS ไม่ใช่แอปสำหรับคนขับ...") ซึ่งขัดกับ `WHY_DRIVEROS_EXISTS.md` ที่ Approved อยู่ Scribe ปฏิเสธที่จะแก้ Vision ตามนั้น และ mark เป็น "รอ reconcile" แทน — Luther ยืนยันว่านี่คือพฤติกรรมที่ถูกต้อง และเสนอกฎเพื่อป้องกันเหตุการณ์แบบนี้ในอนาคต

## Decision — Repository Precedence

ลำดับความน่าเชื่อถือของข้อมูลเมื่อแหล่งข้อมูลขัดกัน:

```
1. HQ Decision / Approved Docs   (สูงสุด)
2. Decision Records (DEC / ADR)
3. Repository Documents
4. Founder Handoff
5. Chat Conversation              (ต่ำสุด)
```

**กฎตายตัว:** ถ้า Chat หรือ Handoff ขัดกับ Repository/HQ/Decision Records — **ห้ามแก้ Repository ตาม Chat/Handoff ทันที** ให้เปิด TODO หรือ flag conflict ไว้ รอ Founder ตัดสินผ่าน Decision Session แทน

## Handoff Format ใหม่ (เปลี่ยนวิธีทำงานของ Luther/Blue)

จากนี้ Handoff จาก Luther/Blue จะแยกชัดระหว่าง:
- **FACT** (อ้างอิงเอกสารที่ Approved อยู่แล้ว) vs **PROPOSED CHANGE** (Status: Proposed, Not Approved)
- หรือ **Repository Truth** vs **Conversation Insight**

และจะสั่งงานแบบระบุ **Objective / Constraints / Inputs** แทนการยืนยันว่า "นี่คือความจริง" ตรงๆ — Constraints จะรวม: HQ is Source of Truth, Do not override Approved Docs, No Folder Creation, No Assumption, Flag Conflicts

## สิ่งที่เปลี่ยนแปลง (ไฟล์ที่แก้)

- `CLAUDE.md` — เพิ่ม Repository Precedence เป็นกฎตายตัวข้อแรก
- `hq/README.md` — cross-reference ลำดับชั้นนี้
- `research/RESEARCH_PRINCIPLES.md` — ขยายข้อ 7 (Single Source of Truth) ให้ชี้ไปยังลำดับชั้นเต็ม
- `AI_CONSTITUTION.md` — เติม TODO บางส่วนใน "Relationship to Other Documents" (ยังไม่ปิดสมบูรณ์ เพราะ Constitution เองยังไม่มีตำแหน่งในลำดับชั้นอย่างเป็นทางการ)

## ยืนยันพฤติกรรม Scribe (ไม่ใช่ Decision ใหม่ แต่บันทึกไว้เพื่อ traceability)

Luther ยืนยันว่าพฤติกรรมของ Scribe ใน Handoff ก่อนหน้า (flag conflict / ไม่สร้าง folder ใหม่ / เขียน Constitution แบบ skeleton / ไม่สร้าง Decision Log ซ้ำ) คือพฤติกรรมที่ต้องการ — ให้ใช้เป็นบรรทัดฐานสำหรับการตัดสินใจกำกวมในอนาคต
