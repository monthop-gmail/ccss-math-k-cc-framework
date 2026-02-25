# คู่มือผู้ใช้ (CCSS Math K.CC Framework)

เอกสารนี้อธิบายวิธีใช้ repo นี้เพื่อผลิตสินค้าใบงาน (printable) สำหรับขายบน Teachers Pay Teachers (TPT) แบบทำซ้ำเร็วและคุมคุณภาพได้

## Repo นี้มีไว้ทำอะไร

- แปลงมาตรฐาน `CCSS Math – Kindergarten: Counting & Cardinality (K.CC)` ให้กลายเป็น “product line” ที่แตกเป็นแพ็กขายได้
- ให้โครงไฟล์/แม่แบบ (templates) และตัวอย่างแพ็ก (examples) ที่ copy ไปต่อได้ทันที

## โครงสร้างโปรเจกต์

- `docs/` คู่มือและกติกากลาง
- `docs/standards/` blueprint รายมาตรฐาน (เลือกอันที่จะทำ)
- `templates/` แม่แบบสำหรับทำซ้ำ (listing, pack spec, credits, checklist)
- `templates/product-pack/` โครงโฟลเดอร์ 1 product (copy แล้วเริ่ม)
- `examples/` ตัวอย่างแพ็ก (ยังไม่ใช่งานกราฟิกจริง)
- `references/` แหล่งอ้างอิง/แชทต้นทาง

หมายเหตุ: ไฟล์ export (PDF) และไฟล์งานกราฟิกใหญ่ ๆ ถูก ignore ด้วย `/.gitignore` เพื่อกัน repo บวม

## วิธีเริ่มทำ “1 product” (แนะนำทำตามนี้ทุกครั้ง)

### Step 1: เลือกมาตรฐาน (Standard)

1) เปิด `docs/standards/README.md`
2) เลือกไฟล์ blueprint ที่จะทำ เช่น `docs/standards/K.CC.B.5.md` หรือ `docs/standards/K.CC.C.7.md`

### Step 2: เลือกสเปกของแพ็ก

ใช้สเปกเริ่มต้นจาก `docs/pack-spec.md` แล้วกำหนดให้ชัด 4 อย่างนี้:

- Standard (เช่น `K.CC.C.7`)
- Skill keyword (สั้น ๆ สำหรับชื่อสินค้า)
- Range (เช่น `1-10` หรือ `0-20`)
- Theme (ถ้ามี เช่น Animals/Space/Farm)

### Step 3: สร้างโฟลเดอร์แพ็กใหม่จาก skeleton

1) Copy โครงจาก `templates/product-pack/`
2) วางไว้ใต้ `examples/` แล้วตั้งชื่อโฟลเดอร์ตาม convention

ตัวอย่างชื่อโฟลเดอร์:

- `examples/k-cc-b5-how-many-0-10-animals/`
- `examples/k-cc-c7-compare-1-10/`

ภายในแพ็กจะมี:

- `src/CONTENT.md` สคริปต์เนื้อหา (หน้าไหนทำอะไร)
- `listing/listing.md` ข้อความหน้าขาย (title/description/keywords)
- `export/` ที่เก็บ PDF export (ไม่ commit)
- `thumbnails/` ที่เก็บภาพหน้าปก/พรีวิว (ไม่ commit)

### Step 4: เขียน “สคริปต์เนื้อหา” ก่อนทำกราฟิก

แก้ไฟล์ `src/CONTENT.md` ให้ครบ:

- โครงหน้า (cover/instructions/practice/review/answer key/credits)
- ประเภทโจทย์ที่วนใช้ (เช่น count & write, circle the number)
- กติกาเฉลย (answer key rule)

แนวคิด: ทำให้คนทำกราฟิก/ทำไฟล์จริงอ่านแล้วทำตามได้ทันที

### Step 5: เขียน listing สำหรับ TPT

เริ่มจาก:

- `templates/tpt-listing-template.md` หรือ
- `templates/product-pack/listing/listing.md`

แล้วปรับให้ตรงสินค้า:

- Title ต้องมี `CCSS` + standard code + skill + range
- Description บรรทัดแรกต้องมี standard code ชัด
- Keywords ใส่ standard code + grade + skill + range + use case

อ้างอิงแนวทาง SEO ที่ `docs/seo.md`

### Step 6: QA ก่อน export/upload

ก่อนส่งออก/อัปโหลด ใช้เช็กลิสต์ 2 ชั้น:

- `templates/quality-checklist.md` (เช็คคุณภาพงาน/ความถูกต้อง)
- `docs/release-checklist.md` (เช็ครอบสุดท้ายก่อนขึ้น TPT)

## วิธีใช้ examples ให้คุ้ม

ถ้าจะทำเร็ว ให้เริ่มจาก copy ตัวอย่างที่ใกล้เคียง:

- `examples/k-cc-b5-how-many-pack/` (How many)
- `examples/k-cc-c7-compare-1-10-pack/` (Compare numbers)
- `examples/k-cc-a3-write-0-20-pack/` (Write numbers)
- `examples/k-cc-b4-one-to-one-cardinality-pack/` (One-to-one + cardinality)
- `examples/k-cc-c6-more-less-equal-pack/` (More/Less/Equal)

แล้วค่อยแตก theme/range เป็นสินค้าใหม่ โดย “คงโครงหน้าเดิม” ให้มากที่สุด

## กติกาแนะนำ (เพื่อให้ร้านโต)

- 1 product/ชุด โฟกัส 1 standard ให้ชัด (ช่วย SEO และความน่าเชื่อถือ)
- แตก variants แบบมีเหตุผล (range/theme/level) แทนการทำมั่ว ๆ
- ทำ bundle ทุก 6-8 products (อ้างอิง `docs/seo.md`)
