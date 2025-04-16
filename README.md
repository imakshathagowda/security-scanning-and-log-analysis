# 🔍 Security Scanning and Log Analysis

## 📄 Overview
This project focuses on core penetration testing and security analysis tasks involving:

- Scanning networks to identify vulnerabilities
- Performing in-depth system enumeration using Nmap
- Analyzing web server logs to detect and respond to potential attacks

Each task mimics real-world scenarios in ethical hacking and red teaming environments, with practical mitigation strategies included.

---

## 🎯 Objective
The objective of this project is to demonstrate fundamental offensive security skills through Nmap scanning techniques and log analysis. The project showcases real-world applications such as half-open scanning, OS detection, and detection of web-based attacks like SQL injection, XSS, and directory traversal. It provides command examples, outputs, and defensive recommendations.

---

## ✅ Tasks Performed

### 🔹 Task 1: Half-Open (SYN) Port Scan
Stealth scan using Nmap to detect open TCP ports.

📄 [Details](./Task1_Scan/README.md)

---

### 🔹 Task 2: Aggressive Nmap Scan (OS & Version Detection)
Performed deep scan to gather OS details, services, and traceroute.

📄 [Details](./Task2_Aggressive/README.md)

---

### 🔹 Task 3: Web Log Attack Analysis
Analyzed HTTP logs to detect DOM XSS, SQL Injection, and Directory Traversal.

📄 [Details](./Task3_LogAnalysis/README.md)

---

## 🔧 Skills Applied

- Nmap scanning (SYN, Aggressive)
- OS & Service fingerprinting
- Manual web log inspection
- Threat classification (XSS, SQLi, Traversal)
- Report writing and documentation

---

## 🖥️ Lab Setup

- OS: Kali Linux 2024.1
- Target VM: Metasploitable2 / DVWA / Custom Web Server
- Tools: Nmap, grep, bash utilities

## 📂 Project Files

| File/Folder               | Description                                 |
|---------------------------|---------------------------------------------|
| `security_scan_report.pdf` | Original report with answers and findings   |
| `Task1_Scan/`             | Nmap SYN scan + result                      |
| `Task2_Aggressive/`       | Aggressive scan with OS detection           |
| `Task3_LogAnalysis/`      | Log samples and attack analysis             |
| `README.md`               | Main documentation                          |

---

## 👩‍💻 Author

**Akshatha K**  
_Penetration Tester | GitHub: [@imakshathagowda](https://github.com/imakshathagowda_

---

## 🏷️ Tags
`Nmap` `Security Scanning` `Log Analysis` `XSS` `SQL Injection` `Directory Traversal` `Penetration Testing` `Network Security`

---

## 🧾 Conclusion

This project demonstrates real-world offensive security skills, including:
- Stealth and aggressive scanning techniques with Nmap
- Log analysis to identify and classify common web attacks
- Understanding of how attackers attempt to bypass security controls

Each task simulates a stage in the penetration testing lifecycle, helping build both technical and analytical skills.

