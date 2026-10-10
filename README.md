# โปรเจกต์ตั้งต้น Quiz Flutter — Provider + SQLite

รายวิชา 273387 Mobile Application Development (MAD) ภาคเรียนที่ 1/2569

โปรเจกต์นี้คือผลลัพธ์ของ **ปฏิบัติการบทที่ 13: แอปบัญชีรายรับ-รายจ่ายด้วย Provider และ SQLite** (กระบวนการที่ 1–6)
ใช้เป็นจุดตั้งต้นของ Quiz ให้ศึกษาโครงสร้างแล้วสร้าง model, provider และ UI ของ entity ที่ได้รับมอบหมายให้ทำ CRUD กับ SQLite ได้

## โครงสร้าง

```
lib/
├── main.dart                              ChangeNotifierProvider ครอบ MyApp
├── models/
│   └── my_transaction.dart                Model + toMap() / fromMap()
├── providers/
│   └── transaction_provider.dart          เปิดฐานข้อมูล + CRUD + notifyListeners()
└── screens/
    └── transaction_list_screen.dart       Consumer แสดงรายการ, ปุ่มลบ, ปุ่ม + เพิ่มรายการตัวอย่าง
```

| การทำงาน | เมธอดใน `TransactionProvider` | คำสั่ง sqflite |
|---|---|---|
| Create | `addTransaction()` | `insert` |
| Read | `fetchAndSetTransactions()` | `query` |
| Update | `updateTransaction()` | `update` |
| Delete | `deleteTransaction()` | `delete` |

## วิธีรัน

ต้องรันบน Android emulator หรือเครื่องจริง (sqflite ไม่รองรับ Web และ Windows)

```bash
flutter pub get
flutter run
```

## การส่งงาน Quiz

1. สร้าง repository ของตนเองบน GitHub ตั้งค่าเป็น **Private**
   (กดปุ่ม **Use this template → Create a new repository** ที่หน้านี้ หรือ clone แล้ว push ขึ้น repository ใหม่)
2. ทำงานและ push ขึ้น repository ของตนเองภายในเวลาสอบ
3. ไปที่ **Settings → Collaborators → Add people** แล้วเพิ่ม `nattaponk@nu.ac.th`

ข้อปฏิบัติ: เปิดได้เฉพาะเอกสารประกอบการสอน ห้ามใช้ AI
