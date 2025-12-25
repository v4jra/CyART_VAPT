# Environment Setup & Tool Installation Guide
*(Week-4 VAPT Internship)*

---

## Overview
This document explains the complete environment and tool setup used during the Week-4 Vulnerability Assessment & Penetration Testing (VAPT) internship project.  
All steps are written in a simple, step-by-step manner so that even beginners can easily reproduce the lab environment.

---

## 1. Operating System Setup

### Attacker Machine
- **OS:** Kali Linux (Latest)
- **Role:** Penetration testing and exploitation

### Target Machines
- VulnHub Machines
- Metasploitable 2
- Android APKs (Offline Analysis)

---

## 2. Virtualization & Network Configuration

### VirtualBox Setup
1. Install VirtualBox
2. Create Host-Only Network:
   - VirtualBox → File → Tools → Network Manager
3. Attach both Kali and target VMs to the same network
4. Verify IP addresses:
```
ip a
```

## 3. Core Tools (Kali Linux)
- Most tools come pre-installed on Kali Linux.

```
sudo apt update
sudo apt install -y \
metasploit-framework \
nmap \
burpsuite \
sqlmap \
wireshark \
ettercap-graphical \
responder \
mitmproxy \
ghidra \
docker.io \
postman
```

## 4. Metasploit Setup
```
sudo systemctl start postgresql
msfconsole
```

### Used for:
- Exploit chaining
- Payload delivery
- Post-exploitation

## 5. API Security Testing Tools
Burp Suite

**Browser Proxy Configuration:**
- IP: 127.0.0.1
- Port: 8080

**Used for:**
- API enumeration
- Token manipulation
- GraphQL testing

**postman**

Used for:
- Manual API requests
- GraphQL fuzzing
- Authorization testing

## 6. MobSF Setup (Docker Based – Recommended)
```
Install & Start Docker
sudo systemctl start docker
sudo systemctl enable docker
```

**Pull MobSF Image**
```
sudo docker pull opensecurity/mobile-security-framework-mobsf:latest
```

**Run MobSF**
```
sudo docker run -it --rm -p 8000:8000 \
opensecurity/mobile-security-framework-mobsf:latest
```

### Access MobSF
Open browser:
```
http://127.0.0.1:8000
```

**Used for:**
- Static APK analysis
- Dynamic APK analysis
- Generating PDF security reports

All MobSF reports are stored separately in the reports folder.

## 7. Frida Setup (Dynamic Analysis)
- Install Frida on Kali
```
pip3 install frida-tools
frida --version
```

### Frida on Android (If Emulator/Device Available)
```
adb push frida-server /data/local/tmp/
adb shell
chmod +x frida-server
./frida-server &
````

**Used for:**
- Function hooking
- Authentication bypass
- Runtime behavior analysis

**If Android emulator is unavailable, only static analysis was performed.**

## 8. Drozer Setup (Optional)
```
sudo apt install drozer
adb forward tcp:31415 tcp:31415
```

**Used for:**
- IPC testing
- Android component exposure analysis

## 9. Ghidra Setup (Binary Analysis)
- ghidra

**Steps**
- Create new project
- Import vulnerable binary
- Analyze unsafe functions
- Understand control flow and memory usage

**Used for:**
- Binary reverse engineering
- Memory vulnerability analysis

## 10. Network Attacks Setup
**Enable IP Forwarding**
```
echo 1 | sudo tee /proc/sys/net/ipv4/ip_forward
```
**Responder**
```
sudo responder -I eth0
```

**Used for:**
- Capturing NTLM hashes
- SMB credential interception
- Ettercap (GUI Mode)
```
sudo ettercap -G
```

**Steps:**
- Sniff → Unified Sniffing
- Select interface
- Start ARP poisoning
- Monitor traffic

### mitmproxy

**Used for:**
- HTTP/HTTPS interception
- Credential capture
- Traffic inspection

## 11. Evidence Collection
Evidence captured during testing:
Screenshots
Burp requests/responses
Meterpreter sessions
Network captures
MobSF PDF reports
Stored in:
```
/evidences/
```
