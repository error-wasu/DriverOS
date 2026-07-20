# Research Principles

**สถานะ:** Draft
**Priority:** 🔴 Critical
**เกี่ยวข้องกับ:** `decisions/019-behavior-discovery-reframe.md`

หลักการเหล่านี้ใช้กำกับงานวิจัยพฤติกรรมทั้งหมดของ DriverOS ตั้งแต่วันนี้เป็นต้นไป

1. **Observe before explaining** — บันทึกสิ่งที่เห็น/เกิดขึ้นก่อน ค่อยตีความทีหลัง อย่าข้ามไปตีความทันที
2. **Describe reality** — อธิบายสิ่งที่เกิดขึ้นจริงตามที่เป็น ไม่ใช่สิ่งที่ทีมคิดว่าน่าจะเกิดขึ้น
3. **Avoid confirmation bias** — ระวังการมองหาแต่ข้อมูลที่สนับสนุนสมมติฐานที่ทีมชอบอยู่แล้ว (ดู `research/anti-assumptions.md`)
4. **Founder Observation != Market Truth** — สิ่งที่ Founder เจอคือจุดเริ่มต้นที่มีค่า แต่ไม่ใช่ความจริงของตลาดทั้งหมด (sample size = 1)
5. **Evidence before Solution** — ห้ามออกแบบทางแก้ก่อนมีหลักฐานว่าปัญหา/พฤติกรรมนั้นมีอยู่จริง
6. **Routine > Opinion** — พฤติกรรมที่ทำซ้ำเป็นประจำ (routine) มีน้ำหนักมากกว่าความคิดเห็น/ความรู้สึกที่พูดออกมาตอนถูกถาม
7. **Single Source of Truth** — HQ ชนะเสมอ (HQ always wins) ถ้าบทสนทนาแชทกับสิ่งที่บันทึกใน `hq/` ขัดกัน ให้อัปเดต HQ ไม่ใช่ยึดบทสนทนาเป็นหลัก (ดู `hq/README.md`) — ลำดับชั้นเต็มของแหล่งข้อมูลทั้งหมด (ไม่ใช่แค่ HQ vs Chat) ดู **Repository Precedence** ที่ `decisions/DEC-023-repository-precedence.md`
8. **Evidence over Documentation** — ถ้า Evidence ไม่เพิ่ม แต่ Documentation เพิ่ม แปลว่าเริ่มเดินผิดทาง วัดความคืบหน้าจริงด้วยจำนวน Decision Cases/Community Evidence/บทสัมภาษณ์ที่เพิ่ม ไม่ใช่จำนวนไฟล์ .md (ดู `decisions/DEC-022-luther-review-2026-07-16.md`)

## ตัวอย่างการใช้หลักการที่ 3 และ 4 ร่วมกัน

> "Drivers optimize time more than distance"

ข้อความนี้ **ยังไม่ใช่ Truth** — เป็นแค่ **Emerging Evidence** จาก Founder Session เดียว ต้องเก็บข้อมูลเพิ่มก่อนจะขยับสถานะเป็น Validated (ดูนิยามสถานะที่ `product/discovery/gate-2-user-journey/PROBLEM_LOG.md`)
