# Arris BGW210 Router — IoT Security Assessment
 
A professional security assessment conducted against an Arris BGW210 Series router following the **PTES (Penetration Testing Execution Standard)** methodology with **MITRE ATT&CK** technique mapping.
 
> Assessment conducted on a personally owned device on a personally owned network. All device identifiers have been sanitized.
 
---
 
## Findings Summary
 
| Severity | Count | Finding |
|----------|-------|---------|
| CRITICAL | 2 | EOL PHP 5.2.17 (15 years outdated) · EOL mini_httpd 1.19 (22 years outdated) |
| HIGH | 1 | Unauthenticated Directory Listing on 4 Web Directories |
| MEDIUM | 2 | Session Storage Failure (/tmp Full) · Verbose Header Disclosure |
| LOW | 1 | No Rate Limiting on Login Endpoint |
 
**Key Finding:** Device runs PHP 5.2.17 (EOL 2011) and mini_httpd 1.19 (released 2004) — extensive catalogued CVEs with no vendor patch path available. CVSS Score: 9.8
 
---
 
## MITRE ATT&CK Coverage
 
| Technique | Name | Tactic | Finding |
|-----------|------|--------|---------|
| T1190 | Exploit Public-Facing Application | Initial Access | EOL PHP + mini_httpd |
| T1203 | Exploitation for Client Execution | Execution | CVE-2012-1823 |
| T1083 | File and Directory Discovery | Discovery | Directory Listing |
| T1592 | Gather Victim Host Information | Reconnaissance | Header Disclosure |
| T1499 | Endpoint Denial of Service | Impact | Session Failure |
| T1110 | Brute Force | Credential Access | No Rate Limiting |
 
---
 
## Methodology
 
1. **Reconnaissance** — Host discovery, port scanning, OS and service fingerprinting
2. **Scanning & Enumeration** — Full port scan, HTTP analysis, directory enumeration, backup file checks
3. **Vulnerability Identification** — CVE cross-referencing, manual exploit testing, injection testing
4. **Exploitation** — CVE-2012-1823 PHP CGI RCE, SQL injection (12 payloads), PHP wrappers, session attacks
5. **Post-Exploitation** — Scoped impact assessment
6. **Reporting** — CVSS v3.1 scoring, MITRE ATT&CK mapping, risk matrix, business impact, remediation
---
 
## Attack Chains Tested
 
- CVE-2012-1823 PHP CGI argument injection RCE
- SQL injection across 12 payloads
- PHP wrapper attacks (php://filter, expect://)
- Default credential enumeration (18 combinations)
- Session hijacking and fixation
- Directory traversal (9 payloads)
- HTTP method abuse (PUT, DELETE, TRACE)
- Backup and config file enumeration
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
- CVE research and exploit cross-referencing
- SQL injection and PHP CGI exploitation techniques
- Session attack vectors
- CVSS v3.1 scoring with justification
- MITRE ATT&CK technique mapping
- Likelihood vs impact risk matrix
- Business impact and compliance mapping (PCI-DSS, NIST SP 800-53, ISO 27001)
- Professional penetration testing report writing
---
 
## Report
 
📄 [IoT_Security_Assessment_Arris_Router_v2.pdf](IoT_Security_Assessment_Arris_Router_v2.pdf)
 
---
 
## Author
 
**Giovanni Moore**
[LinkedIn](https://www.linkedin.com/in/giovanni-moore-408589362/) | [GitHub](https://github.com/Truxnks)
