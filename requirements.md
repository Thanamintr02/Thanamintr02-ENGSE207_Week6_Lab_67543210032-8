## Requirements Analysis

### Functional Requirements
1. นักศึกษาสามารถเลือกดูห้องที่ว่างและทำรายการจองห้องพักออนไลน์ได้
2. ระบบรองรับการแจ้งซ่อม/แจ้งปัญหาผ่านระบบ พร้อมแนบรูปภาพประกอบ
3. ระบบบันทึกเลขมิเตอร์และคำนวณค่าน้ำค่าน้อยไฟอัตโนมัติในแต่ละเดือน
4. แอดมินสามารถจัดการสถานะการชำระเงินและตรวจสอบหลักฐานการโอนเงินได้
5. ระบบสามารถส่งประกาศแจ้งเตือนข่าวสารไปยังผู้เช่าทุกคนได้

### Non-Functional Requirements
1. **Availability:** ระบบต้องพร้อมใช้งานอย่างน้อย 99.5% เพื่อรองรับการเข้าใช้งานในช่วงต้นเดือน
2. **Security:** ข้อมูลส่วนบุคคลและประวัติการชำระเงินต้องถูกปกป้องและเข้าถึงได้เฉพาะผู้มีสิทธิ์
3. **Usability:** ส่วนต่อประสานกับผู้ใช้ (UI) ต้องรองรับการใช้งานผ่านมือถือได้อย่างราบรื่น (Mobile Responsive)

### Constraints
1. **Time:** ต้องออกแบบและพัฒนาให้เสร็จสิ้นภายในระยะเวลาที่รายวิชากำหนด
2. **Cost:** ต้องใช้เทคโนโลยีที่เป็น Open-source เพื่อลดค่าใช้จ่ายในด้าน License
3. **Platform:** ต้องสามารถ Deployment บน Cloud Service ทั่วไปได้

### Quality Attribute Scenarios

#### Scenario 1: Performance during billing cycle
- **Quality Attribute:** Performance
- **Source:** ผู้เช่าหอพัก
- **Stimulus:** เข้าใช้งานพร้อมกันเพื่อตรวจสอบบิลค่าไฟในวันแรกของเดือน
- **Artifact:** System Service
- **Environment:** ช่วงเวลาที่มีการใช้งานสูง (Peak Load)
- **Response:** ระบบสามารถประมวลผลข้อมูลและแสดงผลบิลได้ถูกต้อง
- **Response Measure:** เวลาในการโหลดหน้าบิลต้องไม่เกิน 2 วินาที

#### Scenario 2: Modifiability for new payment methods
- **Quality Attribute:** Modifiability
- **Source:** นักพัฒนา (Developer)
- **Stimulus:** ต้องการเพิ่มช่องทางการชำระเงินใหม่ (เช่น PromptPay หรือ Credit Card)
- **Artifact:** Source Code / Payment Module
- **Environment:** ช่วงการปรับปรุงระบบ (Maintenance)
- **Response:** สามารถเพิ่ม Module ใหม่ได้โดยไม่กระทบระบบการจองห้องเดิม
- **Response Measure:** ใช้เวลาในการแก้ไขและทดสอบระบบใหม่ไม่เกิน 3 วันทำการ