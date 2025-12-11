
# Vulnerability Scanning – Overview

## Target & Environment
- **Target Machine:** Metasploitable 2  
- **Attacker Machine:** Kali Linux  
- **Network:** Private isolated lab environment  
- **Purpose:** Safe vulnerability scanning practice  
- **Tools Used:** Nmap, Nikto, OpenVAS, Wappalyzer  

---

## Scope of Assessment
The scanning activity was limited to:
- Host discovery  
- Port enumeration  
- Service and version detection  
- Web vulnerability scanning (Port 80 & 8180)  
- Technology fingerprinting  
- No exploitation beyond basic validation  

Everything was performed within an approved **local VAPT lab scope**.

---

## Summary
A structured vulnerability scan was executed against the Metasploitable 2 target using Kali Linux. The scans identified multiple open ports, outdated services, and web vulnerabilities. Service banners, web server fingerprints, and potential CVEs were collected for further analysis. This phase focused purely on enumeration to prepare for later exploitation steps. All findings are documented with screenshots and scan outputs inside this directory.
