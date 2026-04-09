# 🔍 Audit Universe Dashboard
### Risk-Based Audit Planning · Technology Audit Analytics · Power BI

<div align="center">

**Built by [Swarleen Bhamra](https://www.swarleen.com)**

[![🚀 Click Here to Open the Live Dashboard](https://img.shields.io/badge/🚀%20Click%20Here%20to%20Open%20the%20Live%20Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://app.powerbi.com/view?r=eyJrIjoiMjQ1NDA3M2EtMTBjOC00YWJkLWIzZjktZGMzZjRhYjdjNWQzIiwidCI6IjMyMWIxNDA4LTIxZjAtNDE0My1hMzkwLTNiNjIwMmU2NWUxZiJ9)

<a href="https://app.powerbi.com/view?r=eyJrIjoiMjQ1NDA3M2EtMTBjOC00YWJkLWIzZjktZGMzZjRhYjdjNWQzIiwidCI6IjMyMWIxNDA4LTIxZjAtNDE0My1hMzkwLTNiNjIwMmU2NWUxZiJ9" target="_blank" rel="noopener noreferrer">
  <img src="https://img.shields.io/badge/🚀%20Open%20Live%20Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Open Live Dashboard"/>
</a>


> 👆 Click the badge above to open the live interactive dashboard in a new tab

[![Portfolio](https://img.shields.io/badge/🌐%20swarleen.com-1B3A6B?style=for-the-badge)](https://www.swarleen.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/swarleenbhamra/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Swarleen/PowerBI-Portfolio)

</div>

---

## 💡 The Story

Every internal audit team faces the same challenge — too many risks, too few resources, and not enough visibility into where to focus.

The answer is an **audit universe**: a structured catalogue of every auditable entity in the organisation, scored by risk, assessed for control quality, and tracked for review history. Without it, audit planning is guesswork. With it, every decision is defensible.

This dashboard brings that audit universe to life in Power BI — simulating the kind of risk-based planning tool a Technology Audit function at a global financial institution would use to answer three fundamental questions:

> 🔴 **Where is the risk?** — Which entities carry the most exposure and weakest controls?
> ⏱️ **What's overdue?** — Where has the audit function lost coverage?
> 📋 **What needs to happen?** — Which open issues are going unresolved?

It's not just a dashboard. It's a decision-support tool built in the language of audit.

---

## 🗂️ The Audit Universe

**44 audit entities · 13 dimensions · 5 technology domains**

The dataset represents the full technology risk landscape of a mid-to-large enterprise. Each row is one auditable entity — a process, system, or control domain — scored across risk exposure, control quality, coverage history, and issue status.

### 🏛️ Domains Covered

| Domain | Entities | What It Covers |
|---|---|---|
| 🛡️ Cybersecurity | 10 | IAM, PAM, Vulnerability Management, SOC, DLP, Incident Response, Endpoint Security, Phishing Controls |
| ☁️ Cloud & Infrastructure | 10 | Azure Cloud Security, CASB, DR/BCP, Patch Management, Network Security, Backup & Recovery |
| 🗄️ Data Governance | 8 | Data Classification, Privacy & PII, Database Access, Data Quality, Data Lineage, Retention |
| ⚙️ IT Governance | 8 | Change Management, Vendor & Third Party Risk, ITAM, Audit Logging, IT Policies |
| 📜 Compliance & Regulatory | 8 | OSFI/PIPEDA, AML Controls, SOX ITGC, Model Risk, Fraud Risk, Insurance Reporting |

### 📐 Data Dimensions

Each entity is scored across 13 fields:

```
Inherent Risk Score       →  Raw underlying risk before controls (1–5)
Control Effectiveness     →  Strong / Adequate / Weak / Not Tested
Residual Risk Score       →  Inherent risk adjusted for control quality (derived)
Audit Priority            →  Critical / High / Medium / Low (derived)
Last Audit Date           →  Date of most recent completed audit
Months Since Last Audit   →  Calculated from last audit date to today
Open Issues               →  Unresolved findings from prior audit cycles
Management Response       →  On Track / Overdue / Not Started
Regulatory Relevance      →  High / Medium / Low compliance obligation
Recommended Audit Cycle   →  Annual / Biennial / Risk-Based
Overdue Flag              →  Yes / No — exceeded scheduled review window
Domain                    →  Technology audit domain classification
Audit Entity              →  Name of the auditable process or system
```

---

## 📊 The Metrics — What Each One Measures

### 🔢 Volume & Coverage

**📌 Total Audit Entities**
The complete count of entities in the audit universe. The foundation metric — establishes universe size and serves as the denominator for all ratio and coverage calculations.

**🔴 Critical & High Priority**
Entities classified as Critical or High audit priority based on their residual risk score. Measures how much of the universe demands prioritised attention — the higher this number relative to total entities, the more stretched the audit function needs to be.

**⏰ Overdue Entities**
Critical and High priority entities that have exceeded their scheduled review window. This is the most operationally significant metric — it directly quantifies how much high-risk territory is going unreviewed. Overdue ≠ missed. Overdue = unquantified risk accumulating in real time.

**📋 Total Open Issues**
Sum of all unresolved audit findings across the entire universe. A high count signals that prior audits are identifying problems but remediation isn't completing — a compounding risk indicator. Open issues in overdue entities are particularly concerning because the audit function hasn't returned to validate whether anything has changed.

**❓ Not Tested Entities**
Entities where control effectiveness has never been assessed. These are true blind spots — the organisation neither knows whether controls work nor whether they exist at all. Not Tested is always higher risk than Weak, because Weak is at least known.

### 📈 Risk & Performance

**📉 Coverage Gap %**
The proportion of the full audit universe that is overdue for review. The primary health metric for audit planning — a high coverage gap means risk is accumulating without oversight. Calculated as: `Overdue Entities ÷ Total Audit Entities`.

**🗓️ Avg Months Since Last Audit**
Average elapsed time since each entity was last reviewed. Contextualises the coverage gap — a high average signals systemic under-resourcing, not just isolated scheduling delays. An average above 24 months for a high-risk domain is a red flag in any regulated environment.

**⚠️ Weak Controls Count**
Count of entities rated Weak for control effectiveness. Drives the gauge visual. Used to quantify the proportion of the universe where controls are insufficient to mitigate inherent risk — the combination of high inherent risk AND weak controls defines the Critical priority tier.

---

## 🛠️ What Was Built

### Data Modelling
Structured a 44-row audit universe with 13 dimensions, combining defined risk inputs with derived calculated fields. Residual Risk Score is computed from Inherent Risk adjusted by Control Effectiveness weighting. Audit Priority and Overdue Flag are both derived classifications — no manual labelling.

### ⚡ DAX Measures
8 custom measures across two analytical domains:

```dax
Total Audit Entities = COUNTROWS(Audit_Universe)

Critical & High Priority =
CALCULATE(COUNTROWS(Audit_Universe),
Audit_Universe[Audit_Priority] IN {"Critical", "High"})

Overdue Entities =
CALCULATE(COUNTROWS(Audit_Universe),
Audit_Universe[Overdue_Flag] = "Yes")

Total Open Issues = SUM(Audit_Universe[Open_Issues])

Not Tested Entities =
CALCULATE(COUNTROWS(Audit_Universe),
Audit_Universe[Control_Effectiveness] = "Not Tested")

Avg Months Since Audit =
AVERAGE(Audit_Universe[Months_Since_Last_Audit])

Coverage Gap % =
DIVIDE([Overdue Entities], [Total Audit Entities], 0)

Weak Controls Count =
CALCULATE(COUNTROWS(Audit_Universe),
Audit_Universe[Control_Effectiveness] = "Weak")
```

### 🎨 Dashboard Design
Single-page dark charcoal canvas with 6 visual types:

| Visual | Purpose |
|---|---|
| 5 × KPI Cards | Executive snapshot — instant read of universe health |
| Matrix Heatmap | Domain × Priority with conditional colour gradient |
| Donut Chart × 2 | Audit Priority distribution + Management Response Status |
| Treemap | Domain concentration by entity count |
| Gauge | Weak controls as a proportion of the full universe |
| Detail Table | Full entity list ranked by priority and open issues |

3 cross-filtering slicers: Domain · Regulatory Relevance · Audit Priority

---

## 🧰 Tools & Technologies

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-1B3A6B?style=for-the-badge&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Excel](https://img.shields.io/badge/Microsoft%20Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Power Query](https://img.shields.io/badge/Power%20Query-742774?style=for-the-badge&logo=microsoft&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)
![Canva](https://img.shields.io/badge/Canva-00C4CC?style=for-the-badge&logo=canva&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-0078D4?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Confluence](https://img.shields.io/badge/Confluence-172B4D?style=for-the-badge&logo=confluence&logoColor=white)

---

## 👩‍💻 About

**Swarleen Bhamra** — Business Analyst & Data Analyst based in Toronto, ON.

I build analytics solutions that turn complex data into decisions — across cybersecurity, audit, HR, and business operations domains. This project reflects my interest in technology audit and risk analytics — combining data engineering, DAX modelling, and audit domain knowledge into a single decision-support tool.

<div align="center">

| | |
|---|---|
| 🌐 Portfolio | [swarleen.com](https://www.swarleen.com) |
| 💼 LinkedIn | [linkedin.com/in/swarleenbhamra](https://www.linkedin.com/in/swarleenbhamra/) |
| 📊 Power BI Portfolio | [github.com/Swarleen/PowerBI-Portfolio](https://github.com/Swarleen/PowerBI-Portfolio) |

</div>

> 💼 Open to Business Analyst, Data Analyst, and Technology Audit Analytics roles.
> If this project resonates with what your team is building — let's connect.

---

<div align="center">
<sub>Dataset is fictional and created for portfolio demonstration purposes only. No real audit data was used.</sub>
</div>
