# GRC Analyst Portfolio — Jeff Longe

## About

Clinical Pharmacy Technician with 10+ years of operational experience in a HIPAA-regulated environment (Texas Children's Hospital), transitioning into Governance, Risk & Compliance. Focused on risk assessment, control gap analysis, and regulatory compliance — built through hands-on engagements via the Harness Projects mentorship program and independent project work.

Most candidates at this level learned HIPAA in a classroom. I spent 10+ years enforcing it operationally — managing PHI handling, dispensing compliance, controlled substance auditing, and regulatory accountability inside a live clinical environment. That experience translates directly into core GRC competencies: access control review, segregation of duties, insider risk awareness, and incident escalation discipline.

---

## Certifications & Credentials

- CompTIA Security+ (SY0-701) — in progress
- ISC2 Certified in Cybersecurity (CC) — planned

---

## Skills

`Risk Assessment` `Risk Register Development` `Control Gap Analysis` `NIST CSF 2.0` `ISO 27001` `HIPAA Security Rule` `SOC 2` `GDPR` `CCPA` `Quantitative Risk Analysis (FAIR)` `Vendor/Third-Party Risk` `POA&M Development` `Policy Authorship` `Regulatory Compliance Mapping`

---

## Projects

| Project | Category | Frameworks / Methods | Role | Status |
|---|---|---|---|---|
| [PulseCare Telehealth Risk Assessment](GRC/pulsecare-risk-assessment/PulseCare_Risk_Assessment.xlsx) | Risk Assessment / Control Gap Analysis | NIST CSF 2.0, NIST SP 800-30, HIPAA Security Rule crosswalk | Risk assessor — primary author | Complete |
| [FAIR Quantitative Risk Analysis](GRC/fair-quantitative-risk-analysis/FAIR_Risk_Quantification_Memo.md) | Quantitative Risk Modeling | FAIR (Factor Analysis of Information Risk), Monte Carlo simulation | Risk analyst — primary author | In Progress |
| Cyber Risk Assessment & Risk Register | Risk Assessment | ISO 31000, likelihood/consequence risk matrix, regulatory scoping | Risk assessor — primary author | Complete |
| [Information Security Policy Suite](GRC/information-security-policy) | GRC / Policy | ISO 27001, SOC 2, GDPR, CCPA | Policy owner — primary author (acting CISO capacity) | Complete |
| [Infrastructure Vulnerability Assessment](GRC/infrastructure-vulnerability-assessment) | Technical Risk Input | CVE/CWE scoring, NIST-aligned remediation guidance | Individual execution + team cross-validation | Complete |
| Web App Vulnerability Assessment | Technical Risk Input | CVE/CWE scoring, OWASP-aligned findings | Team contributor | Complete |

*Note: Vulnerability assessments are retained as supporting technical evidence — they demonstrate the ability to translate raw findings into risk-rated, business-relevant remediation guidance, a core GRC skill, not a SOC specialization.*

---

### Featured: PulseCare Telehealth Risk Assessment

A fictional case study built to demonstrate end-to-end GRC risk assessment methodology — not based on any real client engagement.

**Scope:** Mid-size telehealth platform (~150 employees) handling PHI across patient scheduling, billing, and live video visits, with cloud-hosted EHR integration and third-party vendor dependencies.

**What it demonstrates:**
- Full risk register (15 risk observations) scored via Likelihood (1–5) × Impact (1–5), mapped to **NIST CSF 2.0 functions** (Govern, Identify, Protect, Detect, Respond, Recover)
- Each risk cross-walked to its corresponding **HIPAA Security Rule safeguard**
- A complete **POA&M (Plan of Action & Milestones)** with remediation actions, resource estimates, ownership, and target completion dates
- 3 Critical findings: absence of centralized log correlation across EHR/video/cloud systems, inconsistent MFA enforcement for clinical staff, and vendor onboarding without formal BAA review

This project shows the full GRC lifecycle — identify, score, document, remediate — using the same structure a healthcare compliance team would expect to see in a real risk assessment deliverable.

---

### Featured: FAIR Quantitative Risk Analysis

A quantitative risk model applying **FAIR (Factor Analysis of Information Risk)** methodology to a real risk scenario from operational pharmacy experience: IV unit-of-measure entry errors.

**What it demonstrates:**
- Monte Carlo simulation (100,000 iterations) producing a full annualized loss exposure (ALE) distribution, rather than a single point estimate
- PERT distribution sampling for calibrated min/most-likely/max inputs, following standard FAIR estimation practice
- **Two competing Vulnerability estimates modeled side-by-side** — an initial unanchored gut-estimate vs. a value derived from direct personal operational observation — rather than collapsing to one number. This makes the cost of estimation uncertainty visible instead of hiding it.
- Primary and secondary loss modeling (productivity, response cost, regulatory fines, civil/malpractice exposure) sourced from a mix of operational estimation and cited public benchmarks

**Why this matters:** quantitative risk analysis (translating risk into a dollar-denominated loss distribution, not just a red/yellow/green rating) is a skill almost no entry-level candidate demonstrates. This project also models honest analytical self-correction — surfacing a two-order-of-magnitude disagreement between estimation methods rather than papering over it.

*Full methodology, source citations, and the comparison memo available in `/GRC/fair-quantitative-risk-analysis`.*

---

## Operational Background

This writeup documents the security and compliance controls I operated within daily during 10+ years as a Clinical Pharmacy Technician — access management, audit logging, incident escalation, PHI handling, and shift accountability — and maps each directly to GRC analyst competencies: least-privilege/RBAC equivalents, two-person integrity and segregation of duties, insider risk awareness, regulatory compliance audits, and incident post-mortems.

→ [Healthcare Security Operations: A Practitioner's Perspective](healthcare-security-operations-perspective.md)

---

## Connect

[LinkedIn](https://linkedin.com/in/jeffl-hacks) | [GitHub](https://github.com/jeffl-hacks)
