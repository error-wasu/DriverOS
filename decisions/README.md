# DriverOS — Decision Log

**สถานะ:** Draft
**Priority:** 🔴 Critical

> หมายเหตุถึง Blue: นี่คือ Decision Log/ADR mechanism ที่เสนอไว้ท้าย HANDOFF ("ทุกครั้งที่ Founder ตัดสินใจเรื่องสำคัญ ควรมีไฟล์บันทึก") — **มีอยู่แล้วตั้งแต่ Decision #013** ไม่ต้องสร้างระบบใหม่ซ้ำ ใช้โฟลเดอร์นี้ต่อไปได้เลย

ทุก Decision ในโฟลเดอร์นี้ต้องมี **วันที่**, **เหตุผล**, และ **สิ่งที่เปลี่ยนแปลง** เพื่อให้ทีมย้อนกลับมาดูได้ว่า "ทำไม" เราถึงเลือกเดินเส้นทางนี้ ไม่ใช่แค่ "เดินไปทางไหน"

> ตาม `AI_WORKFLOW.md` — Scribe รับบันทึกเฉพาะ **Approved Decisions** เท่านั้น ไม่รับ Chat Log ดิบ

## Index

| # | ชื่อ | สรุป |
|---|---|---|
| 013 | [Home](./013-home.md) | Home = Prepare for Work ไม่ใช่ Dashboard |
| 014 | [Snapshot Flow](./014-snapshot-flow.md) | Daily flow แบบถ่ายรูปเลขไมล์ต้น-ปลายกะ |
| 015 | [Evidence First](./015-evidence-first.md) | ผูกกับ Evidence ไม่ผูกกับเทคโนโลยี |
| 016 | [GPS ไม่ใช่ Requirement](./016-gps-not-requirement.md) | ตัด GPS tracking ตลอดเวลาออกจาก MVP |
| 017 | [Validate Human Behavior](./017-validate-human-behavior.md) | ทุก feature ต้อง validate พฤติกรรมก่อนสร้าง |
| 018 | [Daily Usage vs First Setup](./018-daily-usage-vs-first-setup.md) | แยกออกแบบระหว่างการใช้งานรายวันกับการตั้งค่าครั้งแรก |
| 019 | [Behavior Discovery Reframe](./019-behavior-discovery-reframe.md) | เปลี่ยนกรอบจาก Product Discovery เป็น Behavior Discovery |
| 020 | [Experience Transfer](./020-experience-transfer.md) | DriverOS คือ Experience Transfer ไม่ใช่ Heatmap |
| 021 | [DriverOS HQ v1](./021-driveros-hq-v1.md) | ✅ Approved (HQ-001) — สร้าง HQ เป็น Single Source of Truth + บทบาท Blue |
| DEC-022 | [Luther Review 2026-07-16](./DEC-022-luther-review-2026-07-16.md) | ✅ Approved — Freeze HQ v1, Scout v2 Mature, ID Scheme, Sprint 01 re-priority |
| DEC-023 | [Repository Precedence](./DEC-023-repository-precedence.md) | ✅ Approved — ลำดับชั้นความน่าเชื่อถือของข้อมูล HQ>Decisions>Repo>Handoff>Chat |
| DEC-024 | [Decision Impact Assessment](./DEC-024-decision-impact-assessment.md) | ✅ Approved — บังคับใช้ Impact Assessment + สร้าง Decision Index |

## เอกสารสำคัญของโฟลเดอร์นี้

- **`TEMPLATE.md`** — ใช้ template นี้กับ Decision ใหม่ทุกอันจากนี้ไป (มี Impact Assessment checklist บังคับ)
- **`DECISION_INDEX.md`** — ตารางสรุป Status/Supersedes/Affected Files ของทุก Decision — **ต้องอัปเดตทุกครั้งที่มี Decision ใหม่**

*หมายเหตุ: Decision #001–#012 เป็นการตัดสินใจช่วงก่อนเริ่มบันทึกอย่างเป็นทางการ ยังไม่ได้ backfill เข้าระบบนี้*

## ✅ ID Scheme — Resolved (2026-07-16)

Luther อนุมัติให้ใช้ระบบ **Prefix + running number** (`HQ-`, `PRD-`, `RQ-`, `DQ-`, `BELIEF-`, `DEC-`) เป็นมาตรฐานถาวรตั้งแต่นี้ไป รายละเอียดเต็มอยู่ที่ `docs/NAMING_CONVENTION.md` หัวข้อ "Cross-Reference ID Scheme"

ไฟล์เดิม `013`–`021` **ไม่ rename** — Decision ถัดไปใช้ `DEC-022` ต่อเนื่องจากเลขเดิม

## Rejected Decisions

สิ่งที่ทีมตั้งใจ **ไม่ทำ** พร้อมเหตุผล ดูที่ `rejected/`

## Change Requests

การเปลี่ยนแปลงเชิง scope ที่กระทบเอกสารหลายฉบับ (เช่น การเปลี่ยน JTBD) ไม่ถูกบันทึกเป็น Decision เดี่ยว แต่ใช้ Change Request แทน ดู `/CHANGE_REQUEST_001.md`
