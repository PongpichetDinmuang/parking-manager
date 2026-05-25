# Parking Manager

A simple, privacy-first parking fee management system — runs entirely in your browser, no installation, no account, no internet required.

ระบบจัดการค่าจอดรถรายเดือน ใช้งานง่าย รันในเบราว์เซอร์ล้วนๆ ไม่ต้องติดตั้ง ไม่ต้องสมัครสมาชิก

---

## 🚀 วิธีใช้งาน / Getting Started

### Desktop (แนะนำ)
ดับเบิลคลิกที่ไฟล์ `parking_manager.html` → เบราว์เซอร์เปิดขึ้นมาใช้งานได้ทันที

### Mobile (iPhone / Android)
เปิด link นี้ใน **Safari** หรือ **Chrome**:

👉 **[https://pongpichetdinmuang.github.io/parking-manager/parking_manager.html](https://pongpichetdinmuang.github.io/parking-manager/parking_manager.html)**

---

## ✨ ฟีเจอร์ / Features

### 🚗 จัดการลูกค้า
- เพิ่ม แก้ไข ลบข้อมูลลูกค้าได้
- เก็บข้อมูล ป้ายทะเบียน, ชื่อ, เบอร์ติดต่อ, วันที่เข้าจอด, ราคา/เดือน, รายละเอียดเพิ่มเติม
- ตั้งสถานะ **ออกแล้ว** สำหรับลูกค้าที่เลิกจอด ข้อมูลยังเก็บอยู่ครบ

### 📅 รายการรายเดือน
- กดปุ่ม **+ เพิ่มเดือนถัดไป** ระบบคำนวณ deadline อัตโนมัติจากวันเข้าจอด
- ติ๊ก ✅ เพื่อบันทึกว่าจ่ายแล้ว กดซ้ำเพื่อยกเลิก
- **ราคาแยกแต่ละเดือน** — ขึ้นราคาเดือนถัดไปได้โดยไม่กระทบเดือนเก่า
- ปุ่มลบเดือน (ป้องกันลบเดือนแรกโดยไม่ตั้งใจ)

### 🔴 สถานะอัตโนมัติ
ระบบคำนวณสถานะจาก deadline ของแต่ละเดือนอัตโนมัติ

| สถานะ | ความหมาย | สี |
|---|---|---|
| ✅ จ่ายแล้ว | ติ๊กว่าชำระแล้ว | 🟢 เขียว |
| 🟡 รอชำระ | ยังไม่ถึงกำหนดและยังไม่จ่าย | 🟡 เหลือง |
| 🔴 เลยกำหนด | เลย deadline แล้วยังไม่จ่าย | 🔴 แดง |

### 📊 ภาพรวม
- จำนวนคันที่จอดอยู่, ค้างชำระ, จ่ายครบ
- สรุปการเงิน — เก็บได้แล้วกี่บาท รอเก็บอีกกี่บาท
- รายชื่อลูกค้าเรียงจากค้างก่อน → รอชำระ → จ่ายครบ

### 📅 ปฏิทิน
- แสดงป้ายทะเบียนในวัน deadline ของแต่ละเดือน
- สีตามสถานะ กดที่ป้ายเพื่อดูรายละเอียดได้

### 💾 บันทึกและโหลดข้อมูล
- **Desktop Chrome/Edge**: กด **บันทึก** เพื่อ save ไฟล์ลง folder ที่เลือกได้เลย
- **Mobile / อื่นๆ**: ดาวน์โหลด `parking_data.json` แล้วโหลดกลับมาได้

---

## 🔒 ความเป็นส่วนตัว / Privacy

- ข้อมูลทั้งหมดอยู่ในเครื่องของคุณเท่านั้น ไม่มีการส่งออก internet
- ไม่มี cookies ไม่มีการติดตาม ไม่มีโฆษณา
- ไม่ใช้ localStorage ของเบราว์เซอร์ — ข้อมูลอยู่ใน `parking_data.json` ที่คุณดูแลเอง

---

## 📁 โครงสร้างไฟล์ / File Structure

```
📁 your-folder/
├── parking_manager.html    ← เปิดไฟล์นี้
└── parking_data.json       ← ข้อมูลของคุณ (สร้างเมื่อกด บันทึก)
```

---

## 📱 วิธีใช้บน iPhone / How to Use on iPhone

1. เปิด **Safari** แล้วไปที่ GitHub Pages link
2. กด **Share** → **Add to Home Screen** เพื่อสร้าง icon บนหน้าจอ
3. กด **บันทึก** เพื่อดาวน์โหลด `parking_data.json` ไปเก็บใน Files
4. กด **เปิด** เพื่อโหลดข้อมูลกลับมา

---

## 🌐 Browser Support

| Browser | Desktop | Mobile |
|---|---|---|
| Chrome | ✅ (save ตรง folder ได้) | ✅ |
| Safari | ✅ | ✅ |
| Edge | ✅ (save ตรง folder ได้) | ✅ |
| Firefox | ✅ (download/upload) | ✅ |

---

## 🛠️ Built With

- Pure HTML, CSS, JavaScript — ไม่มี framework ไม่มี dependency
- [Tabler Icons](https://tabler.io/icons)
- File System Access API (Chrome/Edge desktop)

---

*ทำเพื่อให้การจดบันทึกง่ายกว่าใช้ดินสอ 🚗*
