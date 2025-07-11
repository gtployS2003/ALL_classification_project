# 🧬 การวิเคราะห์ภาพเซลล์มะเร็งเม็ดเลือดขาวชนิด ALL เพื่อการจำแนกประเภทด้วยโมเดลการเรียนรู้ 

โครงงานนี้มีวัตถุประสงค์เพื่อพัฒนาระบบวิเคราะห์และจำแนกประเภทของภาพเซลล์มะเร็งเม็ดเลือดขาวชนิด Acute Lymphoblastic Leukemia (ALL) ซึ่งพบบ่อยในเด็กและเยาวชน โดยใช้เทคนิคปัญญาประดิษฐ์และการเรียนรู้ของเครื่อง (Machine Learning) เพื่อจำแนกเซลล์ออกเป็น 4 กลุ่มย่อย ได้แก่ benign, early, pre และ pro

## ในโครงการมีการ:
- รวบรวมและวิเคราะห์ข้อมูลภาพ
- พัฒนา Workflow สำหรับประมวลผลภาพในแพลตฟอร์ม KNIME
- สร้างและเปรียบเทียบโมเดลหลายประเภท ได้แก่ Deep Learning (Keras), Random Forest, MLP, และ SVM
- ประเมินผลด้วย Accuracy, F1-score และ Confusion Matrix
- นำเสนอผลลัพธ์ในรูปแบบ Visualization เพื่อความเข้าใจที่ชัดเจน
  
## 📁 ข้อมูลชุดข้อมูล (Dataset)

- แหล่งที่มา: นำมาจากชุดข้อมูลแบบเปิด (Open Dataset) บนแพลตฟอร์ม Kaggle ชื่อว่า "Multi Cancer Dataset" เลือกใช้เฉพาะส่วนที่เกี่ยวข้องกับ Acute Lymphoblastic Leukemia (ALL) เท่านั้น 
- แบ่งออกเป็น 4 ประเภท:
  - `all_benign` : เซลล์ปกติที่ไม่เป็นมะเร็ง
  - `all_early` : เซลล์ในระยะแรกของการเปลี่ยนแปลงเป็นมะเร็ง
  - `all_pre` : เซลล์ที่มีความผิดปกติก่อนเข้าสู่ภาวะรุนแรง
  - `all_pro` : เซลล์ที่เข้าสู่ระยะรุนแรงของโรค
- สำหรับการทดลองในโครงการนี้ ได้เลือกใช้ 1,000 ภาพแรกจากแต่ละคลาสย่อย รวมเป็นทั้งหมด 4,000 ภาพ 

🔗 [📂 ดาวน์โหลดชุดข้อมูล (Google Drive)](https://drive.google.com/file/d/1JxeIWdxCIpTOKOjK_TjxJVdu6ldFgITr/view?usp=sharing)

## 🧪 ขั้นตอนการดำเนินงาน
![ขั้นตอนการดำเนินงาน](assets/1.png)

## 📊 ผลการทดลอง

| โมเดล | Accuracy (Test)| Accuracy (Validate) | สรุปผล |
|-------------------------------|------------|-------------|-------------------------------|
| `Deep Learning (Keras)` | 0.932 | 0.927 | ต่ำที่สุดในกลุ่ม อาจต้องปรับปรุงโครงข่าย |
| `Random Forest` |0.968 | 0.943 | ประสิทธิภาพดีและเสถียร |
| `Multilayer Perceptron (MLP)` | 0.975 | 0.958 | ความแม่นยำสูงมาก |
| `Support Vector Machine (SVM)` | 0.978 | 0.968 | ดีที่สุดในทุกค่าประเมิน |

- โมเดล **SVM** ให้ผลลัพธ์ดีที่สุดในการจำแนกเซลล์

## 🎥 วิดีโอนำเสนอโปรเจกต์

📺 [คลิกเพื่อดูวิดีโอนำเสนอ](https://drive.google.com/file/d/12MTRZovXodTAMMyR801WaMSs7okX1I6A/view?usp=drive_link)

## 📄 รายงานฉบับเต็ม

[📄 เปิดอ่านรายงาน PDF](https://drive.google.com/file/d/1CVM14l4r9nVEpv9isX_muls_8J5-uj0i/view?usp=drive_link)

## 🔧 หมายเหตุเพิ่มเติม

> ⚠️ โปรเจกต์นี้พัฒนาทั้งหมดโดยใช้เครื่องมือ KNIME โดยไม่มีการเขียนโค้ดใด ๆ  
> รายงาน ชุดข้อมูล และวิดีโอจัดทำขึ้นเพื่อการศึกษาเท่านั้น

---

📌 **ผู้พัฒนา**: นางสาวสิริฉัตร์ ปานน้อย  
📚 **สำหรับโครงงานวิชา**: *Data Science*  
📅 **ปีการศึกษา**: *2/2567*
