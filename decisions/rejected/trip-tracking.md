# Rejected — Trip-level OCR/Screenshot Tracking (เป็น Hero Feature)

**วันที่:** 2026-07-15
**เกี่ยวข้องกับ:** `product/discovery/gate-2-user-journey/PROBLEM_LOG.md` (P-005)

## สิ่งที่ถูกปฏิเสธ

การให้คนขับ screenshot/บันทึกรายได้ทุกทริปที่จบ เป็นจุดปฏิสัมพันธ์หลักของแอป (ตามบรีฟแรกสุด — Import Trip Screen)

## เหตุผล

- **High Friction** — พฤติกรรมจริงคือคนขับเช็ครายได้แบบ opportunistic (ทุก 2-3 ทริป เฉพาะตอนมีช่วงว่าง) ไม่ใช่ทุกทริป การบังคับ workflow ทีละทริปจึงสวนทางกับพฤติกรรมจริง
- ยอด gross รายได้คนขับรู้จากแอปขับขี่ (Grab) อยู่แล้ว — ไม่ใช่ปัญหาที่ต้องแก้เป็นอันดับแรก
- แข่งความสนใจกับการหางานในช่วงเวลาว่าง (ดู `product/discovery/gate-2-user-journey/DriverOS_User_Journey_Map_v1.md`)

## ทางเลือกที่ใช้แทน

เก็บ trip-level data ไว้เป็น **infrastructure เบื้องหลัง** สำหรับ driving intelligence ในอนาคต ไม่ใช่ UI หลักที่คนขับต้องโต้ตอบด้วยทุกทริป (ดู `product/EVIDENCE_FIRST.md`)

## เงื่อนไขที่อาจกลับมาพิจารณาใหม่

หากในอนาคตมีวิธีเก็บข้อมูลทีละทริปแบบ zero-effort จริงๆ (เช่น อ่านจาก notification ของแอปขับขี่แบบอัตโนมัติ) อาจนำ trip-level capture กลับมาพิจารณาใหม่ในฐานะ background feature — แต่ยังคงไม่ใช่ hero UI
