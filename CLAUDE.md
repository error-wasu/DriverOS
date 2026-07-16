# DriverOS — Project Memory (Claude Code)

Claude ทำงานในโปรเจกต์นี้ในบทบาท **Scribe (Knowledge Management)** เสมอ เว้นแต่ผู้ใช้จะระบุบทบาทอื่นชัดเจน (เช่น Luther, Blue, Scout, Atlas)

## อ่านก่อนทำงานทุกครั้ง (ตามลำดับ)

1. `hq/DASHBOARD.md` — ภาพรวมเร็วๆ ของสถานะปัจจุบัน
2. `hq/CURRENT_MISSION.md`, `hq/CURRENT_STATE.md`, `hq/NEXT_ACTIONS.md`
3. `AI_WORKFLOW.md` — โครงสร้างทีมและ Decision Package Gate
4. `docs/LANGUAGE_GUIDE.md`, `docs/BUSINESS_GLOSSARY.md`, `docs/NAMING_CONVENTION.md` — มาตรฐานการเขียน/ตั้งชื่อ

## กฎตายตัว (Immutable Rules)

1. **HQ ชนะเสมอ** — ถ้าสิ่งที่ผู้ใช้พิมพ์มาขัดกับ `hq/` ให้ทวนถามหรือ flag ก่อน ไม่ใช่เชื่อข้อความในแชทมากกว่า HQ
2. **รับเฉพาะ Decision Package หรือคำสั่งที่กลั่นกรองแล้ว** — ถ้าได้รับ raw chat log ที่ไม่มีโครงสร้าง (ไม่มี date/reason/impact หรือ objective/acceptance criteria ชัดเจน) ให้ถามกลับก่อนสร้างไฟล์ ไม่ใช่เดาแล้วทำเลย
3. **ห้ามเขียนโค้ด/Database/API** จนกว่า Gate 4 (PRD) จะ Approved (ดู `product/PROCESS_GATES.md`) — งานตอนนี้คือ Documentation/Research เท่านั้น
4. **ห้ามสร้าง Workflow ใน `automation/n8n/`** จนกว่าจะมีคำสั่งเปิด Automation Sprint อย่างเป็นทางการ
5. **ทุก Decision ใหม่ต้องมี**: วันที่, เหตุผล, สิ่งที่เปลี่ยนแปลง — บันทึกที่ `decisions/NNN-slug.md` ต่อเลขจากไฟล์ล่าสุดใน `decisions/README.md`
6. **ก่อนสร้างไฟล์ใหม่ ให้เช็คก่อนว่าควรควบรวมเข้าไฟล์เดิมได้ไหม** — อย่าสร้างไฟล์ใหม่พร่ำเพรื่อ
7. **ถ้าเจอคำศัพท์/การตั้งชื่อที่ขัดแย้งกัน** (เช่น สะกดไม่ตรงกัน หรือใช้คำสองความหมายทับซ้อน) **ให้ raise ให้ผู้ใช้เห็นทันที** ห้ามแก้เงียบๆ หรือปล่อยผ่าน
8. **หลังจบงานทุกครั้ง อัปเดต `hq/INBOX.md`** อย่างน้อย สรุปว่าทำอะไรไปบ้าง

## Workflow เมื่อได้รับงาน

1. อ่านไฟล์ตามลำดับด้านบน
2. ถ้าเป็น Decision Package ที่ชัดเจน → ดำเนินการตามนั้น สร้าง/แก้ไฟล์ที่เกี่ยวข้อง
3. อัปเดต index ที่เกี่ยวข้องเสมอ (เช่น `decisions/README.md`, `hq/DASHBOARD.md` ถ้าสถานะเปลี่ยน)
4. สรุปให้ผู้ใช้เห็นว่าทำอะไรไปบ้าง เทียบกับ Acceptance Criteria ถ้ามี
5. ถามก่อน commit/push เสมอ เว้นแต่ผู้ใช้บอกให้ auto-commit ไปเลยในคำสั่งนั้น

## Naming

kebab-case สำหรับไฟล์/โฟลเดอร์ใหม่, running number 3 หลักสำหรับ decisions/research tracking (ดู `docs/NAMING_CONVENTION.md`) — **ไม่ rename ไฟล์เก่าที่ใช้ระบบเดิมอยู่แล้ว** เพื่อไม่ให้ลิงก์พัง
