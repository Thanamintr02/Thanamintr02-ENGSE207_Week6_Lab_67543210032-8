## Evaluation

### Comparison Table

| Criteria | Weight | Arch 1: Monolith (Score) | Arch 1 (Weighted) | Arch 2: Microservices (Score) | Arch 2 (Weighted) |
|----------|--------|----------------|-------------------|----------------|-------------------|
| Development Speed | 30% | 5 | 1.5 | 2 | 0.6 |
| Operational Cost | 30% | 5 | 1.5 | 2 | 0.6 |
| Scalability | 20% | 2 | 0.4 | 5 | 1.0 |
| Maintainability | 20% | 4 | 0.8 | 4 | 0.8 |
| **Total** | **100%** | | **4.2** | | **3.0** |

### Selected Architecture
**Decision:** Architecture 1: Monolithic Architecture

**Reasons:**
1. **เหมาะสมกับขอบเขตงาน:** เนื่องจากจำนวนผู้เช่าหอพักมีจำนวนจำกัดและแน่นอน ไม่จำเป็นต้องใช้การ Scale ระดับสูง
2. **ความรวดเร็วในการพัฒนา:** Monolith ช่วยให้การพัฒนาและทดสอบทำได้จบในที่เดียว เหมาะกับข้อจำกัดด้านเวลา
3. **การจัดการที่ง่ายกว่า:** ลดความซับซ้อนในการ Deploy และการดูแลรักษา Server สำหรับนักศึกษาคนเดียว