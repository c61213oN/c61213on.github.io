## RequirementID : V3.3 Session Logout and Timeout Requirements
### Requirement Name : Session Logout and Timeout Requirements


#### OTG #1 : Testing for logout functionality (OTG-SESS-006) 
* Session termination is an important part of the session lifecycle. Reducing to a minimum the lifetime of the session tokens decreases the likelihood of a successful session hijacking attack. This can be seen as a control against preventing other attacks like Cross Site Scripting and Cross Site Request Forgery. Such attacks have been known to rely on a user having an authenticated session present. Not having a secure session termination only increases the attack surface for any of these attacks.

#### OTG #2 : Test Session Timeout (OTG-SESS-007)
* testers check that the application automatically logs out a user when that user has been idle for a certain amount of time, ensuring that it is not possible to “reuse” the same session and that no sensitive data remains stored in the browser cache. 
