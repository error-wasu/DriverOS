# Decision Index

**สถานะ:** Draft
**หน้าที่:** ไม่เก็บเนื้อหา Decision — เก็บแค่สถานะ/ความสัมพันธ์/ไฟล์ที่กระทบ เพื่อให้ AI ทุกตัวเช็คได้เร็วว่า Decision ไหน Active, ถูกแทนที่ไปแล้ว, หรือกระทบไฟล์อะไรบ้าง โดยไม่ต้องเปิดอ่านทุกไฟล์

**อัปเดตทุกครั้งที่มี Decision ใหม่หรือ Decision เดิมเปลี่ยนสถานะ** (ตาม `decisions/TEMPLATE.md` หัวข้อ Impact Assessment)

| Decision | Status | Supersedes | Affected Files |
|---|---|---|---|
| [013](./013-home.md) | Active | - | `product/HOME_EXPERIENCE.md` |
| [014](./014-snapshot-flow.md) | Active | - | Gate 2 Journey (ต้น/ปลายกะ), Gate 3 Wireframe (ค้าง) |
| [015](./015-evidence-first.md) | Active | - | `product/EVIDENCE_FIRST.md` |
| [016](./016-gps-not-requirement.md) | Active | - | MVP scope (ลบ GPS requirement), `decisions/rejected/gps-always-on.md` |
| [017](./017-validate-human-behavior.md) | Active | - | Gate 2 process, `research/anti-assumptions.md` |
| [018](./018-daily-usage-vs-first-setup.md) | Active | - | Gate 3 Wireframe (ค้าง — ยังไม่เริ่ม) |
| [019](./019-behavior-discovery-reframe.md) | Active | - | `product/README.md`, `product/PROCESS_GATES.md`, `research/decision-model.md`, `research/RESEARCH_QUESTIONS.md`, `research/spatial-behavior.md`, `research/RESEARCH_PRINCIPLES.md`, `CURRENT_BELIEFS.md`, `PROBLEM_LOG.md` |
| [020](./020-experience-transfer.md) | Active | - | `WHY_DRIVEROS_EXISTS.md`, `product/PRODUCT_PHILOSOPHY.md` |
| [021](./021-driveros-hq-v1.md) | Active (Frozen v1) | - | `hq/`, `automation/`, `AI_WORKFLOW.md`, `research/RESEARCH_PRINCIPLES.md`, `CHANGELOG.md` |
| [DEC-022](./DEC-022-luther-review-2026-07-16.md) | Active | - | `docs/NAMING_CONVENTION.md`, `decisions/README.md`, `hq/CURRENT_MISSION.md`, `hq/DASHBOARD.md`, `hq/NEXT_ACTIONS.md`, `hq/README.md`, `research/community/SCOUT_COWORK_BRIEF.md`, `research/RESEARCH_PRINCIPLES.md`, `CURRENT_BELIEFS.md`, `SPRINT_LOG.md`, `CHANGE_REQUEST_001.md` |
| [DEC-023](./DEC-023-repository-precedence.md) | Active | - | `CLAUDE.md`, `hq/README.md`, `research/RESEARCH_PRINCIPLES.md`, `AI_CONSTITUTION.md` |
| [DEC-024](./DEC-024-decision-impact-assessment.md) | Active | - | `decisions/TEMPLATE.md` (new), `decisions/DECISION_INDEX.md` (new), `decisions/README.md`, `CLAUDE.md` |

*Decision #001–#012 ยังไม่ backfill (ดูหมายเหตุใน `decisions/README.md`) — ไม่อยู่ใน Index นี้จนกว่าจะ backfill*

## วิธีอ่านตาราง

- **Status:** `Active` (ยังมีผลอยู่) / `Superseded` (ถูกแทนที่แล้ว — ดูช่อง Supersedes ของ Decision ที่แทนที่) / `Rejected`
- **Supersedes:** ถ้า Decision นี้แทนที่ Decision เก่า ใส่เลขไว้ (เช่น `DEC-025 supersedes DEC-019`)
- **Affected Files:** ไฟล์/โฟลเดอร์ที่ Decision นี้แก้ไขจริง (ไม่ใช่แค่พูดถึง)
