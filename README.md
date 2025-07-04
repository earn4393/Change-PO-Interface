# Change PO Interface
change request
- interface ที่ใช้แก้ไข PO
* S : ด้วยข้อจำกัดด้าน license ผู้ใช้ต้องการแก้ไขข้อมูลใน PO เพิ่มโดยไม่ผ่าน SAP
* T : แก้ไข payment term ใน SAP interface ที่ใช้แก้ไข PO
* A
  - review การทำงานของ code
  - ออกแบบและหา case ที่ใช้ในการเพิ่ม field payment term ใน PO 
  - แก้ไข Code และทดสอบ โดยเพิ่ม confige ใน table ZTMM001 และเพิ่มเงื่อนไขว่าถ้าแก้ที่ header ให้เช็คแค่ว่ามี PO ในระบบไหมเท่านั้นใน validation
  - ทดสอบกับผู้เกี่ยวกับข้อง
* R : ผู้ใช้สามารถแก่ไข SO ได้ตาม field ที่ร้องขอมา
## องค์ประกอบ
- ZFM_SD_0018_SO_INTERFACE : main programe
- LZFG_SD_18TOP : ประกาศตัวแปร , พารามิเตอร์ และหน้า screen
- LZFG_SD_18F01 : ฟังก์ชันเพิ่มเติมที่เขียนขึ้นเพื่อให้ main ใช้
## จุดเด่น
- ใช้ STD BAPI สำหรับแก้ SO : BAPI_SALESORDER_CHANGE
