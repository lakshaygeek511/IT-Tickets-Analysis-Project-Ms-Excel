<div align="center">

<img src="https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white" alt="Excel"/>
<img src="https://img.shields.io/badge/PowerPoint-B7472A?style=for-the-badge&logo=microsoft-powerpoint&logoColor=white" alt="PowerPoint"/>
<img src="https://img.shields.io/badge/Data%20Analysis-0078D4?style=for-the-badge&logo=databricks&logoColor=white" alt="Data Analysis"/>
<img src="https://img.shields.io/badge/Dashboard-FF6F00?style=for-the-badge&logo=grafana&logoColor=white" alt="Dashboard"/>

# 🎫 Call Center IT Tickets Analysis

### A comprehensive data analysis project on Call Center IT Support Ticket Management, Agent Performance & Resolution Time & Customer Satisfaction.

---

</div>

## 🎯 Problem Statement

> You are tasked with analyzing the IT support ticket management system to understand the **performance of IT agents**, the **efficiency of ticket resolution**, and the **satisfaction levels of employees**.

The objective is to:
- Identify **high and low performers** among IT agents
- Assess the **overall effectiveness** of the IT team
- Pinpoint **areas for improvement** in the ticket resolution process
- Make informed **staffing decisions** — including hiring, firing, and training
- Enhance overall **service quality and team performance**

---

## 📌 Project Overview

This project performs an end-to-end data analysis on an IT support ticketing system spanning **5 years (2016–2020)** with **97,498 tickets** across **50 agents**. The analysis addresses both objective data questions (metrics, trends, correlations) and subjective business questions (investment priorities, staffing strategies, operational improvements).

| Metric | Value |
|---|---|
| 📊 Total Tickets Analyzed | **97,498** |
| 👥 Total IT Agents | **50** |
| 📅 Time Period | **2016 – 2020** |
| ⭐ Avg. Satisfaction Rate | **4.10 / 5** |
| ⏱️ Avg. Resolution Time | **4.55 Days** |
| 📁 Daily Ticket Volume | **53.37 tickets/day** |

---

## 📂 Dataset Description

The raw data consists of **two sheets**:

### 🎟️ Tickets Sheet — 11 Attributes
| Attribute | Description |
|---|---|
| Ticket ID | Unique identifier for each support ticket || Employee ID | ID of the employee who raised the ticket |
| Request Category | Category of the issue (Hardware, Login Access, Software, System) || Issue Type | Type of issue (IT Error / IT Request) |
| Severity | Severity level combined with type || Priority | Priority level combined with type || Issue Date (`Fecha`) | Date when the ticket was raised *(originally mislabelled)* |
| Agent ID | ID of the agent who handled the ticket || Resolution Time | Days taken to resolve the ticket |
| Satisfaction Rate | Employee's satisfaction rating || Age | Age of the employee |

### 🧑‍💼 IT Agents Sheet — 7 Attributes
| Attribute | Description |
|---|---|
| Agent ID | Unique identifier for each agent |
| Agent Name | Full name of the agent |
| Email | Agent's email address |
| Year of Birth | Birth year |
| Month of Birth | Birth month |
| Day of Birth | Birth day |
| Department | Agent's department |

### ✅ Cleaned Data — 15 Attributes
After preprocessing, two new columns were added per split (`Severity Type`, `Priority Type`) and corrections were applied — resulting in **15 clean attributes** used for all analysis.

---

## 🧹 Data Cleaning & Preprocessing

| Issue Found | Details | Count | Fix Applied |
|---|---|---|---|
| Inconsistent `Severity` column | Combined field — split into `Severity` + `Severity Type` | 97,498 | Text to Columns |
| Inconsistent `Priority` column | Combined field — split into `Priority` + `Priority Type` | 97,498 | Text to Columns |
| Misspelled "Unassigned" in Priority Type | Corrected via Find & Replace | 29,410 | Find & Replace |
| Misspelled "Major" in Priority Type | Corrected via Find & Replace | 4,836 | Find & Replace |
| Misspelled "Unclassified" in Severity Type | Corrected via Find & Replace | 356 | Find & Replace |
| Column name `Fecha` | Renamed to `Issue Date` | — | Column rename |
| Missing Values | None found | 0 | — |
| Duplicate Values | None found | 0 | — |

