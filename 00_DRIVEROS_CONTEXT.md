# 00 — DriverOS Context

**สถานะ:** 🟡 Draft — บาง section รอ reconcile กับเอกสารที่ Approved อยู่แล้ว (ดูหมายเหตุ ⚠️ ด้านล่าง)
**ที่มา:** HANDOFF 001–003 (Blue, ในฐานะ Chief of Staff) — 2026-07-17

---

## ⚠️ หมายเหตุสำคัญก่อนอ่าน

Section "Background" ด้านล่างนี้ให้กรอบ DriverOS ที่**กว้างกว่า**สิ่งที่ Approved อยู่ใน `WHY_DRIVEROS_EXISTS.md` ปัจจุบัน (ซึ่งเน้นแอปคนขับ + Experience Transfer) ตอนนี้ยังไม่ได้ผ่านการ reconcile กันอย่างเป็นทางการ — และตาม `decisions/DEC-022-luther-review-2026-07-16.md` การเปลี่ยน Vision/Product Identity (รวมถึง CR-001) ต้องผ่าน **Decision Session แยกต่างหาก** เท่านั้น

**TODO (Founder):** จัด Decision Session เพื่อฟันธงว่า Background ด้านล่างนี้คือ Vision ใหม่ที่แทนที่ `WHY_DRIVEROS_EXISTS.md` หรือเป็นแค่กรอบความคิดเสริมที่ยังไม่ผ่านอนุมัติ — จนกว่าจะฟันธง ให้ถือว่า `WHY_DRIVEROS_EXISTS.md` เป็น Vision ทางการที่ใช้อ้างอิงได้

---

## Background

DriverOS ไม่ใช่แอปสำหรับคนขับ แต่เป็นบริษัทที่กำลังสร้าง AI Decision Intelligence Platform สำหรับศึกษาวิธีคิด การตัดสินใจ และพฤติกรรมของคนขับแพลตฟอร์ม (Grab, Bolt, LINE MAN และแพลตฟอร์มอื่นๆ)

โปรเจกต์นี้อยู่ในช่วง **Research Foundation** ยังไม่เข้าสู่การพัฒนาผลิตภัณฑ์

## Vision (ตาม HANDOFF 001 — รอ reconcile)

สร้างระบบที่เข้าใจการตัดสินใจของคนขับจากข้อมูลจริง และสามารถเปลี่ยนข้อมูลเหล่านั้นให้กลายเป็นองค์ความรู้ที่นำไปใช้ได้

## Mission

- ศึกษาพฤติกรรมของคนขับจากหลักฐานจริง
- สร้าง Knowledge Base เกี่ยวกับการตัดสินใจของคนขับ
- พัฒนา AI Team ที่ช่วยวิจัย วิเคราะห์ และจัดการความรู้
- พัฒนาผลิตภัณฑ์จาก Evidence ไม่ใช่จากสมมติฐาน

## DriverOS is NOT

- Dashboard
- Income Tracker
- OCR Project
- Grab Helper
- Automation Tool
- Feature Collection

ทั้งหมดข้างต้นอาจเป็นผลลัพธ์ในอนาคต แต่ไม่ใช่ตัวตนของ DriverOS

## Current Phase

**Research Foundation**

เป้าหมายของเฟสนี้:
- สร้าง Operating System
- สร้าง Knowledge Base
- สร้าง AI Workflow
- สร้าง Documentation

ยังไม่เน้น Feature Development (สอดคล้องกับ `product/PROCESS_GATES.md` และ Sprint 01 priorities ใน `hq/CURRENT_MISSION.md`)

---

## Core Principles (HANDOFF 002)

1. **Evidence Before Opinion** — ทุกข้อสรุปต้องมีหลักฐานรองรับ
2. **Describe Reality** — บันทึกสิ่งที่เกิดขึ้นจริงก่อนตีความ
3. **Decision Before Feature** — ศึกษา "การตัดสินใจ" ก่อนสร้าง Feature
4. **Research Before Product** — Research สำคัญกว่าการรีบสร้างแอป
5. **Pattern Before Solution** — หาความสัมพันธ์ก่อนเสนอทางแก้
6. **Human in the Loop** — Founder เป็นผู้ตัดสินใจขั้นสุดท้าย AI ไม่มีสิทธิ์กำหนด Vision

> หมายเหตุ: หลักการเหล่านี้สอดคล้องและเสริมกับ `research/RESEARCH_PRINCIPLES.md` ที่มีอยู่แล้ว — ไม่ได้ทดแทนกัน ทั้งสองไฟล์อ้างอิงกันได้

## Research Model (HANDOFF 003)

```
Observation
  ↓
Evidence
  ↓
Insight
  ↓
Pattern
  ↓
Decision Model
  ↓
Knowledge
  ↓
Feature (Future)
```

Feature จะเกิดหลังจาก Pattern มีความน่าเชื่อถือแล้วเท่านั้น — สอดคล้องกับ `research/decision-model.md`

**Session Goal ยังถือเป็น Research Variable** — ยังไม่ใช่ Product Feature ต้องเก็บข้อมูลเพิ่มก่อน

## เชื่อมโยง

- Vision ทางการปัจจุบัน (Approved): `/WHY_DRIVEROS_EXISTS.md`
- Change Request ที่รอ reconcile: `/CHANGE_REQUEST_001.md`
- Decision Model: `research/decision-model.md`
- Research Principles: `research/RESEARCH_PRINCIPLES.md`
