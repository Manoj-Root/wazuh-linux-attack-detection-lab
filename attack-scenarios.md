# ⚔️ Attack Scenarios

## 🔴 SSH Brute Force

### Command Used:
ssh kali@target-ip

### Detection:
- Rule ID: 5763
- Multiple failed login attempts detected

<img src="screenshots/event-logs.png" width="800"/>

<img src="screenshots/SSH-brute-force.png" width="800"/>

---

## 🟢 Successful Login

### Detection:
- Rule ID: 5715, 5901
- Authentication success observed
<img src="screenshots/ssh-login-success.png" width="800"/>

---

## 🔥 Privilege Escalation

### Command:
sudo su

### Detection:
- Rule ID: 5402, 5405

<img src="screenshots/id-5402.png" width="800"/>

<img src="screenshots/id-5405.png" width="800"/>

---

## 👤 Persistence (User Creation)

### Command:
sudo useradd hacker
sudo passwd hacker

### Detection:
- Rule ID: 5902,5555


<img src="screenshots/new-user.png" width="800"/>

<img src="screenshots/hacker.png" width="800"/>

---


## 🔥 File Integrity Monitoring (FIM) was used to detect persistence (authorized_keys modification) and defense evasion (log tampering).


## 🔑 SSH Backdoor

### Command:
echo "key" >> ~/.ssh/authorized_keys

### Detection:
- FIM (Rule ID: 550 )

<img src="screenshots/FIM-file.png" width="800"/>


---

## 🧹 Log Tampering

### Command:
truncate -s 0 /var/log/auth.log

### Detection:
- FIM alert triggered
- MITRE: T1070

<img src="screenshots/modifies.png" width="800"/>


---

### 🌐 Network Activity Detection
- Detected new listening ports
- Possible tunneling/backdoor activity observed

<img src="screenshots/netcat.png" width="800"/>

---

## 📂 File Monitoring (FIM)

### Commands:
echo "test" > file.txt
rm file.txt

### Detection:
- Rule ID: 554 (created)
- Rule ID: 553 (deleted)

<img src="screenshots/File-add-event.png" width="800"/>

<img src="screenshots/file-deleted-event.png" width="800"/>
