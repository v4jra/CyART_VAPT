# Week 4 – Advanced Vulnerability Assessment & Penetration Testing (VAPT)

## Overview
This repository documents **Week 4 of my Cybersecurity Internship**, focused on **advanced penetration testing and vulnerability assessment**. The week involved hands-on exploitation of vulnerable systems, API security testing, privilege escalation, network protocol attacks, mobile application security testing, and a full end-to-end VAPT capstone project.

All testing activities were conducted in **authorized lab environments** such as VulnHub, Metasploitable2, DVWA, and OWASP Juice Shop, following industry-standard methodologies.

---

## Scope of Work
The scope of this week included:

- Advanced exploitation and exploit chaining
- API security testing (REST & GraphQL)
- Privilege escalation and persistence
- Network protocol attacks (MITM)
- Mobile application security testing
- Full VAPT simulation using PTES

## Detailed scope is available in:
- **scope/scope.md**

---

## Tools & Technologies

### Kali Linux Tools
- Metasploit Framework
- Nmap
- Burp Suite
- sqlmap
- LinPEAS
- Responder
- Ettercap
- mitmproxy
- Wireshark
- Ghidra

### Mobile Security Tools
- MobSF
- Frida
- Drozer

### Containerization
- Docker (used for MobSF deployment)

Detailed setup instructions:
- **tools-setup/**

---

## Labs Performed

| Lab No. | Lab Name | Description |
|------|--------|-------------|
| 1 | Advanced Exploitation | Exploit chaining, PoCs, ASLR concepts |
| 2 | API Security Testing | OWASP API Top 10, GraphQL testing |
| 3 | Privilege Escalation | SUID, LinPEAS, persistence |
| 4 | Network Protocol Attacks | MITM, SMB, ARP spoofing |
| 5 | Mobile App Security | APK static & dynamic analysis |
| 6 | Capstone VAPT | Full PTES-based penetration test |

Detailed lab documentation:
- **labs/**

---

## Evidence Collection
All screenshots, command outputs, and proof-of-exploitation images are stored **lab-wise** in the evidence directory.
```
evidence/
├── lab-1/
├── lab-2/
├── lab-3/
├── lab-4/
├── lab-5/
└── lab-6/
```

Each folder contains **only real lab artifacts** captured during testing.

---

## Mobile Security Reports (MobSF)
MobSF-generated reports for Android application analysis are attached separately due to size and detail.
```
mobsf-reports/
├── mobsf-static-analysis.pdf
└── mobsf-dynamic-analysis.pdf
```

> Note: The MobSF PDFs contain **complete static and dynamic analysis**, including permissions, API usage, insecure storage, runtime behavior, and traffic analysis.

---

## Final Reports
Professional reports prepared as part of this week include:
reports/
└── week-4.pdf

These reports follow **PTES reporting standards** and include both **technical and non-technical summaries**.

---

## Key Learnings
- Real-world exploitation techniques
- API & GraphQL security testing
- Privilege escalation methodologies
- MITM attack execution and detection
- Mobile application attack surface analysis
- Professional VAPT documentation & reporting

---

## Disclaimer
All activities in this repository were conducted **strictly in controlled lab environments** for **educational purposes only**. No unauthorized systems were targeted.

---

## References
References and learning resources:
- **references/references.md**


---

## Author
VAPT Intern  
Week 4 - Advanced VAPT



