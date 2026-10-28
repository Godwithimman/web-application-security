# 🛡️ Offensive Security & Web Pentesting Labs

![Focus](https://img.shields.io/badge/Focus-Web_App_Security-red?style=for-the-badge)
![OS](https://img.shields.io/badge/OS-Kali_Linux-blue?style=for-the-badge&logo=kalilinux)
![Tools](https://img.shields.io/badge/Tools-Burp_Suite-orange?style=for-the-badge&logo=burpsuite)
![Status](https://img.shields.io/badge/Status-Active_Learning-brightgreen?style=for-the-badge)

Welcome to my personal cybersecurity learning repository! This repo contains structured notes, payload cheatsheets, and step-by-step lab writeups covering various web application vulnerabilities and offensive security concepts.

---

## 📌 Repository Index & Progress

| Vulnerability Category | Core Concepts Covered | Key Lab Environments | Current Status |
| :--- | :--- | :---: | :---: |
| **SQL Injection (SQLi)** | Union-based, Error-based, Blind SQLi | DVWA, PortSwigger | 🟢 Completed |
| **Cross-Site Scripting (XSS)** | Reflected, Stored, DOM-based | PortSwigger Academy | 🟡 In Progress |
| **CSRF** | Token Bypass, SameSite Cookie Testing | Custom Labs | 🔴 Planned |

---

## 🛠️ Lab Setup & Tooling

- **Operating System:** Kali Linux (VMware Workstation)
- **Interception Proxy:** Burp Suite Community Edition / FoxyProxy
- **Testing Targets:** 
  - Damn Vulnerable Web Application (DVWA)
  - PortSwigger Web Security Academy
- **Documentation:** VS Code (Markdown)

---

## 📑 Lab Writeups & Notes

### 1. SQL Injection
- 📂 [SQLi Fundamentals & Methodology](./SQL-Injection/README.md)
- 📝 [DVWA SQL Injection (Low to High)](./SQL-Injection/Labs/DVWA-SQLi-Lab.md)
- 📝 [PortSwigger: SQLi Union Attacks](./SQL-Injection/Labs/PortSwigger-Labs.md)

### 2. Cross-Site Scripting (XSS)
- 📂 [XSS Payloads & Context Analysis](./XSS/README.md)
- 📝 [PortSwigger: Reflected XSS into HTML Context](./XSS/Labs/PortSwigger-XSS.md)

---

## 🎯 Learning Roadmap & Tasks

- [x] Master SQLi Column Enumeration & Union Payloads
- [x] Extract Database Versions (Oracle `v$version`, MySQL `@@version`)
- [ ] Complete PortSwigger Stored XSS Labs
- [ ] Build automated CSRF PoC generator script in HTML/JS

---

## 💡 Quick Payload Reference

<details>
<summary><b>Click to expand SQLi Version Extraction Payloads</b></summary>

```sql
-- Oracle Database
' UNION SELECT BANNER, NULL FROM v$version--

-- Microsoft / MySQL
' UNION SELECT @@version, NULL--

-- PostgreSQL
' UNION SELECT version(), NULL--
