---
สถานะ: Draft
Priority: 🔴 Critical
เกี่ยวข้องกับ: `research/community/SCOUT_COWORK_BRIEF.md`, `research/EVIDENCE_LOG.md`
---

# Research — How to Access Communities

เอกสารนี้ไม่ใช่ Evidence — เป็นบันทึกผลการทดสอบว่า Scout Agent (รันผ่าน Cowork) "เข้าถึง" คอมมูนิตี้แต่ละแพลตฟอร์มได้จริงแค่ไหนด้วยเครื่องมือที่มีอยู่ตอนนี้ วัตถุประสงค์คือให้ Scout รอบต่อไปเริ่มจาก **"หาทางเข้า" ก่อน "หาโพสต์"** — ถ้าเข้าไม่ได้ ไปหาโพสต์ก็เสียเวลาเปล่า

ทดสอบเมื่อ 2026-07-16 ด้วยเครื่องมือ `WebSearch` และ `web_fetch` (ไม่มี browser/login ใดๆ)

## สรุปผลการทดสอบ

| ช่องทาง | ต้อง Login ไหม | ผลทดสอบรอบนี้ (WebSearch/web_fetch) | ทางเข้าที่ใช้ได้จริง |
|---|---|---|---|
| Pantip | ไม่ต้อง (อ่านได้แบบ public) | เข้าได้บางส่วน — สุ่มโดนบล็อกเป็นระยะ (`2g.pantip.com/cafe/pleasecontact.php`) ดูเหมือน rate-limit/anti-bot มากกว่า login wall | `web_fetch` ใช้ได้แต่ไม่เสถียร ควรเว้นจังหวะระหว่างคำขอ หรือใช้ Chrome จริงถ้าต้องการอ่านทุกกระทู้ |
| Facebook Groups (public) | ต้อง login เพื่อเห็นเนื้อหาจริง | `web_fetch` คืนหน้าเปล่า (JS-rendered + login wall) ทุกกรณีที่ลอง — **แต่ Claude in Chrome + Chrome Profile ที่ล็อกอินอยู่แล้ว ทดสอบจริงแล้วเมื่อ 2026-07-16 ใช้งานได้** เปิด 3 กลุ่ม (Grab, LINE MAN, Bolt) อ่านโพสต์/คอมเมนต์ได้ปกติผ่าน `navigate` + `get_page_text` + scroll ดูผลใน `research/community/sessions/2026-07-16-scout-session.md` | ใช้ **Claude in Chrome** ผูกกับ Chrome Profile ที่ล็อกอิน Facebook ของผู้ใช้จริง — validated แล้ว ไม่ใช่แค่สมมติฐาน |
| Reddit | ไม่ต้อง (ปกติอ่าน public ได้) | `web_fetch` ปฏิเสธทันที — โดนบล็อกจาก allowlist ของ sandbox (`URL is on blocklist`) ไม่ใช่ปัญหาจาก Reddit | ต้องใช้ Claude in Chrome เพื่อเลี่ยงข้อจำกัดของ sandbox fetch (โดเมนนี้ไม่อยู่ใน allowlist) |
| YouTube (วิดีโอ/คอมเมนต์) | ไม่ต้อง | หน้าค้นหา/วิดีโอโหลดมาเป็นเปลือกเปล่า ไม่มีเนื้อหา (client-rendered) | ต้องใช้ Claude in Chrome เพื่อ render JS แล้วอ่านคอมเมนต์จริง |
| TikTok | ไม่ต้อง (ดูวิดีโอ/คอมเมนต์ public ได้ปกติ) | `web_fetch` ปฏิเสธทันที — โดนบล็อกจาก allowlist ของ sandbox (`URL not in allowed provenance set`) | ต้องใช้ Claude in Chrome เช่นกัน |
| Discord | ต้อง (invite link + account) | ยังไม่ได้ทดสอบ — คาดว่าเข้าไม่ได้เลยด้วยเครื่องมือปัจจุบัน | ต้องมี invite link ของ server คนขับที่เกี่ยวข้องก่อน แล้วใช้ Discord ผ่าน Chrome (เว็บ) หรือแอป desktop ผ่าน computer-use — ทั้งสองทางต้องมี **account จริงที่เข้าร่วม server แล้ว** |
| LINE OpenChat | ต้อง (LINE account + เข้าร่วม OpenChat) | ยังไม่ได้ทดสอบ — ไม่มีเวอร์ชันเว็บสาธารณะที่เข้าถึงเนื้อหาข้อความได้โดยไม่ล็อกอิน | ต้องใช้ **computer-use** เปิดแอป LINE บนเครื่อง (มือถือ/เดสก์ท็อป) ด้วย account ที่เข้าร่วม OpenChat ของคนขับแล้ว — เป็นช่องทางที่ automate ยากที่สุดในลิสต์นี้ |

## ทางเข้าที่มีจริง (เรียงจากง่ายไปยาก)

