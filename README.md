# 🐞 Bug Bounty Report: XSS & IDOR Vulnerabilities

---

## 📌 Overview

This repository documents identified security vulnerabilities in a demo banking application, including:

- Cross-Site Scripting (XSS)
- HTTP Parameter Tampering (IDOR)

The report demonstrates how these vulnerabilities can be exploited and provides mitigation strategies.

---

## 🔐 Vulnerability 1: Cross-Site Scripting (XSS)

### 📝 Description
Cross-Site Scripting (XSS) allows attackers to inject malicious scripts into a trusted web application, enabling unauthorized access to sensitive data.

### 🌐 Target
https://demo.testfire.net/login.jsp

### ⚙️ Steps to Reproduce
1. Navigate to the login page  
2. Enter the payload:
   ```html
   <script>alert(document.cookie)</script>
   Observe the encoded output
Decode the Base64 response
🚨 Impact
Exposure of sensitive user data
Risk of financial fraud
Reputational damage
🛡️ Mitigation
Input validation and sanitization
Output encoding
Implement Content Security Policy (CSP)
🔓 Vulnerability 2: HTTP Parameter Tampering (IDOR)
📝 Description

This vulnerability allows attackers to manipulate request parameters and gain unauthorized access to sensitive data or perform unauthorized transactions.

🌐 Targets
https://demo.testfire.net/bank/transfer.jsp
https://demo.testfire.net/feedback.jsp
⚙️ Steps to Reproduce
Initiate a transaction
Intercept request using Burp Suite
Modify:
Transaction amount
Account number
Forward the request
🚨 Impact
Unauthorized transactions
Financial loss
Data breach
🛡️ Mitigation
Validate all user inputs
Implement proper access control
Avoid exposing sensitive identifiers
Use session-based authentication checks
🛠️ Tools Used
Burp Suite
Web Browser
Base64 Decoder
👩‍💻 Author

Chioma Lilian
Cybersecurity Analyst (ISC2 CC)

💼 LinkedIn: https://www.linkedin.com/in/chioma-lilian/
⚠️ Disclaimer

This project is for educational purposes only.
All testing was conducted on a legal demo environment.

---

