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
