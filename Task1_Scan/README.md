# 🔹 Task 1: Half-Open (SYN) Port Scan

## 🧾 Objective
Perform a stealth scan using Nmap's SYN scan mode to identify open TCP ports on the target system.

## 🔧 Commands Used

```bash
# Basic SYN scan
sudo nmap -sS TARGET_IP

# Full port scan with faster timing and output saved to file
sudo nmap -sS -p- -T4 -oN Result_scan.txt TARGET_IP
```

### 🔍 Explanation
- `-sS`: TCP SYN (half-open) scan  
- `-p-`: Scans all 65535 ports  
- `-T4`: Faster timing for quicker scanning  
- `-oN`: Outputs result to a readable text file

## 📤 Sample Output

```text
PORT     STATE SERVICE
22/tcp   open  ssh
80/tcp   open  http
443/tcp  open  https
3306/tcp open  mysql
```

## ✅ Use Case

This scan is useful for **stealthy reconnaissance**, especially when testing:

- Network security controls
- Firewall evasion techniques
- Detection capabilities of IDS/IPS systems
