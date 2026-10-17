# เอกสารและข้อมูลสรุปสำหรับแก้ไขเล่มเค้าโครงโครงงาน (CP353761 Seminar)

**หัวข้อโครงงาน (ภาษาไทย):** การเพิ่มประสิทธิภาพการตรวจจับภาวะปอดอักเสบจากภาพเอกซเรย์ทรวงอกด้วยการลดสัญญาณรบกวนและปัญญาประดิษฐ์ที่อธิบายได้  
**หัวข้อโครงงาน (ภาษาอังกฤษ):** Enhancing Chest X-RAY Infiltration Detection Using Noise Reduction and Explainable AI  

Repository นี้รวบรวม **เอกสารต้นฉบับ, รายการแก้ไขเล่มตาม Feedback อาจารย์, ตารางผลลัพธ์ (`.csv`), และรูปภาพ Confusion Matrix / กราฟความละเอียดสูงสำหรับพิมพ์ใส่เล่ม** ไว้ครบในที่เดียว เพื่อให้ผู้ร่วมวิจัยหรือ AI สามารถนำไปเขียนและจัดพิมพ์เล่มเค้าโครงโครงงานต่อได้ทันที

---

## เริ่มต้นใช้งาน (สำหรับเพื่อนร่วมทีม หรือ AI ที่มารับช่วงต่อ)

1. **อ่านแผนและรายการสิ่งที่ต้องแก้ไขทั้งหมดได้ที่ไฟล์หลัก:**
   - **[`รายการแก้ไขเล่มโครงงาน.md`](./รายการแก้ไขเล่มโครงงาน.md)** *(มีครบทั้ง Checklist รายบท/รายหน้า, ตารางผลลัพธ์ทั้ง 2 ชุดข้อมูล, และแนวทางวางรูป Confusion Matrix)*
2. **อ่านข้อความต้นฉบับของเล่มเดิม (แบบแก้สระลอยแล้ว) และกฎการจัดหน้าได้ที่:**
   - [`reference_docs_for_ai/1_ข้อความต้นฉบับเล่มเค้าโครง_ฉบับคลีน.md`](./reference_docs_for_ai/1_ข้อความต้นฉบับเล่มเค้าโครง_ฉบับคลีน.md) *(ข้อความทั้ง 19 หน้าจากเล่มเดิม)*
   - [`reference_docs_for_ai/2_สรุปแนวปฏิบัติในการจัดพิมพ์เค้าโครงโครงงาน.md`](./reference_docs_for_ai/2_สรุปแนวปฏิบัติในการจัดพิมพ์เค้าโครงโครงงาน.md) *(กฎการตั้งขอบกระดาษ ฟอนต์ TH Sarabun New 18/16/14pt และรูปแบบตาราง/รูปภาพ)*

---

## โครงสร้างไฟล์และโฟลเดอร์ใน Repository นี้

```text
.
├── รายการแก้ไขเล่มโครงงาน.md                     <-- [ไฟล์หลัก] Checklist สิ่งที่ต้องแก้ในเล่ม + ตารางสรุปทั้งหมด
├── เค้าโครงโครงงานคอมพิวเตอร์-ฉบับแก้ไข-091069-0643.pdf <-- ไฟล์ PDF เล่มเค้าโครงเดิม (ก่อนแก้รอบล่าสุด)
├── แนวปฏิบัติในการจัดพิมพ์เค้าโครงโครงงาน.pdf           <-- ไฟล์ PDF คู่มือการจัดพิมพ์ของสาขาวิชา
├── class200_methods_colab.ipynb                 <-- Notebook ทดลอง 21 วิธี (L1-L4 + DWT) บนชุดข้อมูล NIH
├── V2Seminar_source_code.ipynb                  <-- Notebook ทดลอง 21 วิธี (L1-L4 + DWT) บนชุดข้อมูล VinBigData
│
├── reference_docs_for_ai/                       <-- ข้อความต้นฉบับและกฎการจัดพิมพ์แบบคลีนสำหรับ AI
│   ├── 1_ข้อความต้นฉบับเล่มเค้าโครง_ฉบับคลีน.md
│   └── 2_สรุปแนวปฏิบัติในการจัดพิมพ์เค้าโครงโครงงาน.md
│
├── confusion_matrices/                          <-- รูป Confusion Matrix ทั้งหมด
│   ├── 4_print_ready_for_report/                <-- [แนะนำสำหรับใส่เล่ม] รูปขนาดตัวอักษรใหญ่ (300 DPI) แยกกลุ่ม 4-6 ช่อง
│   │   ├── 1_NIH_21_methods_split_large/
│   │   ├── 2_VinBigData_21_methods_split_large/
│   │   └── 3_v7_beta_print_ready/
│   ├── 1_21_methods_clean/                      <-- รูปต้นฉบับ 21 วิธีจาก Notebook
│   ├── 2_v7_beta_NIH/                           <-- รูปแยกตาม 16 สภาวะ Noise ของ NIH (Notebook_7 beta)
│   └── 3_v7_beta_VinBigData/                    <-- รูปแยกตาม 12 วิธีของ VinBigData (Notebook_7 beta vinbigdata)
│
├── figures/                                     <-- กราฟประกอบและภาพตัวอย่าง CXR ที่ผ่านการจำลอง/ลด Noise
│   ├── 1_notebooks_21_methods/                  <-- ภาพตัวอย่างจาก Notebook 21 วิธี
│   ├── 2_v7_beta_NIH/                           <-- กราฟ ROC-AUC Heatmap, PSNR vs AUC, Learning Curves (NIH)
│   └── 3_v7_beta_VinBigData/                    <-- กราฟและภาพตัวอย่างจำลอง Noise 5 ตระกูล (VinBigData)
│
└── github_v7_data_and_tables/                   <-- ไฟล์ข้อมูลตาราง .csv, .json และบทสรุปผลรันจริงทั้งหมด
    ├── 1_NIH_Notebook_7_beta/                   <-- ข้อมูลและตาราง .csv ครบชุดของ NIH (Notebook_7 beta)
    ├── 2_VinBigData_Notebook_7_beta/            <-- ข้อมูลและตาราง .csv ครบชุดของ VinBigData (Notebook_7 beta vinbigdata)
    └── 3_21_methods_tables/                     <-- ไฟล์ .csv ตารางผลลัพธ์ 21 วิธีของทั้ง NIH และ VinBigData
```

---

## Repository โค้ดการทดลองต้นทาง
- โค้ดและผลการทดลอง `Notebook_7 beta` ต้นทาง: [Catsack423/Enhancing-Chest-X-RAY-Infiltration-Detection-Using-Noise-Reduction-and-Explainable-AI (branch: `codex/notebook-v7-beta`)](https://github.com/Catsack423/Enhancing-Chest-X-RAY-Infiltration-Detection-Using-Noise-Reduction-and-Explainable-AI/tree/codex/notebook-v7-beta)
