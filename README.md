# 🔐 Web Application Penetration Testing

This repository documents the setup, methodology, and findings from practicing **Web Application Penetration Testing** using vulnerable applications like **DVWA (Damn Vulnerable Web App)** and **OWASP Juice Shop**, tested with tools such as **Burp Suite**.

---

## 🛠️ Lab Setup

### 1. Tools & Environment
- **Host OS:** Kali Linux (VM or Bare Metal)
- **Vulnerable Apps:**
  - [DVWA](https://github.com/digininja/DVWA) via Docker
  - [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)
- **Testing Tools:**
  - Burp Suite Community Edition
  - Browser (Firefox configured with Burp proxy)

### 2. Installation

#### DVWA via Docker
```bash
# Pull and run DVWA
sudo docker run --rm -it -p 8888:80 vulnerables/web-dvwa
```
Access at: http://127.0.0.1:8888

## OWASP Juice Shop
# Pull and run Juice Shop
sudo docker run --rm -p 3000:3000 bkimminich/juice-shop
Access at: http://127.0.0.1:3000
---
# 🔎 Testing Methodology

The penetration testing approach follows the OWASP Top 10 guidelines.

## 1. Reconnaissance

Mapping the application

Identifying hidden files/directories

Detecting technologies used

### 2. Vulnerability Assessment

Cross-Site Scripting (XSS)

SQL Injection

Command Injection

Broken Authentication

Insecure Direct Object References (IDOR)

CSRF (Cross-Site Request Forgery)

3. Exploitation

Using Burp Suite to intercept and manipulate requests

Exploiting authentication bypasses

Injecting malicious payloads

4. Post-Exploitation

Extracting sensitive information

Privilege escalation

Session hijacking

📊 Reporting

Each test case should include:

Vulnerability Name

Description

Steps to Reproduce

Impact

Recommendation

Example:

Vulnerability	Description	Steps to Reproduce	Impact	Recommendation
SQL Injection	Unsanitized input in login form	Enter ' OR 1=1-- in username field	Authentication bypass	Use parameterized queries
⚠️ Disclaimer

This project is for educational purposes only.
Do NOT use these techniques on real-world applications without proper authorization.

📚 References

OWASP Testing Guide

Burp Suite Docs

DVWA GitHub

OWASP Juice Shop
