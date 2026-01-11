## Candidate Architecture 1: Monolithic Layered Architecture ##
**Overview**
เป็นการออกแบบโครงสร้างที่รวมทุก Module (จอง, แจ้งซ่อม, บิล) ไว้ใน Application เดียวกัน โดยแบ่งเป็นชั้น (Layers) ชัดเจน เน้นความเรียบง่ายในการพัฒนาและ Deploy

## Components
**Presentation Layer:** ส่วนหน้าจอผู้ใช้งาน (Web UI)

**Business Logic Layer:** ส่วนประมวลผลการจอง, คำนวณค่าไฟ และจัดการแจ้งซ่อม

****Data Access Layer:** ส่วนเชื่อมต่อกับฐานข้อมูล

**Database:** ฐานข้อมูลเชิงสัมพันธ์สำหรับเก็บข้อมูลทั้งหมด

## Technology Stack 
**Frontend:** React.js

**Backend:** Node.js (Express)

**Database:** PostgreSQL

**Others:** Docker สำหรับการ Deploy

**Architectural Patterns**
Layered Architecture

Model-View-Controller (MVC)

**Diagram**

**Pros & Cons**
**Pros:**

✅ พัฒนาและทดสอบได้รวดเร็วเนื่องจากไม่มีความซับซ้อนในการเชื่อมต่อเครือข่าย

✅ ง่ายต่อการ Deploy และประหยัดค่าใช้จ่าย Server

**Cons:**

❌ หากส่วนใดส่วนหนึ่งมี Error รุนแรง อาจทำให้ระบบล่มทั้งหมด (Single point of failure)

❌ ขยายระบบเฉพาะส่วน (Scale) ได้ยาก


