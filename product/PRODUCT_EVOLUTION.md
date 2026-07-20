# DriverOS — Product Evolution

**สถานะ:** Draft
**Priority:** 🔴 Critical

เอกสารนี้บันทึกวิวัฒนาการของแนวคิด DriverOS ตามลำดับเวลา เพื่อให้ทีมเข้าใจว่าทำไม product ถึงเปลี่ยนขอบเขตมาเรื่อยๆ — ไม่ใช่ scope creep แต่คือความเข้าใจที่ลึกขึ้นทีละชั้น

## Version History

```
Phase 1 — Income Tracker
   ↓
Phase 2 — Expense Tracker
   ↓
Phase 3 — Net Profit Calculator
   ↓
Phase 4 — Business Intelligence Dashboard
   ↓
Phase 5 — Decision Support System
   ↓
Phase 6 (Current) — Confidence Support System
```

**Phase 6 — Confidence Support System:** ช่วยให้คนขับ "มั่นใจ" ว่าการตัดสินใจของตัวเองดีพอ ไม่ใช่แค่บอกตัวเลข แต่ช่วยลดความเคว้งคว้างในการตัดสินใจระหว่างกะ (ดู `research/founder/lost-state.md`)

## Core Job-to-be-Done — UPDATE

> ⚠️ **นี่คือการอัปเดตจากข้อสรุปเดิมใน Gate 2** (`discovery/gate-2-user-journey/DriverOS_User_Journey_Map_v1.md`) — เก็บฉบับเดิมไว้เพื่อ traceability ไม่ได้ลบทิ้ง

| | เดิม (Gate 2) | ใหม่ (ปัจจุบัน) |
|---|---|---|
| Job-to-be-Done | รู้กำไรสุทธิ | ช่วยให้คนขับตัดสินใจได้ดีขึ้นทุกวัน |
| สถานะของ Net Profit | เป้าหมายหลัก | เป็นเพียง **Metric** หนึ่งที่ป้อนเข้าสู่การตัดสินใจ ไม่ใช่ **Mission** |

**เหตุผลของการอัปเดต:** งานวิจัยกับ Founder เพิ่มเติม (`research/founder/001-last-night.md`, `research/founder/lost-state.md`) พบว่า pain ที่ลึกกว่าเรื่องกำไรคือ "Lost State" — คนขับไม่รู้จะไปไหน ไม่มั่นใจในการตัดสินใจ กำไรสุทธิเป็นแค่ข้อมูลชิ้นหนึ่งที่ช่วยตอบคำถามที่ใหญ่กว่านั้น

## ผลกระทบต่อเอกสารอื่น

- `product/PRODUCT_PHILOSOPHY.md` — เพิ่ม Decision Library สะท้อน JTBD ใหม่
- `product/HOME_EXPERIENCE.md` — ออกแบบ Home ใหม่ตาม JTBD นี้
- Gate 2 เดิมยังคง **Approved-pending-review** — ต้องพิจารณาว่าจะเปิด Change Request หรือไม่ ก่อนเข้า Gate 3 อย่างเป็นทางการ (ดู `product/PROCESS_GATES.md`)
