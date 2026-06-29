# AML Transaction Monitoring — Analytics Portfolio Project (2024–2025)
## 1) Project Overview
This project simulates an end-to-end **Anti-Money Laundering (AML) transaction monitoring** operation across a fictional multi-jurisdictional bank (2024–2025). The core focus is **alert lifecycle management**—identifying suspicious transactions, understanding where financial crime risk concentrates (client segment, product, jurisdiction, and channel), and defining escalation and SAR-filing actions to close detection and documentation gaps. The dataset covers **22,399 transactions**, **500+ clients**, and **15 detection rules** across all major AML typologies including structuring, high-risk jurisdiction transfers, PEP exposure, sanctions proximity, layering, and crypto/virtual asset activity.

## 2) Tools Used
- **Excel** — data structuring, pivot analysis, KYC/SAR/jurisdiction cross-tabulations, and risk distribution summaries
- **Power BI** — visualisation and executive dashboarding (SteerCo-ready views across three report pages
## 3) Insight Highlights
- **Alert coverage is structurally broad:** 15 detection rules span all primary FATF typologies — structuring, layering, PEP transactions, dormant account reactivation, sanctions proximity, and crypto activity.
- **Risk rating is heavily skewed toward elevated segments:** only **22.3%** of transactions (4,997) relate to Low-rated customers; **77.7%** sit in Medium, High, or Very High — indicating genuine portfolio risk concentration or calibration issues in the underlying rating model.
- **High-risk jurisdiction exposure is material:** 10 FATF/EU-listed jurisdictions account for **2,831 transactions**; North Korea, Iran, and Afghanistan generate the highest SAR-to-transaction ratios relative to volume.
- **PEP population SAR rate is elevated:** **109 unique PEP-flagged clients** have confirmed SAR filings, making PEP status combined with transaction velocity a reliable predictor of suspicious activity.
## 4) What I Achieved
- Built a **full AML transaction monitoring risk view** across a 22,399-transaction synthetic dataset covering alert generation, case management, SAR filing, and multi-dimensional risk scoring.
- Identified where financial crime risk concentrates — by jurisdiction, client segment, product type, and channel — to support **risk-based alert prioritisation** and MLRO escalation decisions.
- Constructed a **four-dimension risk scoring model** (geographic, product, channel, composite) driving alert priority and auto-escalation logic.
- Produced a **SteerCo-ready Power BI dashboard** covering SAR filing intelligence, PEP/customer risk exposure, and risk rating distribution.
- Delivered a **60-action written recommendations register** with regulatory hooks across FATF, EU AMLD, Wwft, CBN, and FINTRAC/PCMLTFA frameworks.

## 5) Challenges & Solutions
| Challenge | Impact | Solution Implemented |
|---|---|---|
| Lack of real-world AML dataset availability | Limited access to representative transaction monitoring data with realistic alert patterns | Created a **synthetic 22,399-row dataset using AI** to simulate realistic typologies (structuring, layering, PEP exposure, dormancy reactivation) with **no PII** |
| Designing detection rules at realistic thresholds | Generic rules produce either too many false positives or miss true positives | Anchored rule thresholds to EU AMLD and FATF guidance (e.g. €10,000 cash reporting, €5,000 PEP trigger) and included velocity and pattern-based rules alongside value-based ones |
| Risk rating skew toward elevated segments | 77.7% of transactions in Medium/High/Very High makes Low-risk the minority — raises questions about model calibration | Flagged as a key finding; segmented analysis by rating tier and used pivot analysis to surface whether Very High clients drive disproportionate alert volume |
| Representing the full alert-to-SAR lifecycle | Capturing every stage (alert → case → escalation → SAR) in a single flat dataset without breaking referential logic | Structured the dataset with `alert_id`, `case_id`, and SAR reference as nullable linked fields; modelled realistic dropout at each lifecycle stage |
| Translating alert analytics into remediation actions | Insights not automatically converted into a usable action plan | Converted findings into a **prioritised 60-action recommendations register** with regulatory hooks, owner assignments, and executive summary narrative |
| Power BI performance on a large transactional model | Slow visuals and relationship ambiguity across alert, case, and SAR fields | Used aggregated pivot inputs for dashboard visuals and limited report pages to **decision-grade KPIs** (SteerCo-level views only) |

## 6) Recommendations (AML Remediation Focus)
1. **PEP-first review sprint:** prioritise the 109 PEP-flagged clients with confirmed SAR filings for MLRO case review.
2. **Jurisdiction exposure remediation:** implement enhanced monitoring and relationship review for all clients with active counterparty flows into North Korea, Iran, Afghanistan, Somalia, and Cuba — the five jurisdictions with the highest SAR-to-transaction ratios.
3. **KYC refresh programme:** address the population of clients in `Expired`, `Due for Renewal`, and `Pending EDD` status — particularly where transactions continue to be processed (a direct R010 trigger and regulatory examination risk).
5. **Governance and KPIs:** implement weekly case closure tracking (alert disposition rate, escalation rate, SAR conversion rate, average days case open) and set escalation triggers for cases exceeding 30-day open thresholds.

## 7) Dataset Source
- **Synthetic dataset generated using AI** to simulate a multi-jurisdictional bank's AML transaction monitoring environment (2024–2025) for **portfolio and learning purposes**.
- Data is **non-production, non-client, and contains no personal identifiable information (PII)**.
- Designed to include realistic detection challenges: **structuring patterns, layering chains, dormant account reactivations, PEP concentration, FATF-jurisdiction exposure**, and KYC lifecycle gaps.
- **22,399 rows · 66 fields · 500+ clients · 15 detection rules · 20 transaction types · 39 industry sectors**

## 8) Contributor
**Ayodeji Jolaoso**

## 9) Contact
- **LinkedIn:** (https://www.linkedin.com/in/a-jolaoso/)
- **Email:** dejijolaosonl@gmail.com
- **Location:** Netherlands (EU)