---
## 📊 Dashboard KPIs & Metrics

The final dashboard includes:

**KPI Cards:**
- Total Tickets | Urgent Tickets | Total Agents | Avg Resolution Time | Avg Satisfaction Rate

**Visualizations:**
- 🍩 Donut Chart — Tickets % by Satisfaction Rate
- 🥧 3D Pie Chart — Tickets % by Resolution Time
- 📊 Clustered Bar Chart — Ticket Count by Severity Type over Time
- 📉 Column Chart — Quarterly Resolution Time by Request Category
- 📈 Clustered Column Chart — Satisfaction Rate by Year & Age Group

**Interactive Slicers:**
- Date (Year) | Priority Type | Severity Type | Issue Type | Request Category

<img width="2718" height="1114" alt="image" src="https://github.com/user-attachments/assets/1af5f90a-5a65-4f0a-aea6-399889b05628" />

---
## 🔍 Key Findings & Insights

### 🗂️ Ticket Distribution by Category

| Request Category | Ticket Count | Distribution |
|---|---|---|
| 🖥️ System | 39,002 | **40.00%** |
| 🔐 Login Access | 29,193 | **29.94%** |
| 💻 Software | 19,570 | **20.07%** |
| 🔧 Hardware | 9,733 | **9.98%** |
| **Grand Total** | **97,498** | **100%** |

> **Insight:** System issues dominate with 40% of all tickets — indicating a need for infrastructure investment and system upgrades.

---

### 📈 Ticket Volume Trend (2016–2020)

| Year | Ticket Count | YoY Growth |
|---|---|---|
| 2016 | 13,051 | — |
| 2017 | 14,915 | +14.3% |
| 2018 | 18,954 | +27.1% |
| 2019 | 21,490 | +13.4% |
| 2020 | 29,088 | **+35.4%** |
| **Total** | **97,498** | — |

> **Insight:** Ticket volume **more than doubled** over 5 years, with a sharp **35% spike in 2020**. This is not a seasonal trend — volume grew every single year with no plateau.

---

### 😊 Satisfaction Rate Trend (2016–2020)

| Year | Avg. Satisfaction Rate | Avg. Resolution Time (Days) |
|---|---|---|
| 2016 | 3.98 | 4.55 |
| 2017 | 4.07 | 4.53 |
| 2018 | 4.09 | 4.56 |
| 2019 | 4.12 | 4.52 |
| 2020 | 4.16 | 4.59 |
| **Average** | **4.10** | **4.55** |

> **Insight:** Despite a rapidly increasing workload, satisfaction rates improved consistently year-over-year — demonstrating excellent performance under pressure.

---

### 🐛 Issue Type Distribution

| Issue Type | Percentage |
|---|---|
| IT Error | ~52% |
| IT Request | ~48% |

---

### 📊 Severity vs. Resolution Time

| Metric | Value |
|---|---|
| Correlation (Severity ↔ Resolution Time) | **-0.0405** |

> **Insight:** The near-zero correlation indicates severity level has **minimal impact** on resolution time — suggesting that process efficiency, not issue complexity, is the primary driver.

---

### 👶 Age Demographics & Satisfaction

| Age Group | Ticket Volume | Avg. Satisfaction |
|---|---|---|
| 25–34 | Lower | ~4.10 |
| 35–44 | **Highest** | ~4.10 |
| 45–54 | **High** | ~4.10 |
| 55+ | Lower | ~4.10 |

> **Insight:** Agents aged 35–54 carry the **highest workload**, while satisfaction remains consistent across all age groups — suggesting uniform service quality regardless of agent age.

---

## 👨‍💻 Agent Performance Analysis

