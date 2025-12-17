# Full-Cycle Vulnerability Assessment & Penetration Testing (VAPT)

## Overview
This repository contains a full-cycle Vulnerability Assessment and Penetration Testing (VAPT) project performed in a controlled lab environment. The project demonstrates hands-on experience in web application security testing, exploit chaining, post-exploitation, evidence handling, and professional reporting.

---

## Scope of Assessment

### Included
- Web application security testing (OWASP Top 10)
- Network and service enumeration
- Chained exploitation
- Post-exploitation and evidence collection
- Reporting and risk analysis

### Excluded
- Denial of Service (DoS)
- Social engineering attacks

---

## Target & Attacker Environment

| Role | Details |
|-----|--------|
| Attacker | Kali Linux |
| Targets | DVWA, Metasploitable2, DC-01 |
| Network | Isolated virtual lab |

---

## Tools Used

- Nmap
- OpenVAS
- Burp Suite
- OWASP ZAP
- sqlmap
- Metasploit Framework
- Wireshark

---

## Key Vulnerabilities Identified

| Vulnerability | Severity | CVSS |
|--------------|----------|------|
| SQL Injection | Critical | 9.1 |
| CSRF | High | 8.0 |
| XXE | High | 7.5 |
| Information Disclosure | Medium | 5.3 |
| Remote Login via SSH | High | 7.4 |

---

## Project Structure
- **reports/** – Final professional VAPT report (PDF)
- **evidence/** – Screenshots, network captures, and hashes
- **diagrams/** – Attack path and chained exploitation diagrams

---

## Disclaimer
All testing was conducted on intentionally vulnerable systems in an isolated environment for educational and professional training purposes only.

---

## About 
**ROLE:** VAPT Analyst / Security Intern

### Reffrences
**Vulnhub lab:** https://www.vulnhub.com/entry/dc-1,292/
**Metasploitabe 2:** https://www.vulnhub.com/entry/metasploitable-2,29/
**Post exploit:** https://gtfobins.github.io/
**exploit DB:** https://www.exploit-db.com/
