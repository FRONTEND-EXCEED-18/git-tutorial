# 📔 Git Tutorial 
นี่คือการสอนวิธีการใช้งาน `git` เบื่องต้น สำหรับน้องๆคนไหนที่ยังไม่ได้ติดตั้ง git บนเครื่องของตนเอง น้องๆสามารถดูวิธีการติดตั้งได้ที่ [link นี้เลย](https://docs.google.com/document/d/1vSLfeUgzAVimUMx4eSJcJV5QIghOD2xPcjDSOFVH9_4/edit?usp=sharing)

## 🤔 What is git?
git คืออะไร? `git` เป็นเครื่องมือที่ใช้ในการติดตามการเปลี่ยนแปลงของโค้ด รวมถึงอนุญาติให้เราสามารถเขียนโค้ดร่วมกับคนอื่นๆได้ โดยในค่าย Exceed 18 นี้ เราจะมาทดลองใช้ git ทำงานร่วมกับเพื่อนๆกัน

เรามาเริ่มรู้จักกับคำศัพท์ต่างๆที่เกี่ยวข้องกับ git กันเลย

### `Repository`
Repository คือที่เก็บโค้ด การสร้าง repository จะเหมือนกับ project ขึ้นมาอันหนึ่ง โดยที่แรกเริ่มมามันจะเป็น repository เปล่าๆหมายความว่าไม่มีโค้ดอยู่ในนั้นเลย

### `Commit`
commit เป็นเหมือนการ save โค้ดที่เราทำไว้เพื่อรอส่งขึ้นไปเก็บไว้บน GitHub

**การสั่ง commit ไม่ได้หมายความว่าโค้ดของเราจะถูกส่งขึ้นไปบน GitHub เลย เป็นเพียงการ save บนเครื่องของเราคนเดียว ถ้าอยากส่งขึ้นไปบน GitHub เพื่อให้เพื่อนสามารถนำไปใช้ต่อ จะต้องใช้คำสั่ง `push` ซึ่งเราจะพูดถึงในภายหลัง**

<hr />
<br />

## 🦄 Getting Started
เริ่มต้นการใช้งาน GitHub กันเถอะ

1. เริ่มจากสมัคร account ของ GitHub ได้ที่ [นี่เลย](https://github.com/join), ใครที่สมัครแล้วสามารถข้ามขั้นตอนนี้ไปได้เลย
2. ทำการ Sign in ให้เรียบร้อย และไปที่หน้าแรกของเรา เมนูทางด้านขวาบนจะมีเครื่องหมาย `+` อยู่ กดเข้าไปและคลิกที่ `New repository`

<p align="center">
  <img src="https://github.com/nutchanonc/exceed18-frontend/blob/main/images/1.png?raw=true" width="60%"/>
</p>

3. เมื่อคลิกเข้าไปเราจะพบกับหน้าที่ให้สร้าง repository ใหม่ ให้ตั้งชื่อ repository ของเราและใส่ description (ถ้ามี) หลังจากนั้นกดปุ่ม `Create repository` สีเขียวที่อยู่ด้านล่าง

<p align="center">
  <img src="https://github.com/nutchanonc/exceed18-frontend/blob/main/images/2.png?raw=true" width="60%"/>
</p>

4. ตอนนี้ repository อันใหม่ของเราถูกสร้างขึ้นมาแล้ว (จะต้องได้ผลลัพธ์ดังภาพด้านล่าง)

<p align="center">
  <img src="https://github.com/nutchanonc/exceed18-frontend/blob/main/images/3.png?raw=true" width="60%"/>
</p>

6. ขั้นตอนต่อไป เราจะทำให้เชื่อม directory (folder) บนเครื่องของเรา ที่เราจะทำงานเข้ากับ repository นี้ โดยให้น้องเข้าไปที่ `Command prompt` สำหรับ Windows และ `Terminal` หรือ เครื่องมือเปิด terminal อื่นๆ สำหรับ macOS
7. ไปที่ folder ที่เราต้องการจะทำงาน/เก็บไฟล์งานไว้ หลังจากนั้นใช้คำสั่งด้านล่างสร้าง folder ขึ้นมาตามภาพตัวอย่างด้านล่าง
```sh
mkdir <your-folder-name>
```
<p align="center">
  <img src="https://github.com/nutchanonc/exceed18-frontend/blob/main/images/6.png?raw=true" width="60%"/>
</p>

8. เข้าไปที่ folder นั้น
```sh
cd <your-folder-name>
```
<p align="center">
  <img src="https://github.com/nutchanonc/exceed18-frontend/blob/main/images/7.png?raw=true" width="60%"/>
</p>

9. ตอนนี้เราอยู่ที่ folder ที่เราต้องการจะทำงานรวมถึงเก็บไฟล์งานไว้ในนี้ เป็นที่เรียบร้อยแล้ว เราจะมาทำให้ folder นี้สามารถใช้งาน `git` ได้ โดยใช้คำสั่งด้านล่าง
```sh
git init
```
<p align="center">
  <img src="https://github.com/nutchanonc/exceed18-frontend/blob/main/images/8.png?raw=true" width="60%"/>
</p>
<p align="center">ควรได้ผลลัพธ์ตามภาพ แต่จะแตกต่างกันตรง path ด้านหลัง</p>