### 🏆 Performance Criteria

Two performance thresholds were established:
- **Low Ticket Resolving:** Agents resolving tickets **below the 25th percentile**
- **Long Resolution Time:** Agents with **above-average resolution time**

### 🚨 Agents Flagged for Action

| Agent ID | Issue | Recommended Action |
|---|---|---|
| **Agent 13** | Low tickets AND long resolution time | 🔴 **Flag for Termination** |
| **Agent 49** | Low tickets AND long resolution time | 🔴 **Flag for Termination** |
| **Agent 19** | Lowest satisfaction rate (3.04 < 3.5) | 🟡 **Issue Formal Notice** |

### 📑 Summary Statistics
- 🔻 **12 agents** identified as least ticket-resolving agents (below 25th percentile)
- ⏱️ **13 agents** identified as having long resolution times
- ⭐ **1 agent** (Agent 19) flagged for critically low satisfaction rate of **3.04**

## 📁 Project Structure

```
📦 IT-Tickets-Analysis/
├── 📊 Project_IT_Tickets_Analysis_Spreadsheet___Dashboard.xlsx
│     ├── Raw Data (Tickets Sheet)
│     ├── Raw Data (IT Agents Sheet)
│     ├── Cleaned Data
│     ├── Pivot Tables & Charts (Objective Q1–Q13)
│     ├── Pivot Tables & Charts (Subjective Q1–Q10)
│     └── 📈 Interactive Dashboard
│
├── 📄 Project_IT_Tickets_Analysis_Answers_Document.docx
│     ├── Objective Questions (Q1–Q13) with Solutions & Approaches
│     └── Subjective Questions (Q1–Q10) with Insights & Recommendations
│
├── 📽️ IT_Tickets_Analysis_Presentation.pptx
│     └── Executive Summary Presentation
│
└── 📝 README.md
```

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Microsoft Excel** | Data storage, cleaning, analysis, pivot tables, charting |
| **Excel Pivot Tables** | Aggregation and cross-tabulation of ticket data |
| **Excel Dashboard** | Interactive KPI dashboard with slicers and charts |
| **Microsoft PowerPoint** | Executive presentation of findings |
| **Excel Functions** | `XLOOKUP`, `CORREL`, `TEXTAFTER`, `TEXTBEFORE`, `DATE`, `DATEDIF`, `AVERAGE`, `ROUND`, `ISBLANK`, `PERCENTILE` |

---

## 🚀 How to Use

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/IT-Tickets-Analysis.git
   cd IT-Tickets-Analysis
   ```

2. **Open the Excel file**
   ```
   Project_IT_Tickets_Analysis_Spreadsheet___Dashboard.xlsx
   ```
   - Navigate to the **Dashboard** sheet for the interactive overview
   - Use slicers to filter by Year, Priority, Severity, Issue Type, or Category

3. **Review the Analysis Document**
   ```
   Project_IT_Tickets_Analysis_Answers_Document.docx
   ```
   - Objective Questions (Q1–Q13): Factual analysis with exact numbers
   - Subjective Questions (Q1–Q10): Business insights and recommendations

4. **View the Presentation**
   ```
   IT_Tickets_Analysis_Presentation.pptx
   ```
   - Executive summary for stakeholders

---

<div align="center">

---

### 📊 Quick Stats

![Total Tickets](https://img.shields.io/badge/Total%20Tickets-97%2C498-blue?style=flat-square)
![Total Agents](https://img.shields.io/badge/Total%20Agents-50-green?style=flat-square)
![Avg Satisfaction](https://img.shields.io/badge/Avg%20Satisfaction-4.10%2F5-brightgreen?style=flat-square)
![Avg Resolution](https://img.shields.io/badge/Avg%20Resolution-4.55%20Days-orange?style=flat-square)
![Years Covered](https://img.shields.io/badge/Years%20Covered-2016--2020-purple?style=flat-square)

---

*Built with ❤️ using Microsoft Excel & Data Analysis*

</div>
