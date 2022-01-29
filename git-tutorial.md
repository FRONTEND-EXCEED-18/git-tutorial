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

#### Table of Content
- [สร้าง repository และเชื่อม folder บนเครื่องของเราเข้ากับ GitHub](#create-repo)
- [การส่งไฟล์ขึ้นไปบน GitHub](#push)
- [ดึงโค้ดล่าสุดลงมาไว้ในเครื่องเรา](#pull)

<span id="create-repo"></span>
## 🦄 Creating repository
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

10. ถึงเวลาที่เราจะทำให้ folder นี้เชื่อมไปที่ repository ที่เราเพิ่งสร้างบน GitHub ผ่านการตั้ง `remote` โดยให้ไปที่หน้า repository ของเราบน GitHub (ดูจากภาพด้านล่าง)

<p align="center">
  <img src="https://github.com/nutchanonc/exceed18-frontend/blob/main/images/4.png?raw=true" width="60%"/>
</p>

ทำการ copy คำสั่งที่เป็น `git remote add origin https://github.com/...` และนำไปวางใน `Command prompt` หรือ `Terminal` ของเราจากนั้นกด Enter

<p align="center">
  <img src="https://github.com/nutchanonc/exceed18-frontend/blob/main/images/9.png?raw=true" width="60%"/>
</p>

หากไม่มีข้อความอะไรขึ้นมาแปลว่า repository ของเราบน GitHub ถูกเซ็ตไว้บน folder นี้เรียบร้อยแล้ว หากใครที่ไม่มั่นใจในการกระทำของตัวเองที่ผ่านมา สามารถเช็คว่าเราตั้ง `remote` ไปหรือยังโดยการใช้คำสั่ง `git remote -v` ดังภาพด้านล่างและเช็คว่าลิงค์ที่แสดงขึ้นมาตรงกับบน GitHub หรือไม่

<p align="center">
  <img src="https://github.com/nutchanonc/exceed18-frontend/blob/main/images/10.png?raw=true" width="60%"/>
</p>

หรือในกรณีที่ copy คำสั่งบน github มาผิด เช่นลิงค์ไม่ครบ ให้ทำใช้คำสั่ง `git remote remove origin` เพื่อลบ remote อันเก่าออก จากนั้นให้กลับไปเริ่มต้นข้อ 10 ใหม่

11. ขั้นตอนสุดท้ายคือการเลือก `branch` ที่เราจะต้องทำงาน สำหรับงานที่ทำใน Exceed รอบนี้เราอาจจะไม่พูดถึงการใช้ branch ช่วยทำงาน แต่การเริ่มต้นทำงานบน repository ใหม่ เราควรที่จะทำงานให้ถูก branch เริ่มต้นของเราด้วย ให้เรากลับไปดูที่หน้า GitHub ***ดังภาพด้านล่าง***แล้วเช็ค **ตัวที่วงกลมสีแดง** ถ้าหากของใครที่เขียนว่า `master` น้องสามารถข้ามขั้นตอนนี้ไปได้เลย แต่สำหรับคนที่ขึ้นว่า `main` หรืออื่นๆ ให้ใช้คำสั่ง 
```sh
git branch -b <ชื่อตรงวงกลมสีแดงของ GitHub เรานะ>
```
 
 เพื่อสลับไปทำงานบน branch เริ่มต้นของ GitHub เรา

<p align="center">
  <img src="https://github.com/nutchanonc/exceed18-frontend/blob/main/images/5.png?raw=true" width="60%"/>
</p>

12. 🎉 ยินดีด้วยครับ ตอนนี้ folder ของน้องได้เชื่อมกับ GitHub เป็นที่เรียบร้อยแล้ว ต่อไปเราจะมาลองส่งไฟล์จากเครื่องของเราขึ้นไปไว้บน GitHub กัน อย่าเพิ่งปิด `Command prompt` หรือ `Terminal` นะ เราจะใช้ต่อกันในหัวข้อด้านล่างกัน 😁

<br /><br />

<span id="push"></span>
## 👩🏻‍💻 Pushing files to GitHub

1. เราจะมาลองสร้างไฟล์ และ ส่งมันขึ้นไปบน GitHub กัน เริ่มจากเปิด Vscode ขึ้นมา จากเมนูด้านบน ไปที่ File > Open Folder > เลือก folder ที่เราเพิ่งสร้างจากขั้นตอนด้านบน
<p align="center">
  <img src="https://github.com/nutchanonc/exceed18-frontend/blob/main/images/push1.png?raw=true" width="60%"/>
</p>

2. สร้างไฟล์ `README.md` ขึ้นมาหลังจากนั้นพิมพ์ `# Welcome to Exceed Camp` ลงไปในไฟล์นั้น หลังจากนั้นให้ save ไฟล์

**Note: พี่แนะนำให้เปิด Autosave ของ Vscode โดยไปที่ File > แล้วเลือก Autosave**

<p align="center">
  <img src="https://github.com/nutchanonc/exceed18-frontend/blob/main/images/push2.png?raw=true" width="60%"/>
</p>

3. กลับมาที่ `Command prompt` หรือ `Terminal` ของเรา ใช้คำสั่ง 3 อัน ตามด้านล่างเลย
```sh
git add .
```
```sh
git commit -m "hello github"
```
ขั้นตอนต่อไป หาก `branch` ของน้องไม่ใช่ `master` ให้ใส่ชื่อ `branch` ของน้องลงไปแทน `master`
```sh
git push origin master
```
<p align="center">
  <img src="https://github.com/nutchanonc/exceed18-frontend/blob/main/images/push3.png?raw=true" width="60%"/>
</p>

หากทุกอย่างเป็นไปตามภาพด้านบน ให้เราลองเข้าไปดูบน GitHub ของเรา (หากไม่มีอะไรเปลี่ยนแปลงให้ refresh หน้า)

<p align="center">
  <img src="https://github.com/nutchanonc/exceed18-frontend/blob/main/images/push4.png?raw=true" width="60%"/>
</p>

หากว่าน้องได้ผลลัพธ์ตามภาพถือว่าเราส่งไฟล์ขึ้นไปบน GitHub สำเร็จแล้ว 🥳 ยินดีด้วยครับตอนนี้น้องก็สามารถที่จะนำโค้ดที่น้องเขียน ส่งขึ้นไปบน GitHub เพื่อให้เพื่อนของน้องอ่านหรือดึงไปเขียนต่อได้แล้วครับ

(สามารถข้ามไปอ่านหัวข้อถัดไปได้เลยนะครับ🤷🏻‍♂️)

อธิบายคำสั่งแต่ละอันด้านบนสำหรับน้องคนไหนที่อยากทราบนะครับ ให้มองภาพการทำงานของ git เป็นเหมือนการส่งจดหมาย
`git add .` บอก git ว่าเราจะเอาทุกอย่างใน folder นี้ (. หมายถึง directory นี้)ใส่ซองจดหมาย
`git commit -m "สิ่งที่เราอยากจะบอก"` สั่งให้ git เอาทุกอย่างใส่ซองจดหมายพร้อมเขียน `สิ่งที่เราอยากจะบอก` ไว้บนซองจดหมาย
`git push origin master` คือการส่งซองจดหมายอันนี้ขึ้นไปบน GitHub โดยบนเว็บของ GitHub เราจะเห็น `commit` หรือ `สิ่งที่เราอยากจะบอก` อยู่ด้านหลังของไฟล์ที่เราเขียนหรือเปลี่ยนแปลงมัน

<span id="pull"></span>
## 👩🏻‍💻 Pulling files to GitHub

ก่อนหน้านี้เราทำการส่งไฟล์ขึ้นไปบน GitHub แล้ว ทีนี้ถ้าเพื่อนส่งไฟล์ขึ้นไปแล้วเราก็ต้องดึงลงมาไว้บนเครื่องของเราเพื่อให้โค้ดหรือ version ของโปรเจ็คระหว่าง **เรา** กับ **เพื่อน** ตรงกัน
โดนเราจะใช้คำสั่ง 

```sh
git pull origin master
```
หาก `branch` ของน้องไม่ใช่ `master` ให้ใส่ชื่อ `branch` ของน้องลงไปแทน `master`

เนื่องจากการทำงานของ `git` ไม่ได้คอย update โค้ดให้เราอัตโนมัติเวลาที่เพื่อน `push` โค้ดขึ้นมา พี่เลยแนะนำว่าก่อนจะเขียนโค้ดลงเพิ่มลงไปในโปรเจ็ค เราควรจะลงใช้คำสั่ง `pull` จากด้านบนดูก่อนเผื่อว่าเพื่อนน้องมีการส่งโค้ดใหม่ขึ้นมา👍🏻
