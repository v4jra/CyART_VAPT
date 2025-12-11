
# OpenVAS / Greenbone Vulnerability Scanning

This folder contains all vulnerability scanning results performed using **OpenVAS (Greenbone Vulnerability Manager)**.  
All reports, CVE references, and screenshots are organized for professional VAPT documentation.

---

# 1. Objective

OpenVAS was used to identify:

- **High-risk vulnerabilities**
- **Outdated software versions**
- **Misconfigurations**
- **Network-exposed services**
- **CVE-mapped security issues**

The goal of this scan is to **prioritize risk** and provide **actionable remediation steps**.

---

# 2. Scan Configuration

### Scan Type  
- Full & Fast  
- Authenticated (where possible)  
- Network discovery enabled  
- Default scripts + CVE feed update

### Target Machines  
- **Metasploitable 2**

### Feed Update Command (Used if required)

```bash
sudo greenbone-feed-sync
```

### OpenVAS findings Table Format
| Vulnerability Name | Host | Port | Threat | Severity | CVSS | Description |
|--------------------|------|-------|---------|----------|--------|-------------|
| Distributed Ruby (dRuby/DRb) Multiple RCE Vulnerabilities | 192.168.56.101 | 8787/tcp | Critical | 10.0 | 10.0 | Remote RCE via instance_eval/syscall due to unsafe DRb exposure. |
| Possible Backdoor: Ingreslock | 192.168.56.101 | 1524/tcp | Critical | 10.0 | 10.0 | System responds to raw `id;` command, indicates backdoor access. |
| Operating System (OS) End of Life (EOL) Detection | 192.168.56.101 | general/tcp | Critical | 10.0 | 10.0 | Host runs Ubuntu 8.04, long past EOL, vulnerable to many issues. |
| TWiki XSS and Command Execution Vulnerabilities | 192.168.56.101 | 80/tcp | Critical | 10.0 | 10.0 | XSS + eval injection enabling remote Perl code execution. |
| The rexec service is running | 192.168.56.101 | 512/tcp | Critical | 10.0 | 10.0 | rexec sends credentials unencrypted; remote command execution risk. |
| MySQL / MariaDB Default Credentials | 192.168.56.101 | 3306/tcp | Critical | 9.8 | 9.8 | MySQL root account accessible with empty password. |
| PHP < 5.3.13 / 5.4.x < 5.4.3 Multiple Vulnerabilities | 192.168.56.101 | 80/tcp | Critical | 9.8 | 9.8 | CGI vulnerability (CVE-2012-1823) allows arbitrary PHP execution. |
| vsftpd Compromised Source Packages Backdoor | 192.168.56.101 | 6200/tcp | Critical | 9.8 | 9.8 | Known vsftpd 2.3.4 backdoor allowing shell access via backdoor trigger. |
