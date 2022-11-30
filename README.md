# DADS5001_Quiz1

โปรแกรมบันทึกข้อมูล Calorie จากอาหารประเภทเครื่องดื่ม

โดยจะเก็บข้อมูล Date, Name, Drink (ประเภทเครื่องดื่ม),และ Calorie

Function ในตัวโปรแกรมจะประกอบไปด้วย
1. Insert - รับข้อมูล Input นำไปสร้าง JSON file เพื่อ Load เข้า MongoDB

2. Edit data - ใน Edit data จะประกอบไปด้วย Edit และ Delete
 
    โปรแกรมจะเริ่มจากการ Search ก่อนด้วย Date, Name เพื่อให้ User เลือกรายการที่ต้องการ Edit หรือ Delete จากกล่องแสดงผล โดยตรงนี้ User สามารถใช้ปุ่ม Search ในการ refresh ดูข้อมูลใน MongoDB ได้
    
    เมื่อ User เลือกรายการที่ต้องการ Edit หรือ Delete แล้ว ตัวโปรแกรมจะเก็บค่า ID ของ Object เอาไว้เป็นตัว Matching ในการ Update ข้อมูลใน MongoDB
    
3. Summary Data - ขั้นตอนการนำผลมาแสดงเป็น Graph
    โดยตัว Graph จะเป็น Pie Chart เพื่อแสดงสัดส่วนการได้รับ Calorie จากเครื่องดื่มประเภทต่างๆในช่วงเวลาที่ User กำหนดได้
    
    ![image](https://user-images.githubusercontent.com/115795313/204820358-64f138ae-c43a-46f5-ac1f-9facee0a4865.png)

    นอกจากนี้ตัว Summary Data ยังมี Function "Get User" เมื่อใส่วันที่เข้าไปจะแสดงชื่อ User ที่มีข้อมูลอยู่ในช่วงวันที่ดังกล่าวเพื่อให้ User สามารถเลือกข้อมูลที่ต้องการแสดงผลได้ แต่ถ้า User ไม่ใส่วันที่ข้อมูลที่ดึงมาจะเป็นข้อมูลทั้งหมดที่มีใน MongoDB โดย User สามารถใส่ข้อมูล Start Date หรือ End Date อย่างใดอย่างหนึ่งได้เช่นกัน
    
    เมื่อ User เลือกข้อมูลที่ต้องการจะทำการไปดึงข้อมูลแบบ Aggregation มาจาก MongoDB เพื่อนำไปแสดงผล
    
