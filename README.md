# 🛡️ Wazuh Linux Attack Detection Lab

![Wazuh](https://img.shields.io/badge/SIEM-Wazuh-blue)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-green)
![Attack](https://img.shields.io/badge/Attack-SSH%20Brute%20Force-red)
![Status](https://img.shields.io/badge/Status-Completed-success)

This project demonstrates end-to-end attack simulation and detection using Wazuh SIEM in a SOC environment.
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



## 🔥 Attack Scenarios Covered

- SSH Brute Force Attack
- Successful Login Detection
- Privilege Escalation (sudo)
- Persistence via User Creation
- SSH Backdoor (authorized_keys)
- Log Tampering Detection
- File Integrity Monitoring (FIM)

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
