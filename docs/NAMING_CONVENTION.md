# DriverOS Naming Convention

**สถานะ:** Draft
**Priority:** 🔴 Critical

- **Folder Names:** ใช้ระบบ `kebab-case` ทั้งหมด (เช่น `decision-cases/`, `field-notes/`)
- **File Names:** ใช้ระบบ `kebab-case` ภาษาอังกฤษแบบสั้น กระชับ ตัดคำฟุ่มเฟือยออก (เช่น `take-low-fare.md`, `go-home-early.md`)
- **Database Structure:** ใช้ระบบ `snake_case` สำหรับการตั้งชื่อ Table และ Column (เช่น `gross_income`, `idle_time_seconds`)
- **Code Classes:** ใช้ระบบ `PascalCase` สำหรับโครงสร้าง Data Model หรือ Components (เช่น `DriverSession`, `NetProfitCalculator`)
- **Research Tracking:** ให้รันนิ่งตัวเลขสามหลัก (เช่น `research-question-001.md`, `decision-case-001.md`)

## Cross-Reference ID Scheme (Approved 2026-07-16)

ใช้ระบบ **Prefix + running number** สำหรับอ้างอิงข้ามเอกสาร แทนเลขเปล่าๆ:

| Prefix | ใช้กับ | ตัวอย่าง |
|---|---|---|
| `HQ-` | Decision Package ระดับ Infrastructure/HQ | `HQ-001` |
| `PRD-` | Product Requirement Document (Gate 4) | `PRD-001` |
| `RQ-` | Research Question | `RQ-005` |
| `DQ-` | Decision Question | `DQ-005` |
| `BELIEF-` | รายการใน `CURRENT_BELIEFS.md` | `BELIEF-001` |
| `DEC-` | Decision ใน `decisions/` | `DEC-022` |
| `E-` | Evidence ใน `research/EVIDENCE_LOG.md` (ใช้อยู่แล้ว ไม่เปลี่ยน) | `E-003` |

**Transition rule:** ไฟล์ `decisions/013-*.md` ถึง `decisions/021-*.md` (เลขเปล่าไม่มี prefix) **ไม่ rename ย้อนหลัง** — ยังอ้างอิงด้วยเลขเดิมได้ตามปกติ ตั้งแต่ Decision ถัดไปเป็นต้นไปให้ใช้ `DEC-022`, `DEC-023`, ... ต่อจากเลขเดิม (ไม่รีเซ็ตกลับเป็น `DEC-001`) เพื่อรักษาความต่อเนื่อง

## หมายเหตุการเปลี่ยนผ่าน (Transition Note)

ไฟล์ที่มีอยู่แล้วในระบบก่อนมาตรฐานนี้ถูกล็อก (เช่น `PascalCase_With_Underscore` ใน `product/discovery/gate-2-user-journey/DriverOS_User_Journey_Map_v1.md`, หรือรูปแบบ `NNN-slug.md` ที่ใช้ในโฟลเดอร์ `decisions/` และ `research/founder/`) **ไม่ต้อง rename ย้อนหลังทันที** เพื่อไม่ให้ลิงก์ที่มีอยู่พัง — ให้เริ่มใช้มาตรฐานนี้กับไฟล์/โฟลเดอร์ใหม่ทั้งหมดตั้งแต่วันนี้เป็นต้นไป

Scribe มีหน้าที่ตรวจพบและ raise issue หากพบการตั้งชื่อที่ขัดแย้งกันเองในไฟล์ใหม่ (เช่น ใช้ทั้ง `kebab-case` และ `snake_case` ปนกันในโฟลเดอร์เดียว) — ห้ามปล่อยผ่านเงียบๆ

## เชื่อมโยง

- กฎการเขียน/คำศัพท์ → `docs/LANGUAGE_GUIDE.md`
- นิยามศัพท์เชิงระบบ → `docs/BUSINESS_GLOSSARY.md`
