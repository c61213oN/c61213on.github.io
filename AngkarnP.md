## Requirement ID : V3.3 Session Logout and Timeout Requirements
### Requirement Name : Session Logout and Timeout Requirements


#### OTG #1 : Testing for logout functionality (OTG-SESS-006) 

* การออกจากระบบเป็นการลด attack surface เนื่องจากเป็นการลดอายุของ session

#### OTG #2 : Test Session Timeout (OTG-SESS-007)

* ในการใช้งาน application จะมีช่วงเวลาที่ผู้ใช้ไม่ได้ใช้งานเป็นระยะเวลาหนึ่ง จึงต้องทำให้มั่นใจว่า session จะ "ไม่สามารถนำกลับมาใช้ซ้ำ" และ "ต้องไม่มีข้อมูลที่ละเอียดอ่อนหลงเหลืออยู่ใน browser cache"
