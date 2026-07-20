# DriverOS — Documentation Standards

## การตั้งชื่อไฟล์

- ใช้ `kebab-case` สำหรับชื่อโฟลเดอร์: `gate-2-user-journey/`
- ใช้ `PascalCase_With_Underscore` สำหรับเอกสารที่มีเวอร์ชัน: `DriverOS_User_Journey_Map_v1.md`
- ไฟล์มาตรฐานระดับระบบใช้ตัวพิมพ์ใหญ่ทั้งหมด: `README.md`, `PROCESS_GATES.md`, `STANDARDS.md`

## Versioning เอกสาร

- ทุกเอกสาร Discovery ต้องมี `v1`, `v2` ต่อท้ายชื่อไฟล์เมื่อมีการแก้ไขใหญ่หลัง Gate ผ่านแล้ว
- ห้ามแก้ไฟล์เดิมทับหลังผ่าน Gate — ให้สร้างเวอร์ชันใหม่ + บันทึกเหตุผลใน ADR

## โครงสร้างเอกสารทุกฉบับต้องมี

1. Header: ชื่อเอกสาร, Gate, Status, วันที่, ผู้จัดทำ
2. เนื้อหาหลัก
3. ท้ายเอกสาร: สถานะการอนุมัติ (อ้างอิง `templates/gate-approval-template.md`)

## ภาษา

- เอกสารฝั่ง Product/Discovery: ภาษาไทยเป็นหลัก (สื่อสารกับ Founder โดยตรง)
- เอกสารฝั่ง Technical (README ของ mobile/, backend/ ฯลฯ): ภาษาอังกฤษ เพื่อรองรับทีม Engineering ในอนาคต

## Architecture Decision Records (ADR)

- ทุกการตัดสินใจเชิงสถาปัตยกรรมที่มีผลกระทบระยะยาว (เช่น "Notification-first interaction model") ต้องบันทึกเป็น ADR แยกจาก Journey Map
- ใช้ `templates/adr-template.md`

## การอ้างอิงข้าม Gate

- ห้ามให้เอกสาร Gate หลังอ้างอิงเนื้อหาที่ยังไม่ผ่าน Gate ก่อนหน้า
- ทุกเอกสารต้องลิงก์กลับไปยัง Gate ต้นทางที่ทำให้เกิดการตัดสินใจนั้น (traceability)
