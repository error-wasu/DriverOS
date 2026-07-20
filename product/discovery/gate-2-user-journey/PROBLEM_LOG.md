# DriverOS — Problem Log

**Gate:** 2 — User Journey
**Source ข้อมูล:** Contextual Inquiry กับ Founder (ผู้ใช้จริง/คนขับ Grab)
**Status เอกสาร:** 🟡 Draft

> 🔄 **อัปเดต 2026-07-15:** เปลี่ยนสถานะ P-001–P-005 จาก "✅ Validated" เป็น "🟢 Emerging Evidence" ตาม `research/RESEARCH_PRINCIPLES.md` (Founder Observation != Market Truth) — ไม่ได้แปลว่าข้อมูลผิด แค่ยังไม่ถึงระดับที่เรียกว่า Validated จริงๆ เพราะ sample size ยังเป็น 1

---

| Problem ID | Title | Evidence | Source | Frequency | Severity | Confidence | Status |
|---|---|---|---|---|---|---|---|
| P-001 | ไม่รู้กำไรสุทธิหลังหักต้นทุน (fuel/ค่าเสื่อม) | "ไม่รู้กำไรสุทธิ (ยังไม่หักค่าน้ำมัน/ค่าเสื่อม)" — ระบุเป็นความหงุดหงิดอันดับ 1 ตอนเช็คระหว่างกะ | Founder self-report (E-000) | ทุกกะ | High | High | 🟢 Emerging Evidence |
| P-002 | อยากรู้กำไรสุทธิ แต่ขี้เกียจคำนวณเอง (effort barrier) | "อยากรู้แต่ขี้เกียจคำนวณเอง" — ตอบตรงเมื่อถามความรู้สึกท้ายกะ | Founder self-report (E-000) | ทุกกะ (ช่วงจบกะ) | High | High | 🟢 Emerging Evidence |
| P-003 | เวลาว่างระหว่างกะถูกใช้หา hotspot งาน ไม่ใช่เช็คการเงิน (attention conflict) | เลือก "ดูจุด/พื้นที่ที่มีงานเยอะ" เป็นพฤติกรรมหลักช่วงว่าง เหนือกว่า "เช็ครายได้" | Founder self-report (E-000) | หลายครั้งต่อกะ | High | High | 🟢 Emerging Evidence |
| P-004 | จังหวะเติมน้ำมันไม่มีรูปแบบตายตัว ทำนายไม่ได้ | "ไม่แน่นอน แล้วแต่สถานการณ์วันนั้น" | Founder self-report (E-000) | ไม่แน่นอน/กะ | Medium | High | 🟢 Emerging Evidence |
| P-005 | คนขับเช็ครายได้แบบ opportunistic (ทุก 2-3 ทริป) ไม่ใช่ทุกทริป | "2-3 ถ้ามีช่วงว่าง หรือไม่มีงานต่อจะเช็ค" | Founder self-report (E-000) | ทุก 2-3 ทริป (เฉพาะช่วงว่าง) | Medium | High | 🟢 Emerging Evidence — ทำให้ per-trip OCR ไม่ใช่ hero feature |
| P-006 | สมมติฐาน: คนขับเลือก "โหมดขับ" ตายตัวตอนเริ่มกะ | "ปรับเปลี่ยนไปเรื่อยๆ ระหว่างกะ" — ตรงข้ามกับสมมติฐานเดิม | Founder self-report (E-000) | ตลอดกะ (พฤติกรรมต่อเนื่อง) | — | High | ❌ Invalidated — ต้องออกแบบใหม่ |

---

## นิยามคอลัมน์ (สำหรับอ้างอิง)

- **Frequency** — ความถี่ที่ปัญหานี้เกิดขึ้นจริงในการใช้งาน
- **Severity** — ผลกระทบต่อผู้ใช้ถ้าไม่แก้ (High/Medium/Low) — ไม่ใช้กับรายการที่เป็น "สมมติฐานที่ถูก invalidate" เพราะไม่ใช่ปัญหาแต่เป็นข้อผิดพลาดในการออกแบบ
- **Confidence** — ความมั่นใจว่าข้อมูลนี้สะท้อนพฤติกรรมจริง (อิงจากจำนวน/ความชัดเจนของหลักฐาน ยังเป็น sample size = 1 คน ต้อง validate เพิ่มกับผู้ใช้คนอื่นก่อน Gate 4)
- **Status** — 🟢 Emerging Evidence (หลักฐานเบื้องต้น ยังไม่ถือเป็น Truth) / ✅ Validated (ผ่านการยืนยันกับกลุ่มตัวอย่างที่เพียงพอแล้ว) / ❌ Invalidated / 🔍 Needs More Research

## ข้อจำกัดของเอกสารนี้

⚠️ ข้อมูลทั้งหมดมาจาก **ผู้ใช้ 1 คน (Founder)** — Confidence "High" หมายถึงความชัดเจนของคำตอบ ไม่ใช่ความครอบคลุมของกลุ่มตัวอย่าง ก่อนเข้า Gate 4 ควร validate P-001 ถึง P-005 กับคนขับอย่างน้อย 3-5 คนเพิ่มเติม
