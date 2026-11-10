# 🎓 เว็บติวสอบ Project Database — ครบทั้ง 2 Business Domain

เว็บสื่อการสอนเตรียมสอบ **Project Face-to-face** วิชา Database Systems (โจทย์: อ.ประพจน์/อ.อู๊ด + อ.วรางคณา/อ.ผึ้ง)
สมาชิกกลุ่มอ่านจบแล้ว **demo "DROP ทุกตารางแล้วสร้างใหม่" ได้เอง** ทั้ง Part I และ Part II — เขียนสำหรับคนที่ไม่มีพื้นฐาน SQL เลย

## หน้าเว็บ (10 หน้า)

| หน้า | เนื้อหา |
|---|---|
| `index.html` | โจทย์อาจารย์ verbatim · พื้นฐานสำหรับคนไม่มีพื้นฐาน SQL · ภาพรวม 2 Part · ลำดับรัน · บทบาท 4 คน · แผน 2 วัน · checklist (localStorage) · ⚠️ เตือนตารางงานอื่นใน User เดียวกัน |
| `p1-usecase.html` | Part I: Actor 4 + UC 9 ตัว (UC Spec ครบ) + Traceability US1–US10 |
| `p1-er-ddl-dml.html` | Part I: E/R 11 ตาราง + โค้ด 00/01/02 เต็ม + อธิบาย Constraint P/R/U/C + อ่าน CREATE/INSERT/SELECT ทีละบรรทัด |
| `p1-plsql.html` | Part I: โค้ด 03 เต็ม (Trigger 1 + Procedure 4) + แผนที่สถานะ 8 สถานะ + ไล่อ่าน SP_SUBMIT_DOC ทีละบรรทัด |
| `p1-join.html` | Part I: โค้ด 04 เต็ม Q1–Q6 + ห้องทดลอง JOIN จิ๋ว + ลำดับอ่าน SELECT 7 ขั้น + ผลที่จะเห็นจริง |
| `p2-usecase.html` | Part II: UC01–UC10 (เอกสาร Business Domain) + REQ 1–17 + Traceability REG1–17 + จับคู่ UC ↔ ตารางฉบับ implement จริง |
| `p2-er-ddl-dml.html` | Part II (Smart Bus Bell): E/R Chen 11 ตาราง + โค้ด oracle_1/oracle_2 เต็ม + กฎ junction/weak entity/derived + seed 27 แถว |
| `p2-plsql.html` | Part II: SP 4 ตัว เต็ม (SP_PRESS_BELL ฯลฯ) + RETURNING INTO/MERGE/SQL%ROWCOUNT + ข้อจำกัด Oracle 10g 3 ข้อ |
| `p2-join.html` | Part II: รายงาน 3 แบบ (JOIN 6 ตาราง · RANK analytic · WITH clause) + ผลที่จะเห็นจริง 2 สภาพ |
| `verify-demo.html` | ⚠️ เตือนตารางงานอื่น · ลำดับ demo (Part II ไฟล์ 1→5) · oracle_5 + วิธีอ่านผล · กรณี error ครบ · Q&A 2 Part + มือใหม่ · บทบาท 4 คน |

## ระบบที่ฝัง

- **styles.css** — ธีม responsive (มือถือ/เดสก์ท็อป) ต่อยอดจากเว็บติวสอบ-Final-DB
- **script.js** — เมนูมือถือ · progress bar · quiz (data-answer 0-based) · checklist localStorage `project-db-checklist-v1`
- **tts.js** — ปุ่ม 🔊 อ่านออกเสียง (Web Speech + เสียงไทยออนไลน์ SoundOfText) · Mermaid ESM CDN ในหน้าที่มีแผนภาพ

## วิธีเปิด

เปิด `index.html` ตรง ๆ ได้ (file://) หรือรัน local server:

```bash
cd "เว็บติวสอบ-Project-DB"
python3 -m http.server 8795
# http://localhost:8795
```

## Deploy (GitHub Pages — repo `db-project-prep`)

```bash
cd "เว็บติวสอบ-Project-DB"
git add -A
git -c user.name="NiabKungg" -c user.email="niabbiekunggit@gmail.com" commit -m "..."
git push
```
Live: ดู URL ใน PROJECT-TUTOR-KB.md (หัวข้อ 0) — .nojekyll รองรับแล้ว, .gitignore กัน .mimosa/

## ต้นฉบับโค้ดจริง

- Part I: `../S2G13-DB-PROJECT/` (00–05)
- Part II: `/home/niab/Desktop/การเรียน/final DB/SE/` (oracle_1–5 + README_Oracle_Exam.md + ER_Diagram_Chen.mmd) — deploy บน iSQL*Plus Oracle 10g แล้ว