1. **Pantip ผ่าน web_fetch/WebSearch** — ใช้ได้เลยตอนนี้ ไม่ต้องเตรียมอะไรเพิ่ม แค่ระวังเรื่อง rate limit (เจอ 403-style block เป็นระยะแม้ไม่ได้เปลี่ยน URL pattern)
2. **Facebook ผ่าน Claude in Chrome** — validated แล้ว (2026-07-16) ใช้ Chrome Profile ที่ล็อกอินอยู่แล้วของผู้ใช้ นำทาง (`navigate`) ไปที่ URL กลุ่มโดยตรง แล้ว `get_page_text` + scroll (`computer` action) เพื่ออ่านโพสต์/คอมเมนต์ ทำงานได้ปกติ ข้อควรระวัง: หน้า get_page_text ปนชื่อโปรไฟล์ผู้โพสต์มาด้วยเสมอ — ต้องกรองออกเองก่อนบันทึกเป็น Raw Note (ห้ามให้ชื่อ/โปรไฟล์หลุดไปอยู่ในไฟล์ที่ commit) โพสต์บางอันถูกตัดด้วย "See more" ซึ่งต้องคลิกเพื่ออ่านต่อ (ยังไม่ได้ลองในรอบนี้เพราะอยู่ใน Ask-before-acting mode)
3. **Reddit / YouTube / TikTok ผ่าน Claude in Chrome** — ยังไม่ได้ทดสอบจริง แต่กลไกน่าจะเหมือน Facebook (ใช้ `navigate` + `get_page_text` ได้เลย ไม่ต้องมี Chrome Profile ล็อกอินสำหรับ Reddit/YouTube/TikTok เพราะเนื้อหาเป้าหมายเป็น public)
4. **Discord ผ่าน Chrome หรือ computer-use** — ต้องมี invite link ของ server ที่เกี่ยวข้องก่อนเป็นอันดับแรก (ยังไม่รู้ว่ามี Discord server คนขับไทยที่เปิดสาธารณะหรือไม่)
5. **LINE OpenChat ผ่าน computer-use** — ยากสุด ต้องมีเครื่องที่ล็อกอิน LINE ไว้แล้วและเข้าร่วม OpenChat กลุ่มเป้าหมายไว้ก่อน ไม่มีทาง automate จากศูนย์

## ข้อจำกัดเชิงนโยบาย (สำคัญ ต้องอ่านก่อนรอบหน้า)

การใช้ Chrome Profile ส่วนตัวของผู้ใช้ (login Facebook/LINE/Discord ของ Wasu เอง) เพื่อสอดส่องคอมมูนิตี้ **ไม่เหมือนกับ** การอ่านกระทู้สาธารณะแบบไม่ระบุตัวตนที่ Scout v2.0 ตั้งใจไว้แต่แรก — เมื่อ Scout ล็อกอินด้วยบัญชีจริง จะทิ้ง trace ว่าใครเข้าไปดู group/OpenChat ไหนบ้าง และอาจขัดกับกฎข้อ 4 ของ Scout Brief ("ห้ามเก็บข้อมูลที่ระบุตัวตนบุคคล") ถ้า Scout เผลอบันทึก username/โปรไฟล์ของสมาชิกกลุ่มที่เห็นระหว่างเข้าไปอ่านมาด้วย ควรตัดสินใจล่วงหน้าว่า:
- ใช้ account เปล่า (ไม่ผูกกับตัวตนจริง) สำหรับงานนี้โดยเฉพาะ หรือ
- ยอมรับความเสี่ยงว่า Wasu ต้องใช้ account ตัวเองล็อกอินให้ Scout ใช้งาน

เรื่องนี้เป็น Blind Spot ระดับนโยบาย ไม่ใช่แค่เทคนิค — ควรให้ Luther ตัดสินใจก่อนรัน Scout รอบที่ใช้ login จริง

## Blind Spot

**อัปเดต 2026-07-16:** Facebook ผ่าน Claude in Chrome ทดสอบแล้วว่าใช้งานได้จริง (ดู session log) — ไม่ใช่ Blind Spot อีกต่อไป ส่วน Reddit/YouTube/TikTok ผ่าน Claude in Chrome ยังไม่ได้ทดสอบจริง (คาดว่าน่าจะได้ผลคล้ายกันแต่ยังเป็นสมมติฐาน) ยังไม่รู้ว่า Facebook Groups ที่ปิด (private) หรือกลุ่มที่ยังไม่ได้เข้าร่วม (join) จะเข้าถึงเนื้อหาได้แค่ไหน — รอบนี้ทดสอบเฉพาะกลุ่มที่ผู้ใช้ join ไว้แล้วเท่านั้น ยังไม่รู้ว่ามี Discord server หรือ LINE OpenChat ของคนขับไทยที่เปิดสาธารณะอยู่จริงหรือไม่ — ยังไม่ได้ค้นหาเลย และยังไม่รู้ว่าการคลิก "See more" เพื่ออ่านโพสต์ที่ถูกตัดจะติด rate-limit หรือทำให้ Facebook สงสัยว่าเป็น bot หรือไม่ (ยังไม่ได้ลอง)
