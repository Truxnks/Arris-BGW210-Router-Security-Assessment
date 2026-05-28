Arris BGW210 Router — IoT Security Assessment
A professional security assessment conducted against an Arris BGW210 Series router following the PTES (Penetration Testing Execution Standard) methodology with MITRE ATT&CK technique mapping.

Assessment conducted on a personally owned device on a personally owned network. All device identifiers have been sanitized.


Findings Summary
SeverityCountFindingCRITICAL2EOL PHP 5.2.17 (15 years outdated) · EOL mini_httpd 1.19 (22 years outdated)HIGH1Unauthenticated Directory Listing on 4 Web DirectoriesMEDIUM2Session Storage Failure (/tmp Full) · Verbose Header DisclosureLOW1No Rate Limiting on Login Endpoint
Key Finding: Device runs PHP 5.2.17 (EOL 2011) and mini_httpd 1.19 (released 2004) — extensive catalogued CVEs with no vendor patch path available. CVSS Score: 9.8

MITRE ATT&CK Coverage
TechniqueNameTacticFindingT1190Exploit Public-Facing ApplicationInitial AccessEOL PHP + mini_httpdT1203Exploitation for Client ExecutionExecutionCVE-2012-1823T1083File and Directory DiscoveryDiscoveryDirectory ListingT1592Gather Victim Host InformationReconnaissanceHeader DisclosureT1499Endpoint Denial of ServiceImpactSession FailureT1110Brute ForceCredential AccessNo Rate Limiting

Methodology

Reconnaissance — Host discovery, port scanning, OS and service fingerprinting
Scanning & Enumeration — Full port scan, HTTP analysis, directory enumeration, backup file checks
Vulnerability Identification — CVE cross-referencing, manual exploit testing, injection testing
Exploitation — CVE-2012-1823 PHP CGI RCE, SQL injection (12 payloads), PHP wrappers, session attacks
Post-Exploitation — Scoped impact assessment
Reporting — CVSS v3.1 scoring, MITRE ATT&CK mapping, risk matrix, business impact, remediation


Attack Chains Tested

CVE-2012-1823 PHP CGI argument injection RCE
SQL injection across 12 payloads
PHP wrapper attacks (php://filter, expect://)
Default credential enumeration (18 combinations)
Session hijacking and fixation
Directory traversal (9 payloads)
HTTP method abuse (PUT, DELETE, TRACE)
Backup and config file enumeration


Tools Used

Nmap
curl
searchsploit
Gobuster
PowerShell
Custom Python scripts


Skills Demonstrated

Network service enumeration and fingerprinting
CVE research and exploit cross-referencing
SQL injection and PHP CGI exploitation techniques
Session attack vectors
CVSS v3.1 scoring with justification
MITRE ATT&CK technique mapping
Likelihood vs impact risk matrix
Business impact and compliance mapping (PCI-DSS, NIST SP 800-53, ISO 27001)
Professional penetration testing report writing


Report
📄 IoT_Security_Assessment_Arris_Router_v2.pdf

Author
Giovanni Moore
LinkedIn | GitHub
