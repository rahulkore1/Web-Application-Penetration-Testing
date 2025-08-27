
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
