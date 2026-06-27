# FAIR Quantitative Risk Analysis — Risk Quantification Memo

**Scenario:** IV Unit-of-Measure (UOM) Entry Error
**Risk Register Reference:** R-003
**Methodology:** FAIR (Factor Analysis of Information Risk) — [fairinstitute.org](https://www.fairinstitute.org/)
**Author:** Jeff Longe

---

## 1. Purpose

Most entry-level risk registers stop at a qualitative rating: Low / Medium / High. This project goes one step further and asks the question a risk owner actually needs answered — **what is this risk likely costing us in dollar terms per year, and how much does that number depend on the assumptions we feed it?**

FAIR breaks risk into two measurable components:

```
Loss Event Frequency (LEF) = Threat Event Frequency (TEF) × Vulnerability
Loss Magnitude (LM)         = Primary Loss + Secondary Loss
Annualized Loss Exposure    = LEF × LM, simulated across many possible years
```

Rather than computing a single number, a Monte Carlo simulation (100,000 simulated years) was run to produce a full **loss distribution** because real-world risk is a range, not a point estimate, and decision-makers need to see the tail risk, not just the average.

---

## 2. The Scenario

An IV unit-of-measure entry error occurs when a dose is entered into the system using the wrong unit (e.g., mg vs. mL), creating downstream risk if the error isn't caught before administration. This is a real operational risk category drawn from pharmacy practice — used here as a quantification case study, not tied to any specific employer's confidential incident data.

**Threat Event Frequency (TEF):** 3–6–12 UOM errors entered per year (min–likely–max), calibrated from typical operational visibility into how often such errors surface through standard pharmacist communication channels.

**Vulnerability:** the probability that, once an error is entered, it slips past all layered controls (pharmacist verification, system alerts, nursing double-check) and becomes an actual loss event.

---

## 3. The Key Finding: Two Estimates, Not One

This is the part of the analysis that matters most, and it's also the most honest part.

Two different ways of estimating "Vulnerability" were modeled **side by side, deliberately left unresolved**, rather than picking whichever number felt more comfortable:

| | Scenario A: Gut-Estimate | Scenario B: Observation-Anchored |
|---|---|---|
| **Method** | Initial unanchored qualitative judgment | Backed out from 2 confirmed events observed over ~12 years of direct operational exposure |
| **Vulnerability (min–likely–max)** | 1/10,000 – 2/5,000 – 1/1,000 | 1/100 – ~1/36 – 1/15 |
| **Mean Annualized Loss Exposure** | **$381** | **$25,736** |

**The two estimation methods disagree by roughly two orders of magnitude on the underlying probability — and that disagreement alone moves the bottom-line annual cost estimate by over 67x.**

This wasn't smoothed over. It's the headline result. A risk estimate is only as good as the weakest input feeding it, and Vulnerability — not Threat Event Frequency, not Loss Magnitude — turned out to be the input doing almost all the work in this model. A risk analyst's job isn't just to produce a number; it's to know which number to trust and why, and to be transparent when two defensible methods don't agree.

---

## 4. Loss Magnitude Components

Each simulated loss event draws from four cost categories, combined for total impact:

- **Productivity loss** — staff time displaced for incident-related discussion (excludes direct clinical response time)
- **Response cost** — RCA documentation, follow-up communication, and (at the high end) mandatory retraining with overtime backfill
- **Regulatory fines** — modeled on public Texas State Board of Pharmacy administrative penalty ranges; most cases resolve with no board involvement ($0)
- **Civil/malpractice exposure** — a deliberately fat-tailed, rare-event input; most likely outcome is $0, with the tail anchored to published settlement examples as a directional benchmark only, not verified case data

---

## 5. Visual Output

![FAIR Scenario Comparison](fair_scenario_comparison.png)

*Left: conditional loss exceedance curve — given a loss event occurs, the probability of exceeding a given dollar amount. Right: mean annualized loss exposure by Vulnerability estimation method.*

---

## 6. Why This Matters for a GRC Role

Quantitative risk analysis is named in security and compliance literature as a maturity step beyond qualitative heat-map scoring, but very few entry-level candidates can show it hands-on. This project demonstrates:

- Practical application of an industry-recognized quantitative risk framework (FAIR), not just familiarity with the name
- Statistical literacy: Monte Carlo simulation, PERT distributions, conditional vs. unconditional probability
- Calibrated estimation discipline — using real operational history to anchor an estimate instead of relying purely on intuition
- The judgment to surface estimation uncertainty rather than resolve it artificially — a trait risk committees and auditors specifically look for

**Reproducibility:** full simulation code, fixed random seed, and inputs are documented in `fair_simulation.py` in this folder.

---

*Note: This analysis uses operational risk categories and publicly available benchmark data for educational/portfolio purposes. It is not based on, and does not disclose, any employer's confidential incident records.*
