# Arris BGW210 Router — IoT Security Assessment

A professional security assessment conducted against an Arris BGW210 Series router following the **PTES (Penetration Testing Execution Standard)** methodology.

> Assessment conducted on a personally owned device on a personally owned network. All device identifiers have been sanitized.

---

## Findings Summary

| Severity | Count | Finding |
|----------|-------|---------|
| CRITICAL | 2 | EOL PHP 5.2.17 (15 years outdated) + EOL mini_httpd 1.19 (22 years outdated) |
| HIGH | 1 | Unauthenticated Directory Listing on 4 Web Directories |
| MEDIUM | 2 | Session Storage Failure (/tmp Full) + Verbose Header Disclosure |
| LOW | 1 | No Rate Limiting on Login Endpoint |

**Key Finding:** Device runs PHP 5.2.17 (EOL 2011) and mini_httpd 1.19 (released 2004) — 100+ unpatched CVEs with no vendor patch path available. CVSS Score: 9.8

---

## Methodology

1. **Reconnaissance** — Host discovery, port scanning, OS and service fingerprinting
2. **Scanning & Enumeration** — Full port scan, HTTP analysis, directory enumeration, backup file checks
3. **Vulnerability Identification** — CVE cross-referencing via searchsploit, manual exploit testing
4. **Exploitation** — CVE-2012-1823 PHP CGI RCE testing, SQL injection, PHP wrapper attacks, session attacks
5. **Reporting** — CVSS v3.1 scoring, business impact analysis, prioritized remediation

---

## Tools Used

- Nmap
- curl
- searchsploit
- Gobuster
- PowerShell
- Custom Python scripts

---

## Skills Demonstrated

- Network service enumeration and fingerprinting
- CVE research and exploit cross-referencing (CVE-2012-1823, CVE-2010-4645)
- SQL injection testing (12 payloads)
- PHP CGI exploitation techniques
- Session attack vectors
- CVSS v3.1 scoring and risk assessment
- Business impact and compliance mapping (PCI-DSS, NIST, ISO 27001)
- Professional penetration testing report writing

---

## Report

📄 [IoT_Security_Assessment_Arris_Router.pdf](IoT_Security_Assessment_Arris_Router.pdf)

---

## Author

**Giovanni Moore**
[LinkedIn](https://www.linkedin.com/in/giovanni-moore-408589362/) | [GitHub](https://github.com/Truxnks)
