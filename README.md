SOC Analyst Portfolio — Jeff Longe
About
Clinical Pharmacy Technician with 10+ years in a HIPAA-regulated environment (Texas Children's Hospital) transitioning into cybersecurity. Focused on SOC operations, threat detection, incident response, and GRC. Hands-on project experience through the Harness Projects mentorship program and active self-study via TryHackMe SOC Level 1 pathway.

Healthcare background provides direct working knowledge of regulated data environments, compliance obligations, and the real-world consequences of security failures — a differentiator for health-adjacent employers.


Certifications & Credentials
TryHackMe SOC Level 1 Pathway (in progress)
CompTIA Security+ (planned Q3 2026)


Projects
Project
Category
Tools Used
Role
Status
Web App Vulnerability Assessment
Vulnerability Assessment
Nessus, Shodan, testssl.sh, Nikto
Team contributor — ran Nessus scans
Complete
Infrastructure Vulnerability Assessment
Vulnerability Assessment
Nessus, OpenVAS, Nmap, Shodan
Individual execution + team cross-validation
Complete
IR Report Simulation
Incident Response
IR frameworks, DLP analysis, IOC documentation
Solo author
Complete
IR Plan — Simulated Client
IR Planning
NIST SP 800-61, IR lifecycle frameworks
Solo author / Policy owner
Complete
Information Security Policy
GRC / Policy
GDPR, CCPA, ISO 27001, SOC 2
Policy owner — primary author
Complete



Skills
SIEM | Splunk | Microsoft Sentinel | Wireshark | Nmap | Nessus | KQL | SPL | MITRE ATT&CK | NIST CSF | OWASP | HIPAA | DLP | Incident Response | Vulnerability Assessment | Risk Assessment | GRC


Project Details
Web App Vulnerability Assessment
Category: Vulnerability Assessment | Date: June–July 2024

External black-box vulnerability assessment of a Business Compliance Platform web application, performed as part of a 6–8 person Harness Projects team. Simulated an attacker with no internal access, credentials, or prior knowledge.

My contribution: Ran Nessus vulnerability scans; contributed to team analysis and report findings.

Tools: Nessus, Shodan, testssl.sh, Nikto

Key Findings:

Severity
Vulnerability
CVE
High
SWEET32 — session cookie theft via 64-bit block cipher exploitation
CVE-2016-2183
High
Deprecated TLS 1.0/1.1 + SHA1 hashing
—
Medium
BEAST — TLS 1.0 + 3DES cipher interception
—
Medium
LUCKY13 — CBC mode timing attack
CVE-2013-0169
Medium
BREACH — HTTPS response body decryption
CVE-2013-3587
Info
Missing security headers, sensitive data exposure, publicly accessible files
—


Root cause analysis: Four of five cryptographic vulnerabilities traced to a single root cause — the server continued supporting deprecated TLS 1.0/1.1 and 3DES ciphers. Remediating at the root (enforce TLS 1.2+ with AES-GCM) would have resolved the majority of findings simultaneously.

MITRE ATT&CK mapping:

T1557 — Adversary-in-the-Middle (SWEET32, BEAST, BREACH)
T1190 — Exploit Public-Facing Application
T1083 — File and Directory Discovery (Nikto findings)


IR Report Simulation
Category: Incident Response | Date: January–March 2025

Solo-authored incident response report for a simulated critical-severity, multi-vector attack scenario. Incident ID: IR-2025-03-003. Severity: Critical.

Scenario: Three simultaneous attack vectors detected and documented:

Vector 1 — Insider Breach (Data Exfiltration)

Employee with admin privileges exfiltrated customer PII and proprietary business data via SFTP/FTP to external devices
Detected via DLP system flagging unusual file access and transfer activity
Root cause: excessive unmonitored administrative privileges; no least-privilege enforcement
MITRE ATT&CK: T1078 (Valid Accounts), T1048 (Exfiltration Over Alternative Protocol)

Vector 2 — DDoS Attack

Botnet-driven volumetric attack on web portal and payment gateway
~6 hours of service disruption before full mitigation
Cloud-based DDoS mitigation engaged at T+5 minutes; full mitigation at T+3 hours
Root cause: absence of proactive DDoS mitigation tools, insufficient traffic filtering
MITRE ATT&CK: T1498 (Network Denial of Service)

Vector 3 — Remote Access Trojan (RAT)

Delivered via phishing email/malicious attachment
Enabled lateral movement, privilege escalation, and network reconnaissance
Spread across internal network exploiting weak segmentation and unpatched systems
Root cause: ineffective email filtering, unpatched systems
MITRE ATT&CK: T1566 (Phishing), T1021 (Remote Services), T1055 (Process Injection)

Key analyst insight: The DDoS attack functioned as adversarial noise — designed to overwhelm response capacity and mask the true objective: the insider breach and RAT deployment occurring simultaneously.

Documented deliverables: Executive summary, incident timeline with timestamped event/action table, initial compromise analysis, lateral movement and privilege escalation analysis, malware deployment analysis, forensic findings, lessons learned, IOC appendix, remediation recommendations.


IR Plan
Category: Incident Response Planning | Date: February–March 2025

Solo-authored cybersecurity Incident Response Plan for a simulated small-business client (5–7 employees). Authored as policy owner. Document designed using "developed/designed" framing — fictional client, AI-assisted scenario construction.

Plan scope: All employees, contractors, and third-party service providers. Covers unauthorized access, data breaches, phishing, ransomware, DDoS, insider threats, compromised cloud accounts (AWS/Google Workspace), unpatched vulnerability exploitation, privileged account misuse, and device loss/theft.

Framework applied: NIST SP 800-61 IR lifecycle (Preparation → Detection → Containment → Eradication → Recovery → Post-Incident)

Key design decisions documented:

Defined severity classification tiers
Established escalation paths and communication protocols
Addressed business continuity and regulatory notification obligations
Scoped for resource constraints of a small organization


Connect
LinkedIn


Infrastructure Vulnerability Assessment
Category: Vulnerability Assessment | Date: August–September 2024

External black-box vulnerability assessment of a confidential healthcare-adjacent client's publicly accessible network infrastructure. Ran all four tools independently and cross-validated findings with teammates.

My contribution: Individually ran Nessus, OpenVAS, Nmap, and Shodan; cross-validated findings with team members to confirm true positives.

Tools: Nessus, OpenVAS, Nmap, Shodan

Key Findings:

Severity
Vulnerability
CVE
Critical
OpenSSH 8.2p1 — remote code execution, 5 public exploits available
CVE-2023-38408
High
Nginx v1.18.0 — outdated web server with known vulnerabilities
—
High
Multiple security headers missing
—
Medium
Untrusted/self-signed SSL certificate
—
Medium
BREACH, SSL/TLS renegotiation DoS, missing secure cookie attribute
—


Key analyst insight: Prioritization driven by exploit availability, not CVSS score alone. CVE-2023-38408 had five confirmed public exploits at time of discovery — making it an immediate remediation priority regardless of other findings.

MITRE ATT&CK mapping:

T1190 — Exploit Public-Facing Application (OpenSSH, Nginx)
T1046 — Network Service Scanning (Nmap enumeration)
T1590 — Gather Victim Network Information (Shodan recon)
T1557 — Adversary-in-the-Middle (BREACH, SSL/TLS)


Information Security Policy
Category: GRC / Policy | Date: October 2024

Served as policy owner and lead author on a comprehensive Information Security Policy for a confidential legal technology client operating across all 50 U.S. states. Addressed GDPR and CCPA compliance obligations.

My contribution: Primary author of Security Incident Reporting Policy; contributing author across 17 additional sub-policies.

Frameworks: GDPR, CCPA, ISO 27001, SOC 2

18 sub-policies authored including:

Security Incident Reporting Policy (primary author)
Access Control Policy
Business Continuity and Disaster Recovery Policy
Third-Party Vendor Policy
AI Customer Interaction Policy
Remote Working and Access Policy
Regulatory Compliance Policy

Key design decisions: Built GDPR 72-hour breach notification obligations directly into the incident reporting workflow; defined severity tiers enabling consistent triage without senior involvement for every event.


## Operational Background

Most candidates at this level learned HIPAA compliance in a classroom. I ran pharmacy operations inside a regulated clinical environment for 10+ years.

→ [Healthcare Security Operations: A Practitioner's Perspective](./healthcare-security-operations-perspective.md)

