# Lab 3 – Privilege Escalation & Persistence

## Objective
To escalate privileges on a compromised system and establish persistence.

---

## Scope
- Local enumeration
- Privilege escalation
- Persistence mechanisms

---

## Tools Used
- Meterpreter
- LinPEAS
- PowerSploit

---

## Enumeration
System enumeration using LinPEAS identified misconfigured SUID binaries and weak permissions.

---

## Exploitation

| Task ID | Technique | Target | Status | Outcome |
|-------|-----------|--------|--------|--------|
| 010 | SUID Exploit | VulnHub VM | Success | Root Access |

---

## Persistence
A cron-based persistence mechanism was configured to maintain access after reboot.

---

## Impact
Privilege escalation allowed complete system compromise.

---

## Recommendations
- Remove unnecessary SUID binaries
- Apply least privilege principles
- Monitor cron jobs and scheduled tasks
