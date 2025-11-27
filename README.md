# ENGCE301-2-68
Software Design and Development

## Group Members
- นายณัฐภัทร กลิ่นจันทร์ — 68543206006-7  /  [GitHub: 20Nattapat05](https://github.com/20Nattapat05)

- นายนันทิพัทธ์ สุกันทา — 68543206045-5  /  [GitHub: Nantipart](https://github.com/Nantipart)

## Important files
- [SE_INTRO_NOTES.md](./SE_INTRO_NOTES.md)
- [ENVIRONMENT.md](./ENVIRONMENT.md)

## DevTools Reflection (Week 1)

### 1) Browser รู้ได้อย่างไรว่าต้องรัน JavaScript ใน <script>?

- ตอน Browser โหลด HTML จะมี *HTML parser* ไล่อ่านโค้ดทีละแท็ก  
- พอเจอแท็ก <script> มันจะ *หยุดสร้าง DOM ชั่วคราว* แล้วส่งโค้ดด้านในไปให้ *JavaScript engine* รัน  
- รันเสร็จแล้วถึงจะกลับไปสร้าง DOM ต่อ  
→ เพราะงั้นแค่เจอแท็ก <script> Browser ก็รู้หน้าที่ว่าต้องรัน JavaScript ทันที

---

### 2) ถ้าไม่มี DevTools การ debug เว็บจะยากขึ้นยังไง?

- มองไม่เห็น *Error ของ JavaScript* (ไม่มี Console) ต้องเดาเองว่าโค้ดพังตรงไหน  
- เช็ค *Network request/response* ไม่ได้ ทำให้หาสาเหตุ API พัง / โหลดช้าแทบไม่ไหว  
- ปรับ *HTML / CSS / JS แบบสดๆ* ไม่ได้ ต้องแก้ไฟล์ → กดบันทึก → รีเฟรช วนไป เสียเวลามาก  
→ สรุปคือ จากการ “วิเคราะห์ปัญหาอย่างเป็นระบบ” กลายเป็น “เดาๆ เอาเอง”

---

### 3) Panel ที่น่าจะได้ใช้บ่อยสุดในเทอมนี้คืออะไร? ทำไม?

*ตอบ: Console (อันดับ 1) + Elements / Network (สำรอง)*

- *Console*  
  - ใช้ดู Error ของ JavaScript  
  - ใช้ console.log() เช็คค่าตัวแปร / Flow การทำงาน  
  - เวลาโค้ดไม่ไปตามที่คิด Console คือที่แรกที่ต้องเปิด

- *Elements*  
  - ใช้ Inspect ดูโครงสร้าง HTML จริงที่ Browser เรนเดอร์ + เช็คว่า class/id ตรงไหม  
  - แก้ CSS ชั่วคราวเพื่อหาว่าต้องเปลี่ยนอะไรในไฟล์จริง

- *Network*  
  - ใช้ดูว่าร้องขอ API สำเร็จไหม, status code อะไร, response เป็นอะไร  
  - ใช้เช็คว่าไฟล์ไหนโหลดช้า / ไม่โหลดเลย

สำหรับนักศึกษาส่วนใหญ่ *Console จะถูกเปิดก่อนเสมอเวลาเว็บ “ไม่ทำงานตามที่คิด”*