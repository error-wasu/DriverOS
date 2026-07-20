# Credentials

⚠️ **ห้าม commit credential, API key, token, หรือ password จริงลงโฟลเดอร์นี้หรือที่ไหนใน repo นี้เด็ดขาด**

โฟลเดอร์นี้มีไว้เป็นที่เก็บ **คำอธิบาย/รายชื่อ credential ที่ต้องใช้** เท่านั้น (เช่น "ต้องมี GitHub Personal Access Token", "ต้องมี n8n API key") ตัว credential จริงให้เก็บใน n8n's built-in credential store หรือ password manager ของทีม ไม่ใช่ในไฟล์ text ที่ commit ขึ้น GitHub

หากพบว่ามี credential จริงหลุดเข้ามาใน repo (แม้แต่ใน commit history เก่า) ให้ revoke/หมุน credential นั้นทันทีและแจ้ง Luther
