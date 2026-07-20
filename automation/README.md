# Automation Layer

**สถานะ:** เตรียมโครงสร้างไว้ล่วงหน้า — **ยังไม่มี workflow จริง** (ตามคำสั่ง Luther: "ยังไม่ต้องมี Workflow")

## แนวคิด

Automation Layer จะเป็นชั้นที่เชื่อม HQ เข้ากับการทำงานอัตโนมัติในอนาคต ผ่าน:

- **n8n** — เครื่องมือ workflow automation (self-hosted) สำหรับเชื่อม GitHub, webhooks, และ AI agents เข้าด้วยกัน
- **Docker** — รัน n8n และบริการที่เกี่ยวข้องแบบ containerized
- **Blue** — ในอนาคต Blue อาจถูก implement บางส่วนผ่าน automation แทนการรันด้วยมือทุกครั้ง
- **Webhooks** — เชื่อมเหตุการณ์จาก GitHub (เช่น commit ใหม่) เข้ากับ workflow
- **GitHub** — จุดเชื่อมหลักระหว่าง repo กับ automation
- **Future MCP** — เผื่อเชื่อมต่อ MCP servers ในอนาคต

## โครงสร้าง

```
automation/
├── README.md          ← ไฟล์นี้
├── n8n/
│   ├── workflows/      ← ไฟล์ workflow .json (ยังไม่มี)
│   ├── templates/      ← workflow template ที่ reuse ได้
│   ├── credentials/    ← ⚠️ ห้าม commit credential จริง ดู credentials/README.md
│   └── backups/        ← backup ของ workflow
├── prompts/            ← prompt ที่ใช้ซ้ำสำหรับ automation
└── blue/               ← ไฟล์ที่เกี่ยวกับการ automate บทบาท Blue ในอนาคต
```

## กฎสำคัญ

- ห้าม commit credential/API key/token จริงลง repo นี้เด็ดขาด — ดู `n8n/credentials/README.md`
- ยังไม่ต้องสร้าง workflow จริงจนกว่า Luther/Blue จะสั่งเริ่ม Automation Sprint อย่างเป็นทางการ
