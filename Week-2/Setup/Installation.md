# Environment Setup Guide

This document explains the complete setup required for executing the CYART VAPT (Vulnerability Assessment & Penetration Testing) labs.  
It covers the installation and configuration of:

- **Metasploitable 2** 
- **DVWA (via Docker)** 
- **OpenVAS (Greenbone Community Edition)**
- **Burp Suite**
- **Kali Linux Essential Tools**

---

## 1. Metasploitable 2 Setup (GUI-Based Installation)

Metasploitable 2 is an intentionally vulnerable Linux machine used for VAPT practice.

### **Steps:**
1. Download Metasploitable 2 ISO/VM → (Rapid7 official website)
2. Import it into **VirtualBox** or **VMware**.
3. Start the VM.
4. Default credentials:

```
username: msfadmin
password: msfadmin
```

5. After login → retrieve the IP:
6. Ensure it is reachable:


### **Metasploitable2 screenshot:**
- ![Step 1](CyART_VAPT/Week-2/Setup/ip_a.png)

---

## 2. DVWA Setup Using Docker

DVWA (Damn Vulnerable Web Application) is used for web exploitation and vulnerability testing.

### **Prerequisites:**
- Docker installed on Kali/Linux

### **Run DVWA using Docker:**
```
sudo docker run --name dvwa -p 9988:80 vulnerables/web-dvwa
```

### **After running:**
- Open browser  
- **http://localhost:9988**
- Complete DVWA setup page
- Set security level to "Low"

### **screenshots:**
- ![Step 2](CyART_VAPT/Week-2/Setup/home.png)

---

## 3. OpenVAS (Greenbone CE) Setup

OpenVAS is used for vulnerability scanning.

### **Installation (Kali Linux):**
```
- sudo apt update
- sudo apt install openvas -y
- sudo gvm-setup
```

### **Start OpenVAS Services:**
```
sudo gvm-start
```

### **Access Web Interface:**
```
https://127.0.0.1:9392/
```

### **Login credentials are shown after:**
```
sudo gvm-setup
```

### **Important Setup Steps:**
- Update vulnerability feed
- Create new scan target
- Run “Full and Fast” scan
- Export PDF results

### **screenshots:**
- ![Step 3](CyART_VAPT/Week-2/Setup/home_opeb.png)
- ![Step 2](CyART_VAPT/Week-2/Setup/success.png)

---

## 4. Burp Suite Installation & Configuration

Burp Suite is used for web application penetration testing.

### **Launch Burp Suite on Kali:**
burpsuite

### **Initial Setup:**
1. Select **Temporary Project**  
2. Choose **Burp Defaults**  
3. Go to **Proxy > Intercept**  
4. Ensure “Intercept is ON”

### **Configure Browser (FoxyProxy recommended):**
- Set Proxy: **127.0.0.1:8080**
- Disable HTTPS certificate errors OR import Burp CA certificate.

### **Test Proxy Working:**
- With proxy ON, open:
**http://burp**

---

## 5. Essential Tools Installed in Kali Linux

### **Networking Tools**
```
sudo apt install net-tools arp-scan
```

### **Subdomain / Recon Tools**
```
sudo apt install sublist3r amass
```

### **Port Scanning**
```
sudo apt install nmap
```
### **Exploit Tools**
(Already available in Kali)
- Metasploit  
- sqlmap  
- Hydra  
- Nikto  

---

## Summary of Environment

| Component          | Status | Purpose                                |
|-------------------|--------|-----------------------------------------|
| Kali Linux        | Ready  | Main attacker machine                   |
| Metasploitable 2  | Ready  | Vulnerable target for exploitation      |
| DVWA (Docker)     | Ready  | Web exploitation practice               |
| OpenVAS (GVM)     | Ready  | Automated vulnerability scanning        |
| Burp Suite        | Ready  | Manual web testing & interception       |

---

## Notes
- All tests must stay inside your **local lab environment** only.  
- Do NOT scan any external IP without permission.  

