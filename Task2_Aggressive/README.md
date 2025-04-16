# 🔹 Task 2: Aggressive Nmap Scan (OS & Version Detection)

## 🧾 Objective
Perform an aggressive scan with Nmap to deeply fingerprint a system, gathering OS, services, and traceroute information.

## 🔧 Commands Used

```bash
# Aggressive scan with default scripts, OS and version detection
sudo nmap -A TARGET_IP

# Same scan with output saved to a file
sudo nmap -A -oN aggressive_scan.txt TARGET_IP
```

## 🔍 Explanation of `-A` Flag

- OS detection  
- Version detection  
- Default script scanning  
- Traceroute mapping

## 📤 Sample Output

```text
PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 7.2p2
80/tcp   open  http    Apache httpd 2.4.18
443/tcp  open  ssl/http Apache httpd 2.4.18
OS details: Linux 3.10 - 4.11
```

## ✅ Use Case

Ideal during **enumeration** to gather **in-depth technical data** about the target system, such as:

- OS versioning
- Running services
- Possible vulnerabilities
- Network path insights (via traceroute)
