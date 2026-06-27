# Cyber Risk Assessment & Risk Register

**Methodology:** ISO 31000 — qualitative Likelihood × Consequence risk matrix
**Engagement:** Harness Projects client engagement (Dec 2024)
**Role:** Risk assessor — primary author
**Status:** Complete

---

## 1. Engagement Scope

The client was a small (4-employee), fully remote AI-services company with no formal security program in place — no role-based access control, no MFA, no documented incident response plan, and no structured patch management process. This is a realistic profile for an early-stage organization, and one that closely mirrors what a GRC analyst encounters when assessing vendor or third-party risk.

The assessment covered:
- **Asset inventory** — 11 information assets identified, owned, and located (cloud infrastructure, employee devices, third-party integrations, financial records, customer data, and communications systems)
- **Threat identification** — modeled separately from vulnerabilities (human factor risk, targeted cyberattacks, malware/phishing), rather than conflating the two
- **Vulnerability identification** — 8 distinct vulnerability categories spanning access control, patch management, network monitoring, cloud configuration, and incident response readiness
- **Regulatory scoping** — applicable U.S. data privacy obligations were determined based on the client's actual operational footprint (CCPA, FTC Act enforcement standards, state breach notification law), while frameworks that didn't apply (GDPR — no EU data subjects or presence) were explicitly scoped out rather than listed by default

---

## 2. Risk Register

17 risk observations were identified and scored using a Likelihood × Consequence matrix (Likelihood: Rare → Almost Certain; Consequence: Insignificant → Extreme), producing a Risk Rating from Low to Critical.

| ID | Risk Description | Likelihood | Consequence | Risk Rating |
|---|---|---|---|---|
| RO1 | Lack of formal policies and procedures across all assets | Almost Certain | Major | **High** |
| RO2 | Unauthorized access due to weak information security policy (password creation/management) | Likely | Major | **High** |
| RO3 | Lack of regular cybersecurity awareness training | Likely | Major | **High** |
| RO4 | Misconfiguration of cloud services / cloud infrastructure | Possible | Major | **High** |
| RO5 | Weak home network security (employee routers) | Likely | Moderate | **High** |
| RO6 | Exposure of shared email account credentials via insecure exchange methods | Possible | Major | **High** |
| RO7 | Exposure to targeted attacks by external opportunistic actors | Possible | Major | **High** |
| RO8 | Inconsistent network monitoring and log analysis (web server, database) | Likely | Major | **High** |
| RO9 | Lack of vulnerability assessment for web application and infrastructure | Possible | Major | **Moderate** |
| RO10 | Lack of compliance auditing across all data systems | Possible | Major | **Moderate** |
| RO11 | Supply chain attack compromising third-party cloud services | Unlikely | Moderate | **Moderate** |
| RO12 | Insider threat causing accidental or intentional data leakage | Unlikely | Major | **Moderate** |
| RO13 | Outdated home network equipment (personal laptops/routers) | Possible | Moderate | **Moderate** |
| RO14 | Dependence on a single technical expert for web server maintenance | Unlikely | Major | **Moderate** |
| RO15 | No incident response policy for business continuity / disaster recovery | Unlikely | Major | **Moderate** |
| RO16 | Backups exist but are untested for restore reliability | Possible | Major | **Moderate** |
| RO17 | Lack of vulnerability assessment of AI/API code and integrations | Possible | Major | **Moderate** |

---

## 3. Existing Controls Assessment

A key part of this engagement was evaluating not just *whether* a control existed, but *how effective* it actually was — a distinction that matters because a documented control with weak effectiveness still leaves real exposure.

| ID | Control | Effectiveness |
|---|---|---|
| C1 | Web Application Firewall (DoS / SQL injection protection) | Moderate |
| C2 | Regular software and AI system updates | Moderate |
| C3 | Identification and Authentication controls | Moderate |
| C4 | Data and log management | Moderate |
| C5 | Access control and procedures (role-based access) | **Low** |
| C6 | Cybersecurity employee training | **Low** |

The two lowest-effectiveness controls — access control and security awareness training — correspond directly to the two highest-rated risks in the register (RO1–RO3). This wasn't a coincidence worth glossing over: it's the clearest signal in the entire assessment that remediation priority should follow control effectiveness, not just risk likelihood alone.

---

## 4. Action Plan (Risk Treatment)

9 action items were developed, each mapped to specific risk IDs with an objective, priority, and assigned owner — turning the assessment from a static report into a working remediation roadmap.

| ID | Linked Risks | Treatment | Priority | Owner |
|---|---|---|---|---|
| AP1 | RO3 | Enhance employee cybersecurity awareness training | High | CEO / CISO |
| AP2 | RO9 | Establish a regular patch management cycle | High | CISO / IT |
| AP3 | RO2, RO5 | Implement multi-factor authentication | High | CISO / IT |
| AP4 | RO4 | Conduct quarterly cloud security audits; automate configuration checks | High | CISO / IT |
| AP5 | RO1 | Establish documentation standards, regular policy review, and compliance audit cycles | High | CISO |
| AP6 | RO7 | Establish a scheduled software patch cycle | High | CISO / IT |
| AP7 | RO5 | Mandate VPN use with strong encryption for all remote work | High | CISO / IT |
| AP8 | RO6, RO7 | Deploy anomalous traffic detection tooling; schedule phishing awareness training | Moderate | CISO / IT |
| AP9 | RO7, RO8, RO11, RO12, RO15 | Establish automated backups, a disaster recovery plan, and evaluate EDR/MDM solutions | Moderate | CEO / CISO / IT |

---

## 5. Why This Matters for a GRC Role

This engagement demonstrates the full risk management lifecycle, not just risk identification in isolation:

- **Asset inventory before risk scoring** — risk can't be rated meaningfully without first knowing what's actually at stake
- **Threats modeled separately from vulnerabilities** — a distinction often blurred at entry level, but one that changes how remediation gets prioritized
- **Control effectiveness, not just control existence** — recognizing that a documented control can still be a weak one
- **Regulatory scoping based on actual footprint** — reasoning through which frameworks genuinely apply rather than defaulting to a generic compliance checklist
- **A remediation roadmap with ownership** — every risk observation ties to an action item with a responsible party, not just a finding left unresolved

*Note: Client name, infrastructure details, and other identifying information have been redacted or generalized throughout this writeup in accordance with confidentiality requirements from the original engagement.*
