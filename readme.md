# 🔍 Audit Universe Dashboard
### An end-to-end Power BI analytics project by [Swarleen Bhamra](https://www.swarleen.com)

[![Live Dashboard](https://img.shields.io/badge/View%20Live%20Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](#)
[![Portfolio](https://img.shields.io/badge/swarleen.com-1B3A6B?style=for-the-badge)](https://www.swarleen.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/swarleenbhamra/)

---

## The Project

Every audit team maintains an audit universe — a catalogue of all auditable entities scored by risk, control effectiveness, and coverage history. This dashboard simulates a risk-based audit planning tool for a Technology Audit function: where to focus, what's overdue, where controls are failing, and what leadership needs to act on.

Built to speak the language of audit — not just visualising data, but surfacing the insights that drive planning decisions, resource allocation, and executive reporting.

> 🔗 **[Explore the live interactive dashboard here](https://app.powerbi.com/view?r=eyJrIjoiMjQ1NDA3M2EtMTBjOC00YWJkLWIzZjktZGMzZjRhYjdjNWQzIiwidCI6IjMyMWIxNDA4LTIxZjAtNDE0My1hMzkwLTNiNjIwMmU2NWUxZiJ9)**

---

## The Data

**44 audit entities · 13 dimensions · 5 technology domains**

A structured mock audit universe spanning the full technology risk landscape of a mid-to-large enterprise. Each row represents one auditable entity — a process, system, or control domain — scored across risk, control quality, coverage history, and issue status.

**Domains covered:**
Cybersecurity · Cloud & Infrastructure · Data Governance · IT Governance · Compliance & Regulatory

**Each entity carries:**
- Inherent risk score (1–5) — the underlying risk before controls are applied
- Control effectiveness rating — Strong / Adequate / Weak / Not Tested
- Residual risk score — derived from inherent risk adjusted for control quality
- Audit priority — Critical / High / Medium / Low, derived from residual risk
- Last audit date and months since last review
- Open issues count — unresolved findings from prior audits
- Management response status — On Track / Overdue / Not Started
- Regulatory relevance — whether the entity carries compliance obligations
- Recommended audit cycle — Annual / Biennial / Risk-Based
- Overdue flag — whether the entity has exceeded its scheduled review window

---

## The Metrics

**Total Audit Entities**
The full count of auditable entities in scope. Establishes the size of the audit universe and the denominator for all coverage and risk calculations.

**Critical & High Priority**
Count of entities classified as Critical or High audit priority based on residual risk score. Measures the proportion of the universe carrying elevated risk that requires prioritised audit attention.

**Overdue Entities**
Count of Critical and High priority entities that have exceeded their scheduled audit review window. Directly measures the coverage gap — how much of the high-risk universe is going unreviewed.

**Total Open Issues**
Sum of all unresolved audit findings across the universe. High open issue counts signal that prior audits are identifying problems but remediation is not completing — a compounding risk indicator.

**Not Tested Entities**
Count of entities where control effectiveness has never been assessed. Represents true blind spots in the control environment — risks that are neither confirmed nor ruled out.

**Coverage Gap %**
Proportion of the full audit universe that is overdue for review. Calculated as overdue entities divided by total entities. The primary measure of audit planning health — a high coverage gap means risk is accumulating unmonitored.

**Avg Months Since Last Audit**
Average time elapsed since each entity was last reviewed. Contextualises the coverage gap — a high average signals systemic under-resourcing of the audit function, not just isolated delays.

**Weak Controls Count**
Count of entities with a Weak control effectiveness rating. Used to drive the gauge visual and quantify the proportion of the universe where controls are insufficient to mitigate inherent risk.

---

## What Was Built

### Data Modelling
44-row audit universe with 13 dimensions — combining defined risk scores with derived calculated fields including Residual Risk Score, Audit Priority classification, and Overdue Flag logic.

### DAX Measures
8 custom measures across two domains — volume and coverage (total entities, critical & high, overdue, not tested) and risk performance (open issues, avg months since audit, weak controls count, coverage gap %).

### Dashboard Design
Single-page layout on a dark charcoal canvas with 6 visual types working together:

- **5 KPI cards** — executive snapshot of audit universe health
- **Matrix heatmap** — Domain × Priority with conditional colour gradient
- **Donut charts ×2** — Audit Priority distribution and Management Response Status
- **Treemap** — Domain concentration by entity count
- **Gauge** — Weak controls as a proportion of the full universe
- **Detail table** — Full entity list ranked by priority and open issues

All visuals cross-filter via Domain, Regulatory Relevance, and Audit Priority slicers.

---

## Tools & Technologies

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-1B3A6B?style=for-the-badge)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

---

## About

**Swarleen Bhamra** — Business Analyst & Data Analyst based in Toronto, ON.

I build analytics solutions that turn complex data into decisions — across cybersecurity, audit, HR, and business operations domains.

- 🌐 [swarleen.com](https://www.swarleen.com)
- 💼 [LinkedIn](https://www.linkedin.com/in/swarleenbhamra/)
- 📊 [Power BI Portfolio](https://github.com/Swarleen/PowerBI-Portfolio)

> Open to Business Analyst, Data Analyst, and Analytics roles in Toronto.

---

*Dataset is fictional and created for portfolio demonstration purposes only. No real audit data was used.*
