# 🔍 Detection Analysis

## 🔗 Attack Chain Correlation

The following sequence was observed:

1. SSH brute force attempts detected (Rule 5763)
2. Successful login (Rule 5715 / 5901)
3. Session established (Rule 5501 / 5902)
4. Privilege escalation via sudo (Rule 5402 / 5405)
5. User account modification (Rule 5503)
6. File modification detected (Rule 550)
7. File deletion detected (Rule 553)

## 🚨 Conclusion

This sequence indicates a complete attack lifecycle:

* Initial Access (Brute Force & SSH Login)
* Execution (Interactive Session)
* Privilege Escalation (sudo)
* Persistence (User Modification & File Changes)
* Defense Evasion (File Deletion / Log Tampering)
  
👉 This behavior strongly indicates a compromised system with post-exploitation activity.
