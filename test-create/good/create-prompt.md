# Role
คุณคือ Senior Frontend Developer ที่ถนัดสร้างเว็บแอปขนาดเล็กด้วย HTML, CSS และ Vanilla JavaScript โดยไม่ใช้ framework และไม่ต้องใช้ database

# Task
ช่วยสร้างเว็บ Todo List แบบง่าย ๆ ในไฟล์เดียว โดยใช้ HTML, CSS และ JavaScript ทั้งหมดอยู่ในไฟล์เดียวกัน สามารถเปิดใช้งานได้ทันทีผ่าน browser

# Context
ฉันต้องการเว็บ Todo List สำหรับจดรายการงานทั่วไป เช่น งานที่ต้องทำประจำวัน งานส่วนตัว หรืองานเล็ก ๆ โดยไม่ต้องมีระบบ login และไม่ต้องเชื่อมต่อ backend หรือ database ข้อมูลทั้งหมดให้บันทึกไว้ใน browser ของผู้ใช้ด้วย localStorage เพื่อให้ปิด browser แล้วเปิดใหม่ ข้อมูลยังอยู่

# Core Requirements
1. ใช้ HTML, CSS และ Vanilla JavaScript เท่านั้น
2. ทำเป็นไฟล์เดียว เช่น index.html
3. ไม่ต้องใช้ database
4. ไม่ต้องใช้ backend
5. ไม่ต้องใช้ framework เช่น React, Vue, Angular
6. บันทึกข้อมูล Todo ลง localStorage
7. เมื่อ refresh หน้าเว็บหรือปิดแล้วเปิดใหม่ รายการ Todo ต้องยังอยู่
8. ผู้ใช้สามารถเพิ่ม Todo ใหม่ได้
9. ผู้ใช้สามารถกด checkbox เพื่อเปลี่ยนสถานะเป็น completed ได้
10. ผู้ใช้สามารถลบ Todo ได้
11. ผู้ใช้สามารถแก้ไข Todo ได้
12. แสดงจำนวนงานทั้งหมด งานที่ทำแล้ว และงานที่ยังไม่เสร็จ
13. มีปุ่ม filter:
   - All
   - Active
   - Completed
14. มีปุ่ม Clear Completed สำหรับลบงานที่ทำเสร็จแล้วทั้งหมด
15. ถ้าผู้ใช้กรอกช่องว่าง ไม่ต้องเพิ่ม Todo
16. ถ้าไม่มีรายการ ให้แสดง empty state เช่น “No tasks yet”

# UI/UX Requirements
1. หน้าตาดูเรียบง่าย สะอาด ใช้งานง่าย
2. รองรับ mobile และ desktop
3. ใช้ layout แบบ card อยู่กลางหน้าจอ
4. มี input สำหรับพิมพ์งาน และปุ่ม Add
5. รายการ Todo แต่ละอันควรอ่านง่าย มี checkbox, ข้อความ, ปุ่ม edit และปุ่ม delete
6. Todo ที่ completed ให้มีเส้นขีดทับข้อความ และสีจางลง
7. ปุ่มควรมี hover effect เล็กน้อย
8. ใช้สีที่ดูสบายตา เช่น ขาว เทา น้ำเงิน หรือเขียวอ่อน
9. ไม่ต้องใช้รูปภาพ
10. ไม่ต้องใช้ icon library

# Technical Requirements
1. เขียน JavaScript ให้แบ่ง function ชัดเจน เช่น
   - loadTodos()
   - saveTodos()
   - renderTodos()
   - addTodo()
   - deleteTodo()
   - toggleTodo()
   - editTodo()
   - clearCompleted()
2. Todo object ควรมีโครงสร้างประมาณนี้:
   {
     id: string,
     text: string,
     completed: boolean,
     createdAt: string
   }
3. ใช้ Date.now() หรือ crypto.randomUUID() สำหรับสร้าง id
4. ใช้ JSON.stringify() และ JSON.parse() สำหรับจัดการ localStorage
5. Code ต้องอ่านง่าย มี comment เฉพาะจุดที่จำเป็น
6. หลีกเลี่ยง code ซ้ำซ้อน
7. รองรับกรณี localStorage ไม่มีข้อมูลหรือข้อมูลเสียหาย
8. ไม่ใช้ external library

# Output Format
ช่วยส่งโค้ดทั้งหมดเป็นไฟล์เดียวใน code block เดียว โดยใช้ชื่อไฟล์ index.html
หลังจากโค้ด ให้สรุปสั้น ๆ ว่าเว็บนี้ทำอะไรได้บ้าง และเปิดใช้งานอย่างไร