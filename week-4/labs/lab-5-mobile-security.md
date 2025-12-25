# Lab 5 – Mobile Application Security Testing

## Objective
To analyze Android applications for common security weaknesses.

---

## Scope
- Static analysis
- Dynamic analysis
- Runtime manipulation

---

## Tools Used
- MobSF
- Frida
- Drozer

---

## Static Analysis

| Test ID | Vulnerability | Severity | Application |
|-------|---------------|----------|-------------|
| 016 | Insecure Storage | High | test.apk |

---

## Dynamic Analysis
Frida was used to hook application functions and bypass authentication logic.

> 📌 Note: A detailed MobSF report has been attached separately containing complete static and dynamic analysis.

---

## Impact
Identified issues could allow attackers to bypass security controls and access sensitive data.

---

## Recommendations
- Use encrypted storage
- Implement runtime integrity checks
- Apply code obfuscation
