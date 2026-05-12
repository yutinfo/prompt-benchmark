# Role
คุณคือ Senior UI Engineer และ Frontend Developer ที่เชี่ยวชาญการออกแบบเว็บด้วย HTML, CSS และ Vanilla JavaScript รวมถึงการทำ UI แนว glassmorphism, liquid glass, iOS-style interface และ modern responsive design

# Task
ช่วยปรับ UI ของเว็บ Todo List เดิมให้เป็นสไตล์กระจกแก้วแบบ iOS 26-inspired / Liquid Glass โดยยังคง logic และ feature เดิมทั้งหมดไว้เหมือนเดิม

# Context
ฉันมีเว็บ Todo List แบบง่าย ๆ ที่สร้างด้วย HTML, CSS และ Vanilla JavaScript อยู่แล้ว ข้อมูลเก็บใน browser ด้วย localStorage ไม่ใช้ database ไม่ใช้ backend และไม่ใช้ framework

ตอนนี้ต้องการเปลี่ยนเฉพาะหน้าตาและประสบการณ์ใช้งานให้ดู modern, premium และเหมือนกระจกแก้วแบบ iOS 26-inspired มากขึ้น โดยไม่ทำให้ระบบเดิมพัง

# Existing Features ที่ต้องคงไว้
1. เพิ่ม Todo ได้
2. แก้ไข Todo ได้
3. ลบ Todo ได้
4. ติ๊ก completed ได้
5. Filter รายการได้:
   - All
   - Active
   - Completed
6. Clear completed ได้
7. แสดงจำนวน:
   - งานทั้งหมด
   - งานที่ทำเสร็จแล้ว
   - งานที่ยังไม่เสร็จ
8. เก็บข้อมูลด้วย localStorage
9. Refresh หรือปิด browser แล้วเปิดใหม่ ข้อมูลยังอยู่
10. ไม่ต้องมี login
11. ไม่ต้องใช้ database
12. ไม่ต้องใช้ backend
13. ไม่ต้องใช้ framework

# UI Direction
ปรับ UI ให้เป็นแนว:
- iOS 26-inspired Liquid Glass
- Glassmorphism
- Frosted glass panel
- Translucent cards
- Soft blur background
- Premium Apple-like minimal interface
- Clean spacing
- Rounded corners ขนาดใหญ่
- Subtle shadows
- Soft border highlight
- Smooth micro-interactions

# Visual Requirements
1. ใช้ background เป็น gradient นุ่ม ๆ เช่น blue / purple / pink / cyan แบบ premium
2. เพิ่ม abstract blurred blobs หรือ glow shapes ด้านหลัง เพื่อให้กระจกดูมีมิติ
3. Todo container หลักให้เป็น glass card:
   - background: rgba(...)
   - backdrop-filter: blur(...)
   - border: 1px solid rgba(...)
   - box-shadow แบบนุ่ม
   - border-radius ขนาดใหญ่
4. Todo item แต่ละรายการให้เป็น glass item แยกชั้น
5. ปุ่ม Add, Filter, Edit, Delete, Clear Completed ให้เป็นปุ่มใสแบบ glass หรือ semi-transparent
6. completed task ให้ยังดูชัดเจน แต่มี opacity ลดลง และ text-decoration line-through
7. input field ให้เป็น glass input:
   - translucent background
   - soft border
   - focus glow
8. เพิ่ม hover effect และ active state ให้ปุ่ม
9. เพิ่ม transition ที่นุ่มนวล เช่น 0.2s–0.3s
10. ใช้ font ที่ดู modern เช่น system font:
   - -apple-system
   - BlinkMacSystemFont
   - "Segoe UI"
   - sans-serif

# UX Requirements
1. UI ต้องอ่านง่าย ไม่ใสจนอ่านยาก
2. Contrast ต้องเพียงพอ
3. ใช้งานบนมือถือได้ดี
4. Layout ต้อง responsive
5. ปุ่มต้องกดง่าย โดยเฉพาะบน mobile
6. อย่าใช้ effect หนักเกินไปจนเว็บช้า
7. Empty state ต้องดูสวยขึ้นและเข้ากับ glass UI
8. Filter ที่ active อยู่ ต้องมองเห็นชัด
9. ไม่ควรเปลี่ยน flow การใช้งานเดิม
10. ไม่ควรลบ feature เดิมออก

# Technical Requirements
1. ใช้ HTML, CSS และ Vanilla JavaScript เท่านั้น
2. ทำเป็นไฟล์เดียวเหมือนเดิม เช่น index.html
3. ไม่ใช้ React, Vue, Angular หรือ framework อื่น
4. ไม่ใช้ database
5. ไม่ใช้ backend
6. ไม่ใช้ external UI library
7. สามารถใช้ CSS backdrop-filter ได้
8. ต้องมี fallback กรณี browser ไม่รองรับ backdrop-filter
9. อย่าแก้ logic localStorage จนข้อมูลเดิมหาย
10. ถ้ามีโค้ดเดิม ให้ refactor เฉพาะส่วน UI/CSS เป็นหลัก
11. JavaScript แก้เฉพาะเท่าที่จำเป็นสำหรับ class, animation หรือ state
12. Code ต้อง clean อ่านง่าย และไม่ซ้ำซ้อน

# Design Details
ช่วยออกแบบให้มีความรู้สึกประมาณนี้:
- หน้าหลักเหมือน floating glass panel อยู่กลางจอ
- มีแสงสะท้อนบาง ๆ บน card
- มุมโค้งใหญ่แบบ modern Apple UI
- ปุ่มมีความนูนเบา ๆ เหมือนอยู่ใต้ชั้นกระจก
- สีโดยรวมสว่าง สะอาด และ premium
- ไม่ทำให้ดูรกหรือแฟนซีเกินไป

# Output Format
ช่วยส่งโค้ดทั้งหมดเป็นไฟล์เดียวใน code block เดียว ชื่อ index.html
ถ้าแก้จากโค้ดเดิม ให้ส่งเวอร์ชันเต็มที่ copy ไปวางแทนไฟล์เดิมได้ทันที
หลัง code block ช่วยสรุปสั้น ๆ ว่าปรับ UI อะไรไปบ้าง และยังคง feature เดิมอะไรไว้