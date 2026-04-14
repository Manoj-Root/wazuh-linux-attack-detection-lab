# 🛡️ Wazuh Linux Attack Detection Lab

> Simulated and detected a full Linux attack chain using Wazuh SIEM in a SOC lab environment.

---

## 📌 Overview

This project demonstrates a **real-world SOC (Security Operations Center) scenario** where multiple attack techniques were simulated on a Linux system and detected using **Wazuh SIEM**.

The objective was to understand how attackers operate and how their activities can be monitored, correlated, and analyzed from a defender’s perspective.

---

## 🎯 Lab Objectives

- Simulate real-world attack scenarios on Linux
- Monitor logs using Wazuh SIEM
- Perform log analysis and event correlation
- Map detected activities to MITRE ATT&CK framework

---

## 🧪 Attack Scenarios Simulated

### 🔴 1. SSH Brute Force Attack (T1110)
- Multiple failed login attempts detected
- Wazuh rules triggered for authentication failures

<img src="screenshots/ssh-brute-force.png" width="800"/>

---

### 🟢 2. Successful Login (Initial Access)
- Attacker gained access after repeated attempts
- Authentication success logs captured

<img src="screenshots/login-success.png" width="800"/>

---

### 🔥 3. Privilege Escalation (T1548)
- Executed `sudo su` to gain root access
- Detected via Wazuh logs

<img src="screenshots/privilege-escalation.png" width="800"/>

---

### 👤 4. Persistence via User Creation (T1136)
- Created a new user (`hacker`)
- Password set for persistence

<img src="screenshots/user-creation.png" width="800"/>

---

### 🔑 5. SSH Backdoor (authorized_keys)
- Added SSH key for persistent access
- Detected using file monitoring

<img src="screenshots/ssh-backdoor.png" width="800"/>

---

### 🧹 6. Log Tampering (T1070)
- Cleared `/var/log/auth.log` to remove traces
- Demonstrates defense evasion technique

<img src="screenshots/log-tampering.png" width="800"/>

---

### 🌐 7. Network Activity Detection
- Detected new listening ports
- Possible tunneling/backdoor activity observed

<img src="screenshots/network-activity.png" width="800"/>

---

## 📊 Detection & Analysis

All attack activities were:

- Detected using Wazuh SIEM
- Correlated across multiple logs
- Analyzed using both dashboard and raw log queries (`wazuh-alerts-*`)

---

## 🧠 MITRE ATT&CK Mapping

| Technique | ID |
|----------|----|
| Brute Force | T1110 |
| Privilege Escalation | T1548 |
| Create Account | T1136 |
| Defense Evasion | T1070 |

---

## 🔍 Detection Logic

- Multiple failed login attempts followed by a successful login indicate a brute-force attack
- Privilege escalation activity (`sudo su`) indicates elevated access
- Creation of new users suggests persistence
- Log clearing indicates defense evasion
- File changes (authorized_keys) indicate backdoor access

---

## ⚙️ Tools Used

- Wazuh SIEM  
- Kali Linux  
- OpenSearch (Discover for log analysis)

---

## 🚀 Key Outcomes

- Built a real-world SOC lab environment  
- Simulated full attack lifecycle  
- Performed log correlation and analysis  
- Gained hands-on experience in threat detection  

---

## 📸 Screenshots

All screenshots are available in the `screenshots/` folder.

---

## 🔗 Connect With Me

- 🌐 Portfolio: https://www.cybergodfather.me  
- 💼 LinkedIn: https://linkedin.com/in/manoj-root  
- 🐙 GitHub: https://github.com/Manoj-Root  

---

## ⭐ Support

If you found this project useful, consider giving it a ⭐
