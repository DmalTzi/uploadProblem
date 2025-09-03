# วิธีเตรียมไฟล์สำหรับการอัพ

### 1. ส่วนประกอบของ directory ที่ใช้สำหรับการอัพ
```
.
├── data
│   ├── sample
│   │   ├── 1.ans
│   │   └── 1.in
│   └── secret
│       ├── 1.ans
│       └── 1.in
│       
├── domjudge-problem.ini
├── problem.pdf
└── problem.yaml
```
`data` คือส่วนที่เก็บไฟล์ testcase ทั้งหมด  
`sample` คือส่วนที่เก็บ testcase ตัวอย่าง  
| ภายในประกอบด้วย `*.in` หมายถึง ไฟล์ input และ `*.ans` หมายถึงไฟล์ output  
`secret` คือส่วนที่เก็บ hidden testcase  
`problem.pdf` คือไฟล์สำหรับเก็บ statement ของโจทย์ข้อนี้  
`problem.yaml` setup สำหรับ domjudge

### 2. เขียน problem.yaml
```yaml
name: 'Say Hi To ...'
limits:
    memory: 512 # default หน่วยเป็น MB
timelimit: 1 # default หน่วยเป็น second
```
หากไม่ตั้งค่า `memory` ในระบบจะตั้งเป็น `default` คือ `256MB`  
### 3. zip file
เมื่อทำตามขั้นตอนด้านบน ทำการ zip ไฟล์ทั้งหมด โดยภายใต้ไฟล์ zip ต้องมีโครงสร้างตามข้อ 1

### 4. การ add file ไปที่ระบบ
1. ทำการ login
2. เข้า import / export
3. ในส่วนของ Contest ให้ทำการเลือกเป็น `Do not add / update contest data`
4. เลือก Problem archive ให้ทำการเลือก ไฟล์โจทย์ที่ถูก zip แล้ว
5. กด import
6. เมื่อ import เสร็จแล้ว สามารถเช็ครายละเอียดของโจทย์ที่ถูกเพิ่มเข้าไปได้
