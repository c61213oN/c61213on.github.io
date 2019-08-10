## RequirementID : V3.3 Session Logout and Timeout Requirements
### Requirement Name : Session Logout and Timeout Requirements


#### OTG #1 : Testing for logout functionality (OTG-SESS-006) 
* Session termination is an important part of the session lifecycle. Reducing to a minimum the lifetime of the session tokens decreases the likelihood of a successful session hijacking attack. This can be seen as a control against preventing other attacks like Cross Site Scripting and Cross Site Request Forgery. Such attacks have been known to rely on a user having an authenticated session present. Not having a secure session termination only increases the attack surface for any of these attacks.

#### OTG #2 : Test Session Timeout (OTG-SESS-007)

* ในการใช้งาน application จะมีช่วงเวลาที่ผู้ใช้ไม่ได้ใช้งานเป็นระยะเวลาหนึ่งต้องทำให้มั่นใจว่า session จะ "ไม่สามารถนำกลับมาใช้ซ้ำ" และ "ต้องไม่มีข้อมูลที่ละเอียดอ่อนหลงเหลืออยู่ใน browser cache"
