# DriverOS HQ

> 🔒 **Status: Frozen v1** (Approved 2026-07-16, `decisions/DEC-022-luther-review-2026-07-16.md`)
> ห้ามแก้โครงสร้าง HQ (เพิ่ม/ลบไฟล์-โฟลเดอร์) อีก จนกว่าจะมีคำสั่งเปิด **HQ v1.1** อย่างเป็นทางการ
> แก้ได้เฉพาะ: **Bug, Missing Link, Documentation content** (อัปเดตเนื้อหาในไฟล์ที่มีอยู่แล้วทำได้ปกติ)

DriverOS HQ คือสำนักงานใหญ่ของโปรเจกต์ — **Single Source of Truth**

AI ทุกตัว (Luther, Blue, Scout, Atlas, Scribe และ Agent ใดๆ ที่เข้ามาทำงานในอนาคต) **ต้องอ่าน HQ ก่อนเริ่มงานทุกครั้ง**

**ห้ามใช้บทสนทนาแชทเป็น Source หลัก** — ทุกการตัดสินใจต้องอ้างอิงกลับมาที่ HQ เสมอ ถ้าบทสนทนากับสิ่งที่บันทึกใน HQ ขัดกัน **HQ ชนะเสมอ** (ดู Research Principle "Single Source of Truth" ใน `research/RESEARCH_PRINCIPLES.md`)

ลำดับชั้นความน่าเชื่อถือแบบเต็ม (เมื่อแหล่งข้อมูลอื่นๆ ขัดกันเองด้วย ไม่ใช่แค่กับ HQ) ดู **Repository Precedence** ที่ `decisions/DEC-023-repository-precedence.md`

## Mission

ทำให้ AI ตัวไหนก็ตาม (Claude, Gemini, OpenAI Codex, GitHub Copilot ฯลฯ) เข้ามาทำงานต่อในโปรเจกต์นี้ได้ทันทีโดยไม่ต้องเรียนรู้ตั้งแต่ศูนย์ — แค่อ่าน HQ ก็เข้าใจสถานะปัจจุบันทั้งหมด

## Workflow

```
Founder → Luther → Blue → HQ → Scout → Atlas → Scribe → GitHub → Automation (n8n)
```

ไม่มี Agent ตัวไหนคุยกันโดยตรง — ทุกคนผ่าน HQ ก่อนเสมอ (ดู `AI_WORKFLOW.md` หัวข้อ "DriverOS HQ Workflow")

## Roles

| Agent | หน้าที่ |
|---|---|
| Luther | Product Thinking |
| Blue | Project Coordination (Chief of Staff) |
| Scout | Collect Evidence |
| Atlas | Extract Patterns |
| Scribe | Knowledge Management |

รายละเอียดเต็มของแต่ละบทบาท ดู `AI_WORKFLOW.md`

## Update Rules

0. **เริ่มที่ `DASHBOARD.md` เสมอ** — เป็นหน้าแรกสรุปภาพรวมทั้งหมด ก่อนไปอ่านรายละเอียดในไฟล์อื่น
1. ก่อนเริ่มงานทุกครั้ง อ่าน `CURRENT_MISSION.md`, `CURRENT_STATE.md`, `NEXT_ACTIONS.md`
2. ระหว่างทำงาน บันทึกความคืบหน้า/ไอเดียชั่วคราวใน `INBOX.md`
3. หลังจบงาน อัปเดต `INBOX.md` ให้เป็นปัจจุบัน — **Blue เป็นคนย้ายของออกจาก INBOX** ไปยังที่ที่เหมาะสม (decisions/, research/, ฯลฯ)
4. Blue **ไม่มีสิทธิ์**เปลี่ยน Product Direction, สร้าง Belief, หรืออนุมัติ Decision — มีหน้าที่ Coordinate เท่านั้น

## Daily Flow

ทุกวันที่มีความคืบหน้า สร้างไฟล์ใหม่ใน `daily/` ชื่อ `YYYY-MM-DD.md` ตาม template (Mission / Summary / Evidence / New Decisions / Actions / Blockers / Tomorrow)

## Weekly Review

ทุกสัปดาห์ สรุปเป็นไฟล์ใหม่ใน `weekly/` ตาม template (Sprint Review / Progress / Beliefs / Evidence Coverage / Risk / Next Sprint)

ไฟล์ daily/weekly เก่าที่ไม่ active แล้ว ย้ายไป `archive/`

## Backlog (v1.1 — ยังไม่ implement)

Luther challenge ไว้ว่า HQ ตอนนี้เป็นแค่ **Documentation** (อ่านอย่างเดียว) ยังไม่ใช่ **Operational System** (อ่าน→Action→Update→Track) — v1.1 จะเพิ่ม **Execution Status** tracking แต่ยังไม่เริ่มตอนนี้ตามสถานะ Frozen v1 ด้านบน
