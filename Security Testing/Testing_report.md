Basic security measures were tested using OWASP ZAP to ensure user data protection and application integrity, especially considering the initial deployment challenges on a public domain.

* **Tool Used:** OWASP ZAP
* **Vulnerabilities Tested:** SQL Injection (SQLi), Cross-Site Scripting (XSS), and Broken Authentication.

### Security Testing Evidence (Screenshots)

#### 1. ZAP Alerts & Vulnerabilities Summary
This screenshot displays the overall active alerts generated during the automated spider and active scan. It categorizes risks into High, Medium, and Low severities.
![ZAP Alerts](./security_testing/Alerts_List.png)

#### 2.Individual Vulnerability Details
Detailed breakdown of the identified alerts, displaying the specific URLs and vectors tested during the vulnerability assessment.
![ZAP Vulnerability List](./security_testing/Individual_Vulnerability_Detail.png)

#### 3. Request Log (Attack Payload)
The exact HTTP request headers and payloads sent by OWASP ZAP to attempt SQL Injection and XSS bypasses.
![ZAP Request Log](./security_testing/Request.png)

#### 4. Response Log (Server Defense Proof)
The server response demonstrating that the malicious payloads were sanitized or rejected (e.g., HTTP 403 Forbidden or inputs being escaped properly).
![ZAP Response Log](./security_testing/Response.png)

### Summary of Results
* **SQL Injection (SQLi):** Pass. The system successfully blocks database manipulation attempts due to parameterized queries.
* **Cross-Site Scripting (XSS):** Pass. Input sanitation effectively prevents scripts from executing in user input fields.
