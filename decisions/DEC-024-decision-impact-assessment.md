# DEC-024 — Decision Impact Assessment & Decision Index

**สถานะ:** ✅ Approved
**วันที่:** 2026-07-17
**เกี่ยวข้องกับ:** `decisions/DEC-023-repository-precedence.md`

## Reason

Luther feedback ต่อ DEC-023: เห็นด้วย 80% กับวิธี sync ของ Scribe แต่ชี้ว่ายังพึ่งความจำของ AI ว่า "ควรแก้ไฟล์ไหนบ้าง" อยู่ — เมื่อ Decision เยอะขึ้นเรื่อยๆ ความเสี่ยงนี้จะสูงขึ้น จึงเสนอ 2 กลไกเสริม

## Decision

### 1. Decision Impact Assessment (บังคับใช้ทุก Decision ใหม่)

ก่อน sync Decision ใดๆ เข้าไฟล์อื่น ต้องเช็ค checklist ก่อนว่ากระทบไฟล์ไหนบ้าง (CLAUDE.md, hq/, README, Constitution, Research Principles, Agent Specs, Prompt ที่ใช้งานอยู่, Decision อื่น) พร้อมเหตุผลของแต่ละข้อ — ไม่ใช่เพื่อเพิ่มขั้นตอน แต่เพื่อไม่ให้พึ่งความจำ AI ล้วนๆ

Checklist เต็มอยู่ใน `decisions/TEMPLATE.md` — ใช้ template นี้กับ Decision ใหม่ทุกอันจากนี้ไป

### 2. Decision Index

สร้าง `decisions/DECISION_INDEX.md` — ตารางสรุป Status/Supersedes/Affected Files ของทุก Decision โดยไม่เก็บเนื้อหา ใช้เช็คเร็วว่า Decision ไหน Active/Superseded และกระทบไฟล์อะไร

**ต้องอัปเดต DECISION_INDEX.md ทุกครั้งที่มี Decision ใหม่หรือเปลี่ยนสถานะ** — ถือเป็นส่วนหนึ่งของ Impact Assessment (checklist มีข้อนี้อยู่แล้ว)

## Impact Assessment ของ DEC-024 เอง (ตัวอย่างการใช้งาน)

- [x] `CLAUDE.md` — ต้องเพิ่มกฎอ้างอิง Impact Assessment ในขั้นตอน sync
- [x] `decisions/README.md` — ต้องเพิ่มลิงก์ไปยัง `TEMPLATE.md` และ `DECISION_INDEX.md`
- [x] `decisions/DECISION_INDEX.md` — ไฟล์ใหม่ที่ DEC-024 นี้สร้างเอง (บันทึกตัวเองไว้ในตารางด้วย)
- [ ] `hq/` — ไม่กระทบโดยตรง (เป็นกฎเฉพาะของ `decisions/` folder)
- [ ] `AI_CONSTITUTION.md` — ไม่กระทบตอนนี้ (ยัง skeleton)

## สิ่งที่ "ไม่ทำ" ตามคำสั่ง Luther

**Repository Mutation** (ใครมีสิทธิ์แก้ไฟล์ประเภทไหน) — Luther สั่งชัดเจนว่า**ยังไม่สร้าง Decision ใหม่ตอนนี้** ให้พักไว้เป็น Backlog ก่อนจนกว่าจะเจอปัญหาจริงเรื่องสิทธิ์การแก้ไข — บันทึกไว้ที่ `hq/INBOX.md` (Luther section) แทน ไม่ใช่ที่นี่

## สิ่งที่เปลี่ยนแปลง (ไฟล์ที่แก้จริง)

- `decisions/TEMPLATE.md` — ไฟล์ใหม่
- `decisions/DECISION_INDEX.md` — ไฟล์ใหม่
- `decisions/README.md` — เพิ่มลิงก์ไปยังทั้งสองไฟล์ + กฎบังคับใช้ template กับ Decision ใหม่
- `CLAUDE.md` — เพิ่มขั้นตอน Impact Assessment ใน workflow
