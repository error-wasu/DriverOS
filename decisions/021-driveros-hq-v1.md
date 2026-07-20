# Decision #021 — DriverOS HQ v1

**Decision Package ID:** HQ-001
**วันที่:** 2026-07-16
**สถานะ:** ✅ Approved (2026-07-16)
**Priority:** 🔴 P0 (Critical Infrastructure)
**หมวด:** Infrastructure only — No Product Decision (ตาม Notes ใน HQ-001)

## บริบท

จำนวนเอกสาร Decision, Research, และ Product ในโปรเจกต์เพิ่มขึ้นเร็วมาก จนต้องพึ่ง Founder เป็นคนกลางเดินเอกสารระหว่าง Agent ต่างๆ (Luther, Scout, Atlas, Scribe) ด้วยตัวเอง — ไม่มี Single Source of Truth ที่ทุก Agent อ่านตรงกัน

## การตัดสินใจ

สร้าง **DriverOS HQ** (`hq/`) เป็นศูนย์กลางที่ทุก Agent ต้องอ่านก่อนเริ่มงานและอัปเดตหลังจบงาน พร้อมเพิ่มบทบาทใหม่ **Blue (Chief of Staff)** ทำหน้าที่ดูแล HQ และประสานงานข้าม Agent — Blue ไม่มีสิทธิ์ตัดสินใจเชิง Product

เตรียมโครงสร้าง **`automation/`** ไว้ล่วงหน้าสำหรับการเชื่อมต่อ n8n ในอนาคต แต่ยังไม่สร้าง workflow จริง

## เหตุผล

- ลดภาระ Founder จากการเป็นคนกลางเดินเอกสารเอง
- ทำให้ AI ตัวใหม่ (ไม่ว่าจะเป็น Claude, Gemini, Codex, Copilot) เข้ามาทำงานต่อได้ทันทีโดยอ่าน HQ อย่างเดียว — DriverOS จะไม่ผูกติดกับ AI ตัวใดตัวหนึ่ง
- แยกบทบาท "ตัดสินใจ" (Luther) ออกจาก "ประสานงาน" (Blue) อย่างชัดเจน ป้องกันไม่ให้ Coordinator กลายเป็นผู้ตัดสินใจโดยไม่ตั้งใจ

## สิ่งที่เปลี่ยนแปลง

- โครงสร้างใหม่: `hq/`, `automation/`
- `AI_WORKFLOW.md` — เพิ่ม Flow ใหม่ทั้งหมด + บทบาท Blue + หัวข้อ "DriverOS HQ Workflow"
- `research/RESEARCH_PRINCIPLES.md` — เพิ่มหลักการ Single Source of Truth
- `CHANGELOG.md` (ไฟล์ใหม่) — เริ่มบันทึกการเปลี่ยนแปลงระดับ infrastructure

## Acceptance Criteria

- [x] HQ Folder Created
- [x] Automation Folder Created
- [x] AI Workflow Updated
- [x] Research Principles Updated
- [x] Blue Role Added
- [x] Cross References Valid
- [x] README Updated
