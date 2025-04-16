# 🔹 Task 3: Web Server Log Attack Analysis

## 🧾 Objective
Analyze web server logs to identify suspicious activity such as SQL injection, directory traversal, and XSS attacks.

---

## 📁 Logs Analyzed

- `access_log_1.txt`: SQL Injection attempts
- `access_log_2.txt`: Directory Traversal probes
- `access_log_3.txt`: Cross-Site Scripting (XSS)

---

## 📘 Log 1 – `access_log_1.txt` (SQL Injection)

```text
192.168.1.10 - - [15/Apr/2025:14:22:01 +0000] "GET /index.php?id=1' OR '1'='1 HTTP/1.1" 200 5320
192.168.1.11 - - [15/Apr/2025:14:23:45 +0000] "GET /product.php?item=5'-- HTTP/1.1" 200 4890
```

### 🔎 Attack Pattern

- SQL Injection via query parameters  
- Use of `' OR '1'='1` and comment-style `--` to bypass logic

### ✅ Use Case

- Detects attempts to exploit insecure database queries
- Useful for strengthening input sanitization and database query handling

---

## 📘 Log 2 – `access_log_2.txt` (Directory Traversal)

```text
192.168.1.20 - - [15/Apr/2025:14:25:32 +0000] "GET /../../../etc/passwd HTTP/1.1" 400 1220
192.168.1.21 - - [15/Apr/2025:14:26:07 +0000] "GET /..%2f..%2f..%2fetc%2fshadow HTTP/1.1" 403 1305
```

### 🔎 Attack Pattern

- Attempt to access restricted files outside web root  
- Encoded versions (`%2f`) used to bypass naive filters

### ✅ Use Case

- Helps detect weak path validation
- Suggests need for hardening file access policies

---

## 📘 Log 3 – `access_log_3.txt` (Cross-Site Scripting - XSS)

```text
192.168.1.12 - - [15/Apr/2025:14:24:55 +0000] "GET /search.php?q=<script>alert(1)</script> HTTP/1.1" 200 5430
192.168.1.13 - - [15/Apr/2025:14:27:19 +0000] "GET /profile?bio=%3Cscript%3Ealert('XSS')%3C%2Fscript%3E HTTP/1.1" 200 5100
```

### 🔎 Attack Pattern

- Injection of `<script>` tags directly or through encoded payloads  
- Targeting unsanitized search or profile inputs

### ✅ Use Case

- Crucial for identifying XSS risks
- Highlights need for strong input/output encoding in web apps

---

## 🧠 Summary

Log analysis revealed:

- SQLi, directory traversal, and XSS attempts
- Common attacker behavior and IP patterns
- Areas where web apps need stronger input validation and filtering

---

## 🛡️ Recommendation

- Implement WAF rules for known attack signatures  
- Sanitize all user input  
- Monitor logs regularly for anomalies
