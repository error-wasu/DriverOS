# DriverOS — AI Workflow

**สถานะ:** Draft
**Priority:** 🟠 High

## Flow

```
Founder
  ↓
Luther
  ↓
Blue
  ↓
HQ
  ↓
Scout
  ↓
Atlas
  ↓
Scribe
  ↓
GitHub
  ↓
Automation (n8n)
```

**ไม่มี Agent ตัวไหนคุยกันโดยตรงอีก** — ทุกคนต้องผ่าน HQ ก่อนเสมอ (ดู `hq/README.md`)

### Decision Package Gate (ทางเข้าของ Scribe โดยเฉพาะ)

```
Founder
    ↓
Blue
    ↓
Decision Package
    ↓
Scribe
    ↓
GitHub
```

กฎตายตัว:
- **Founder ไม่ส่งงานให้ Scribe โดยตรง** — ต้องผ่าน Blue ก่อนเสมอ
- **Scribe รับเฉพาะ Decision Package** (มี ID/Title/Status/Date/Reason/Scope/Files/Acceptance Criteria) **ไม่รับ chat log ดิบ**
- **ทุก Agent ต้องอัปเดต HQ** หลังจบงานของตัวเอง (`hq/INBOX.md` เป็นอย่างน้อย)

> นี่คือ zoom-in เฉพาะขั้นตอนที่งานไหลเข้าสู่ Scribe — ไม่ได้แทนที่ Flow เต็มรูปด้านบน (Founder→Luther→Blue→HQ→Scout→Atlas→Scribe→GitHub→Automation) เพียงแต่เน้นย้ำว่าจุดที่ Scribe รับงานต้องผ่านการกลั่นกรองเป็น Decision Package เสมอ

## บทบาท

- **Luther** — **Product Thinking** ตัดสินใจเชิง Product/Strategy วิเคราะห์และ challenge ทิศทาง ก่อนส่งต่อผ่าน Blue
- **Blue** — **Project Coordination** (Chief of Staff) ดูแล Mission Tracking, Sprint Tracking, Task Assignment, Inbox Management, HQ Maintenance, Daily Brief, Weekly Review, Cross-Agent Coordination
  - Blue **ไม่มีสิทธิ์**เปลี่ยน Product Direction, สร้าง Belief, หรืออนุมัติ Decision — มีหน้าที่ **Coordinate เท่านั้น**
- **Scout** — **Collect Evidence** (เดิม "Collect Problems") เก็บข้อมูลพฤติกรรมจริงจากสนามและชุมชน โดยต้องขอ/สร้าง **Evidence ID** ทันทีที่บันทึกข้อมูล (ดู `research/EVIDENCE_LOG.md`) โดยเฉพาะข้อมูลที่ขัดกับสมมติฐานทีม (ดู `research/anti-assumptions.md`)
  - **การรัน Scout ฝั่ง Community:** ใช้ Claude Cowork เป็น agent — brief สำเร็จรูปอยู่ที่ `research/community/SCOUT_COWORK_BRIEF.md`
- **Atlas** — **Extract Patterns** (เดิม "Write Insight") ทุก Pattern/Insight ที่ Atlas เขียนต้องผูกกับ Evidence ID อย่างน้อย 1 รายการเสมอ ห้ามเขียน insight ลอยๆ โดยไม่มี evidence อ้างอิง
- **Scribe** — **Knowledge Management** (เดิม "Write Documents" → "Maintain Knowledge Graph") ไม่ใช่แค่จัดไฟล์ แต่ดูแลให้ Evidence → Belief → Decision เชื่อมโยงกันได้ตลอดทั้งระบบ รับเฉพาะ **Approved Decisions** เท่านั้น **ไม่รับ Chat Log ดิบ**

## DriverOS HQ Workflow

ทุก Agent **ก่อนเริ่มงาน** ต้องอ่าน:
- `hq/DASHBOARD.md` (ภาพรวมเร็วๆ)
- `hq/CURRENT_MISSION.md`
- `hq/CURRENT_STATE.md`
- `hq/NEXT_ACTIONS.md`

**หลังจบงาน** ต้องอัปเดต:
- `hq/INBOX.md`

รายละเอียดกฎการดูแล HQ ทั้งหมด ดู `hq/README.md`

## กติกาสำคัญ

Scribe จะไม่แปลงบทสนทนาดิบเป็นเอกสารโดยตรง — ทุกอย่างที่ถูกบันทึกต้องผ่านการกลั่นกรองจนกลายเป็น "การตัดสินใจที่ชัดเจน" (Decision) ก่อนเสมอ ซึ่งเป็นเหตุผลที่ `decisions/` มีโครงสร้างวันที่/เหตุผล/ผลกระทบ ไม่ใช่การ copy-paste บทสนทนา

## เชื่อมโยง

- `decisions/README.md` — บันทึกผลลัพธ์ของ workflow นี้
- `product/PROCESS_GATES.md` — Gate การอนุมัติระดับ Product Discovery (คนละชั้นกับ AI Workflow นี้ ซึ่งเป็นกระบวนการทำงานภายในทีม)
