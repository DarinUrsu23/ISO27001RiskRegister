# Information Security Risk Register — ISO/IEC 27001:2022

A working risk register built for a fictional financial services entity, demonstrating practical application of ISO 27001:2022 **Clause 6.1.2** (Risk Assessment) and **Clause 6.1.3** (Risk Treatment).

![Risk Heatmap — Inherent vs Residual Position](risk_heatmap_linkedin.png)

---

## About

This is a portfolio artefact — not a live document, and not derived from any real organisation. The fictional entity ("Nexus Financial Services Ltd") and all risk content, scores, ticket references, policy IDs, and named approvers are invented. The patterns it reflects are based on the standard, on EU regulatory context (DORA, NIS2, GDPR), and on observed industry practice.

It exists because operational GRC roles increasingly require the ability to author and maintain a risk register fluently, defend scoring decisions in front of internal audit, and connect technical controls back to a recognised framework. A working artefact demonstrates these abilities more concretely than a CV bullet.

---

## Repository Contents

| File | Description |
|------|-------------|
| `ISO27001_Risk_Register_Nexus_FINAL.xlsx` | The main artefact. Seven sheets covering document control, methodology, the register itself, heatmap, risk acceptance log, Annex A mapping, and a project notes / AI disclosure sheet. |
| `risk_heatmap_linkedin.png` | Anonymised summary visualisation showing inherent vs residual risk position. |
| `README.md` | This file. |

---

## Sheet-by-Sheet Overview

**Document Control** — version history, document owner and approver, distribution list, risk appetite statement. Five versions tracked from initial release through final QA review.

**Methodology** — 5×5 likelihood and impact scales with definitions tied to financial services context (€ thresholds, GDPR Article 33 notification, DORA major incident classification, CBI reporting). Four treatment options aligned to Clause 6.1.3 with explicit approval thresholds.

**Risk Register** — 15 risks across six categories. Columns include inherent and residual scoring, control effectiveness rating, Annex A control mapping, treatment plan with action references (JIRA tickets, policy IDs, programme codes), named risk owner, last review date, trend indicator versus prior baseline, and status.

**Risk Heatmap** — Side-by-side 5×5 inherent and residual matrices with quarterly movement summary.

**Risk Acceptance Log** — Formal records of risks accepted by the organisation, including a legacy mainframe risk with a CRO-signed Risk Acceptance Record valid until system decommissioning in 2027.

**Annex A Mapping** — 27 ISO 27001:2022 Annex A controls referenced in the register, organised by theme (Organisational, People, Physical, Technological). Cross-references the Statement of Applicability.

**Project Notes & AI Disclosure** — methodology rationale, AI assistance disclosure, difficulties encountered, and limitations.

---

## Risk Coverage

Fifteen risks were selected to represent the spread you would expect on a financial services register:

- **Cyber** — ransomware, account takeover via phishing, privilege escalation, web application attack, Azure misconfiguration, BYOD endpoint exposure, legacy system exploitation
- **Compliance** — GDPR breach via unmasked test data, DORA non-compliance, NIS2 incident reporting gap
- **Third-Party** — critical SaaS vendor compromise (treated as Mitigate + Transfer hybrid via cyber liability cover)
- **Operational** — catastrophic ICT failure / DR readiness, workforce security awareness
- **Physical** — unauthorised data closet access
- **Strategic** — shadow AI / unsanctioned public LLM use

The register is sorted by residual risk descending. Most risks are Open – In Treatment; one is Closed (privileged access following PIM rollout), one is formally Accepted (legacy mainframe with compensating controls), and one has a Q1 action that has slipped past its due date and is flagged as Open – Action Overdue.

---

## AI Use — Disclosure

I used Claude (Anthropic) as an iterative drafting partner. Transparency on this matters; the disclosure is also documented inside the workbook itself on a dedicated sheet.

**What AI accelerated:** Excel structure and formatting, drafting risk statement language, suggesting candidate Annex A controls, and a final critical-review pass that surfaced logical inconsistencies in my own work.

**What I owned:** Methodology choices (5×5 matrix, appetite threshold at Medium, treatment option definitions, acceptance approval routing), risk selection and weighting, scoring decisions for each risk, realism calibration, and editorial control over what made it into the final document.

**What needed rework:** The first AI-assisted draft was unrealistically clean — every risk reduced to a Low residual, uniform scoring, every status set to "In Progress." Successive iterations introduced realistic friction: a Closed risk, an Accepted risk with a formal RAR, residuals that stop at Medium because controls aren't perfect, an action past its due date, and a Mitigate + Transfer hybrid for the SaaS vendor.

**Final review pass:** A critical review against four common reviewer questions caught three logical errors and one Annex A mis-mapping. All four were corrected in v2.5. The version history in the Document Control sheet records the specifics.

---

## Limitations

This register is not derived from real threat intelligence, real asset inventories, or real control test results. It is not a substitute for an organisation-specific risk assessment.

Methods deliberately excluded for scope reasons:

- Quantitative loss methods such as FAIR or Annualised Loss Expectancy
- Key Risk Indicator (KRI) thresholds with explicit escalation triggers
- The full Statement of Applicability (referenced as a separate document — ISMS-SOA-001 — in line with how most organisations structure it)
- Linked control library or evidence repository
- Workflow integration; in production this would typically live in a GRC platform such as ServiceNow GRC, Archer, or OneTrust

---

## What I Would Extend in a Real Engagement

Key Risk Indicators tied to live monitoring data — phishing click-rate, mean time to remediate, patch SLA compliance — with defined escalation triggers. Scenario-based assessments for the top three to five risks. Integration with the incident register so realised events feed back into likelihood scoring. Quantified loss bands for risks where the modelling effort is justified, typically the high and critical-rated ones.

---

## Author

**Darin Ursu** — Compliance Operations Analyst (Microsoft OMP, via Infosys). Working towards CISSP; Associate of ISC², CompTIA Security+, ISC² CC.

[LinkedIn](https://www.linkedin.com/in/darinursu)

---

*Built April 2025. All organisational details are fictional. Provided for portfolio review and educational use.*
