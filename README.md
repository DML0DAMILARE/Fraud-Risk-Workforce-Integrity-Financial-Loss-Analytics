# Aegis Financial Services — Fraud Risk, Workforce Integrity & Financial Loss Analytics

An end-to-end analytics case study for a UK-based financial services company, combining **HR workforce-integrity analysis** and **financial fraud-loss analytics** into a single joint risk framework — the **Employee Fraud Risk Score (EFRS)** — and a live executive dashboard.

![status](https://img.shields.io/badge/status-complete-2FD1C0) ![tools](https://img.shields.io/badge/tools-Excel%20%7C%20Power%20Query%20%7C%20HTML%2FJS-D8B45C) ![domain](https://img.shields.io/badge/domain-fraud%20analytics-FF5A5F)

---

## 📌 Overview

Aegis Financial Services Ltd. is a mid-sized UK lender and payment processor (2,000+ employees, 1M+ customer accounts) that experienced rising internal fraud losses — payroll manipulation, expense abuse, ghost employees, and suspicious transactions — with no unified way to see who or where the risk was concentrated.

This project builds that unified view across **two analyst workstreams**:

| Workstream | Owner | Focus |
|---|---|---|
| **HR Analyst** | Workforce behaviour | Attendance abuse, performance-fraud signals, disciplinary history, workforce integrity scoring |
| **Financial Analyst** | Financial exposure | Fraud loss & recovery, payroll/expense/transaction fraud, department exposure, EFRS model |

The two workstreams are joined by two shared models: the **Employee Fraud Risk Score (EFRS)** and the **Workforce Integrity Score**, which power a single executive dashboard.

---

## 🗂️ Repository Contents

```
├── HR_Analyst_Data.xlsx           # Source data + HR risk models (Excel/Power Query)
├── Financial_Analyst_Data.xlsx    # Source data + fraud/financial risk models (Excel/Power Query)
├── Aegis_Risk_Dashboard.html      # Interactive executive dashboard (open in any browser)
└── README.md
```

> The dashboard is a **static, self-contained HTML file** — no server or install required. Open it directly in a browser, or publish it via GitHub Pages.

---

## 🧩 Data Architecture

Data flows from simulated HRIS, Payroll, Expense, and Transaction-monitoring systems into Excel for cleaning and modelling, then into the dashboard for visualization.

**Core tables:**

| Table | Rows | Description |
|---|---:|---|
| `Employee_Master` | 2,000 | Demographics, department, salary, tenure, manager hierarchy |
| `Attendance` | 56,000 | Monthly overtime, absences, lateness, sick days |
| `Performance_Data` | 18,000 | Quarterly productivity, error rate, suspicious-pattern flags |
| `Disciplinary_Records` | 287 | Incident type, severity, resolution time |
| `Fraud_Incidents` | 195–203 | Fraud type, financial loss, recovery, detection method |
| `Payroll_Transactions` | 56,000 | Base pay, overtime, bonus, payroll anomalies |
| `Expense_Claims` | 4,426 | Claim category, approval status, duplicate/exception flags |
| `Transactions` | 13,777 | Channel, amount, suspicious flag, risk score |

---

## 🎯 Objectives

1. Build a centralized fraud analytics framework across HR and Financial data
2. Score every employee's fraud risk with a transparent, weighted model (EFRS)
3. Track fraud KPIs — loss, recovery, incident rate — over time
4. Identify workforce behaviours that correlate with fraud risk
5. Rank departments by fraud exposure
6. Deliver one executive dashboard for proactive, not reactive, risk management

---

## 🧮 The Employee Fraud Risk Score (EFRS)

A single 0–100 score per employee, blending seven weighted risk factors:

| Factor | Weight |
|---|---:|
| Fraud Incident History | 30% |
| Suspicious Transactions | 15% |
| Expense Fraud | 15% |
| Payroll Abuse | 10% |
| Attendance Abuse | 10% |
| Disciplinary History | 10% |
| Performance Anomalies | 10% |

Employees are banded **Low (0–20) · Moderate (21–40) · High (41–60) · Critical (60+)**, and department-level **Exposure Score = Avg. EFRS × Headcount** ranks business lines by aggregate fraud risk.

---

## 📊 Key Findings

- **£6.99M** total fraud loss across 195 confirmed cases (FY2024–2026 YTD), only **20.0%** recovered
- **Ghost Employee** and **Kickback Scheme** fraud account for the largest share of losses
- **Consumer Lending** is the highest-exposure department (largest headcount × above-average EFRS)
- Average EFRS is low (**16.6/100**) — risk is concentrated in a small tail of **31 employees** flagged High or Critical
- Workforce Integrity Score averages **96.0/100**, but **63 employees** sit in the High-Risk band and warrant monitoring
- **2,140** employees show a High-Productivity/High-Error pattern — a leading indicator worth watching alongside fraud flags

---

## 🖥️ Dashboard

`Aegis_Risk_Dashboard.html` — a single-page executive command center with six sections:

1. **Executive Pulse** — headline KPIs across both workstreams
2. **Financial KPIs** — fraud loss Pareto, recovery effectiveness, payroll/expense/transaction fraud
3. **HR KPIs** — workforce profile, attendance risk, performance fraud, disciplinary breakdown
4. **EFRS Model** — weight breakdown and top-10 highest-risk employees
5. **Department Fraud Exposure** — ranked exposure ladder by business line
6. **Workforce Integrity** — score distribution and risk bands

Built with vanilla HTML/CSS/JS and [Chart.js](https://www.chartjs.org/) — all figures are computed directly from the source workbooks.

---

## 🛠️ Tech Stack

| Layer | Tool |
|---|---|
| Data storage & cleaning | Microsoft Excel, Power Query |
| Risk modelling & KPIs | Excel formulas (SUMIFS/COUNTIFS/AVERAGEIFS) |
| Visualization | HTML5, CSS3, JavaScript, Chart.js |

---

## 🚀 Usage

```bash
# Clone the repo
git clone https://github.com/<your-username>/aegis-fraud-risk-analytics.git
cd aegis-fraud-risk-analytics

# Open the dashboard — no build step required
open Aegis_Risk_Dashboard.html   # macOS
start Aegis_Risk_Dashboard.html  # Windows
```

Or enable **GitHub Pages** on this repo (Settings → Pages → Deploy from branch) and share the dashboard as a live link.

---

## 📁 Data Disclaimer

All data in this repository is **synthetically generated** for the purposes of this case study. Aegis Financial Services Ltd. is a fictional company; no real customer, employee, or transaction data is used.

---

## 👤 Author

Case study designed and built as a portfolio project demonstrating joint HR + Financial fraud analytics, risk scoring, and dashboard design.
