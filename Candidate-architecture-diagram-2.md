## Candidate Architecture 2: Microservices Architecture

**Overview**
แยกการทำงานออกเป็น Service ย่อยๆ ตามโดเมนงาน เช่น Booking Service, Billing Service และ Notification Service โดยสื่อสารกันผ่าน API

## Components
**API Gateway:** จุดรับ Request แรกและกระจายไปยัง Service ที่เกี่ยวข้อง

**Auth Service:** จัดการการเข้าสู่ระบบและสิทธิ์

**Booking Service:** จัดการห้องพักและการจอง

**Billing Service:** จัดการคำนวณเงินและชำระเงิน

## Technology Stack
**Frontend:** Next.js

**Backend:** Go (Golang) หรือ Java Spring Boot

**Database:** แยก Database ตาม Service (PostgreSQL และ MongoDB)

**Others:** RabbitMQ สำหรับส่งข้อความระหว่าง Service

## Architectural Patterns
Microservices Pattern

API Gateway Pattern


**Diagram**


<img width="900" height="518" alt="image" src="https://github.com/user-attachments/assets/5cdf07b7-a994-4e51-8e06-811da3794bd8" />


**Pros & Cons**
**Pros:**

✅ สามารถขยายเฉพาะ Service ที่มีความต้องการสูงได้ (Scalability)

✅ เทคโนโลยีที่ใช้ในแต่ละ Service ไม่จำเป็นต้องเหมือนกัน

**Cons:**

❌ ความซับซ้อนสูงมากในการจัดการเรื่องการเชื่อมต่อและข้อมูลข้าม Service

❌ ใช้ทรัพยากร Server สูงและมีค่าใช้จ่ายมากกว่า Monolith
