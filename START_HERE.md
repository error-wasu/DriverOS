# Start Here

ยินดีต้อนรับสู่ DriverOS — ไม่ว่าคุณจะเป็นมนุษย์หรือ AI Agent ที่เพิ่งเข้ามาทำงานในโปรเจกต์นี้ อ่านตามลำดับนี้ก่อนเริ่มทำอะไร:

1. **`00_DRIVEROS_CONTEXT.md`** — DriverOS คืออะไร, Vision, Mission, หลักการพื้นฐาน (⚠️ มีส่วนที่ยังรอ reconcile — ดูหมายเหตุในไฟล์)
2. **`hq/DASHBOARD.md`** — สถานะปัจจุบันของโปรเจกต์ ณ วันนี้
3. **`AI_WORKFLOW.md`** — โครงสร้างทีมและ workflow การส่งงาน
4. **`AGENTS.md`** — หน้าที่ของแต่ละ Agent (Founder, Blue, Scout, Atlas, Luther, Scribe)
5. **`docs/`** — มาตรฐานการเขียน/ตั้งชื่อ ก่อนสร้างหรือแก้ไฟล์ใดๆ
6. **`decisions/README.md`** — ประวัติการตัดสินใจทั้งหมด พร้อมเหตุผล

## ถ้าคุณคือ Claude Code

`CLAUDE.md` ที่ root จะถูกโหลดอัตโนมัติอยู่แล้ว ไม่ต้องอ่านไฟล์นี้ซ้ำ แต่ควรอ่านลำดับข้างบนตามที่ `CLAUDE.md` ระบุ

## กฎที่ต้องรู้ก่อนทำอะไรทั้งสิ้น

- **HQ Frozen v1** — ห้ามแก้โครงสร้าง `hq/` (ดู `hq/README.md`)
- **Scout v2 Mature/Frozen** — ห้ามแก้ prompt ใน `research/community/SCOUT_COWORK_BRIEF.md`
- **ห้ามเปลี่ยน Vision/Philosophy** โดยไม่ได้รับอนุมัติจาก Founder ผ่าน Decision Session แยก
- **Scribe รับเฉพาะ Decision Package** ที่กลั่นกรองแล้ว ไม่รับ chat log ดิบ (ดู `AI_WORKFLOW.md` หัวข้อ Decision Package Gate)
