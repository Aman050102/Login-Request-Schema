# UP REG - Academic Tracking System (Test & API Mockup)

โปรเจกต์นี้เป็นส่วนหนึ่งของการทดสอบระบบและออกแบบ API Setup สำหรับระบบ **UP REG (Academic Tracking System)** ของมหาวิทยาลัยพะเยา โดยครอบคลุมทั้งการทำ Automated Testing ด้วย Robot Framework และการออกแบบ API Schema บน Postman

## 📌 ฟีเจอร์ของโปรเจกต์
1. **Automated Login Testing:** ทดสอบกระบวนการ Login ที่ผ่านระบบ Microsoft OAuth และรองรับ Multi-Factor Authentication (MFA)
2. **API Mocking:** ออกแบบ API Responses สำหรับกรณีต่างๆ (Success, Invalid Password, MFA Timeout) บน Postman

---

## 🤖 1. Automated Testing (Robot Framework)
ระบบใช้ SeleniumLibrary ในการควบคุม Browser เพื่อจำลองการล็อกอินของนักศึกษา

### เงื่อนไขการทดสอบ (Test Scenarios)
- **Valid Login:** ล็อกอินด้วยชื่อผู้ใช้และรหัสผ่านที่ถูกต้อง พร้อมระบบหยุดรอให้กดยืนยัน MFA บนมือถือ
- **Invalid Password Error:** รองรับการดักจับ Alert เมื่อรหัสผ่านผิดพลาด (`รหัสผ่านไม่ถูกต้อง`)
- **MFA Timeout Error:** รองรับกรณีที่ผู้ใช้ยืนยันตัวตนไม่ทันเวลา (`ไม่ได้รับการติดต่อจากคุณทันเวลา`)

---

## 🌐 2. API Specification & Mock Server
สำหรับการออกแบบฝั่ง Backend API ได้จำลอง Endpoint สำหรับการ Authentication ไว้ดังนี้:

* **Endpoint:** `POST /api/v1/auth/login`
* **Mock Server URL:** `[วาง URL Mock Server ของคุณที่ได้จาก Postman ตรงนี้]`


