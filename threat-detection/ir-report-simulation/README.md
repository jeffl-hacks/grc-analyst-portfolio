Incident Response Report Simulation
Organization: Harness Projects
Date: January–March 2025
Category: Incident Response
Incident ID: IR-2025-03-003
Severity: Critical
Role: Solo author


Scenario / Objective
Authored a full incident response report for a simulated critical-severity, multi-vector attack scenario. The objective was to document a coordinated security incident involving three simultaneous attack vectors, demonstrate analyst-level thinking across detection, containment, and forensic analysis, and produce a professional IR deliverable following industry standards.

Note: Incident scenario was AI-assisted simulation. IOCs and identifying details have been anonymized. Language reflects designed/developed work rather than live incident response.


Tools / Frameworks Applied
Tool / Framework
Application
IR Report structure (NIST-aligned)
Executive summary, timeline, forensic findings, IOC appendix
DLP analysis concepts
Detection of insider data exfiltration
IOC documentation
Indicators of Compromise appendix
MITRE ATT&CK
Technique mapping across all three vectors



What the Incident Involved
Three Simultaneous Attack Vectors — March 1, 2025
Vector 1 — Insider Breach (Data Exfiltration)

An employee with administrative privileges exfiltrated customer PII and proprietary business data via SFTP/FTP to external devices. Detected by the DLP system flagging unusual file access and transfer activity at 2:30 PM.

Attack vector: Admin credentials used to bypass security protocols
Exfiltration method: SFTP/FTP transfer to external devices
Root cause: Excessive unmonitored administrative privileges; no least-privilege enforcement
Account suspended and access revoked at 3:00 PM

Vector 2 — DDoS Attack

Botnet-driven volumetric attack on web portal and payment gateway beginning at 2:00 PM. Caused approximately 6 hours of service disruption before full mitigation at 5:00 PM.

Cloud-based DDoS mitigation engaged at 2:05 PM (T+5 minutes)
Root cause: Absence of proactive DDoS mitigation tools; insufficient traffic filtering
All affected services restored after ~3 hours of mitigation

Vector 3 — Remote Access Trojan (RAT) Malware

RAT delivered via phishing email/malicious attachment. Enabled lateral movement, privilege escalation, and network reconnaissance across internal systems.

Detected at 2:15 PM via antivirus flag on employee system
Spread laterally exploiting weak network segmentation and unpatched systems
Root cause: Ineffective email filtering; unpatched systems
Malware eradicated and detailed forensic analysis initiated at 6:00 PM


Analysis
Key analyst insight: The DDoS attack functioned as adversarial noise — a deliberate distraction designed to overwhelm response capacity and mask the true objective: the simultaneous insider breach and RAT deployment.

This multi-vector coordination reflects a pattern consistent with advanced threat actors who use high-visibility attacks to consume SOC attention while lower-noise exfiltration and persistence techniques operate in parallel. Detection of the true threat required looking past the most visible incident and correlating the DLP alert with the malware detection.

Forensic findings summary:

Insider breach root cause: Unmonitored admin privileges + no least-privilege enforcement
DDoS root cause: No proactive mitigation tooling + insufficient traffic filtering
RAT root cause: Phishing delivery via ineffective email filtering + unpatched systems


MITRE ATT&CK Mapping
Technique
ID
Vector
Valid Accounts
T1078
Insider breach — admin credential abuse
Exfiltration Over Alternative Protocol
T1048
SFTP/FTP data exfiltration
Network Denial of Service
T1498
DDoS attack
Phishing
T1566
RAT delivery mechanism
Lateral Movement via Remote Services
T1021
RAT lateral spread
Privilege Escalation
T1055
RAT and insider privilege abuse



Incident Timeline
Time (UTC)
Event
Action Taken
2:00 PM, March 1
DDoS attack begins on web portal and payment gateway
Initial signs observed; DDoS mitigation services engaged
2:05 PM, March 1
DDoS mitigation activated
Traffic filtering begins
2:15 PM, March 1
Malware detected on employee system
Containment measures initiated
2:30 PM, March 1
Data breach detected — unusual file access flagged by DLP
Investigators review access logs
3:00 PM, March 1
Insider breach confirmed
Employee account suspended; access revoked
3:15 PM, March 1
DDoS attack peaks
Full mitigation implemented
4:00 PM, March 1
Malware spreading laterally
Infected systems isolated
5:00 PM, March 1
DDoS mitigation complete
All services restored after ~6 hours
6:00 PM, March 1
RAT identified and eradicated
Detailed forensic analysis begins
8:00 PM, March 1
Insider threat confirmed; employee terminated
Investigation escalated
12:00 AM, March 2
Full investigation initiated
Legal/compliance engaged; customers notified per breach notification laws



Outcome / Recommendations
Enforce principle of least privilege — audit and restrict all admin accounts
Implement real-time monitoring of privileged account activity
Deploy proactive DDoS mitigation tooling before incident occurs
Strengthen email filtering and conduct regular phishing awareness training
Establish patch management cadence to eliminate unpatched system exposure
Implement network segmentation to limit lateral movement potential
Develop multi-vector incident response playbook — simultaneous attack scenarios require parallel response tracks, not sequential



Note: Scenario was AI-assisted simulation for training purposes. All IOCs, client names, and identifying details are fictional or anonymized.


