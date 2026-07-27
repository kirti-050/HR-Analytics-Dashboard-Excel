# 👥 HR Analytics Dashboard — Excel Portfolio Project

An end-to-end interactive HR analytics dashboard built in Microsoft Excel, analyzing **1,470 employee records** from the IBM HR Attrition dataset to identify the root causes of above-benchmark employee attrition and provide actionable retention recommendations.

---

## 🖥️ Dashboard Preview

> *Add your dashboard screenshot here — drag and drop the image into GitHub after uploading*

---

## 📌 Project Overview

This project simulates a real-world HR analyst task — transforming raw employee data into an interactive executive dashboard that helps HR leadership understand *why* people are leaving and *where* to focus retention efforts. The dashboard allows stakeholders to filter by Department, Gender, and Job Level using interactive slicers, with all charts and KPIs updating dynamically.

**Key Business Finding:** Employees required to work overtime leave at **3x the rate** of non-overtime employees — making workload management, not compensation, the single most actionable lever for reducing attrition.

---

## 🎯 Business Questions Answered

- Is the company's attrition rate above or below industry benchmark?
- Which department faces the highest employee turnover?
- Which age group is most at risk of leaving?
- Does overtime work predict attrition — and by how much?
- How does compensation vary across job roles, and does it drive dissatisfaction?
- What is the salary distribution across the workforce?

---

## 📁 Project Structure

```
HR-Analytics-Dashboard/
│
├── HR_Analytics_Dashboard_Kirti.xlsx    ← Main Excel file
│
└── README.md                            ← You are here
```

### Workbook Sheet Structure

| Sheet | Purpose |
|---|---|
| **Dashboard** | Interactive KPI cards, 5 charts, slicers — main view |
| **Raw Data** | Clean employee data (1,470 rows) loaded via Power Query |
| **Calculations** | COUNTIFS, AVERAGEIFS, INDEX-MATCH, RANK aggregation tables |
| **Pivot Analysis** | 5 Pivot Tables and 5 Pivot Charts linked to dashboard |
| **Insights** | Written business insights and strategic recommendations |

---

## 🔧 Excel Features & Functions Used

### Data Cleaning — Power Query (Get & Transform)
| Step | Purpose |
|---|---|
| Remove Other Columns | Kept only 19 relevant columns from 35 total |
| Change Data Types | Ensured numeric columns aren't stored as text |
| Custom Column: Age_Group | Grouped ages into 5 bands (18-25, 26-35, 36-45, 46-55, 55+) |
| Custom Column: Income_Band | Grouped salaries into 4 tiers (Low, Mid, High, Very High) |
| Close & Load To Table | Loaded clean data as named Excel Table (`HRData`) |

### Formulas & Functions
| Function | Purpose |
|---|---|
| `COUNTIF` | Total attrition count (single condition) |
| `COUNTIFS` | Multi-condition attrition segmentation by dept, age group, overtime |
| `AVERAGEIFS` | Average salary by department and job role |
| `IFERROR` | Clean error handling across all calculated fields |
| `INDEX-MATCH` | Dynamic lookup — identifying highest/lowest earner roles and highest attrition dept |
| `RANK` | Ranking departments by average salary (1 = highest) |
| `AGGREGATE` | MAX/MIN salary by job role (Excel 2016 compatible alternative to MAXIFS/MINIFS) |
| `COUNTA` | Total employee headcount |
| `TEXT` + `&` | Dynamic insight text bar concatenating live KPI values |

### Excel Features
- **Power Query** — automated data cleaning with recorded, repeatable steps
- **Pivot Tables** — Department × Attrition, Age Group × Attrition, Job Role Salary, Overtime × Attrition, Income Band distribution
- **% of Row Total** — converting raw attrition counts to attrition rate percentages inside Pivot Tables
- **Pivot Charts** — Column, Line, Bar, and Pie charts linked to Pivot Tables
- **Slicers** — Department, Gender, Job Level filters connected to all 5 Pivot Tables via Report Connections
- **Conditional Formatting** — Attrition Rate KPI card turns red above 15% benchmark, green below
- **Dynamic Text Bar** — concatenated formula that updates with slicer selections showing live attrition rate, highest risk dept, and top earner role
- **Named Tables** — structured referencing (`HRData[MonthlyIncome]`) for robust formulas
- **Calculated Fields** — custom aggregations inside Pivot Tables

---

## 📊 Key Metrics

| KPI | Value | Benchmark | Status |
|---|---|---|---|
| Total Employees | 1,470 | — | — |
| Employees Who Left | 237 | — | — |
| Attrition Rate | 16.1% | 15.0% | ⚠️ Above Benchmark |
| Avg Monthly Income | ₹6,503 | — | — |
| Avg Age | 36.9 years | — | — |
| Avg Years at Company | 7.0 years | — | — |

---

## 💡 Key Business Insights

**1. Attrition Rate Exceeds Industry Benchmark**
At 16.1%, the attrition rate exceeds the standard 15% benchmark. With 237 out of 1,470 employees having left, this represents a significant and costly retention challenge requiring immediate strategic action.

**2. Sales Department Faces Highest Attrition Risk**
Sales records the highest attrition volume across all three departments. Human Resources, despite being the smallest department, shows a disproportionately high attrition rate relative to its headcount — suggesting high-pressure roles are primary drivers of turnover.

**3. 26–35 Age Group is the Critical Retention Window**
Early-to-mid career professionals (26–35) account for the highest absolute attrition numbers. Employees who survive this window tend to stay long-term — making this age band the most strategically important for retention investment.

**4. Overtime is the Strongest Attrition Predictor (3x Effect)**
Overtime employees leave at 30.5% versus 10.4% for non-overtime employees — approximately 3 times higher. This is the single strongest attrition predictor in the dataset, suggesting workload and work-life imbalance are more significant push factors than compensation alone.

**5. 7x Compensation Gap Between Junior and Senior Roles**
Managers earn approximately 7 times more than Sales Representatives. Given that Sales Representatives also belong to the highest-attrition department, this gap likely contributes to junior staff dissatisfaction and turnover.

---

## 🚀 Strategic Recommendations

1. **Target 26–35 age group** with structured career development programs — this is the highest-risk retention window
2. **Audit overtime policies** in Sales and R&D — the 3x attrition multiplier makes this the most immediately actionable finding
3. **Review entry-level Sales compensation** — the 7x salary gap between Representatives and Managers likely drives junior staff dissatisfaction
4. **Conduct exit interviews** focused on overtime workers and the 26–35 cohort to validate data findings with qualitative insight
5. **Set a 15% attrition target** and use this dashboard to monitor monthly progress by department and job level

---

## 🆕 New Skills vs Previous Project

This is my second Excel portfolio project. Here's what this project added beyond the Sales Dashboard:

| Skill | Sales Dashboard | HR Dashboard |
|---|---|---|
| Data Cleaning | Manual (Text to Columns, TRIM) | Power Query (automated, repeatable) |
| Lookup Formula | VLOOKUP | INDEX-MATCH (direction-free) |
| Ranking | Not used | RANK function |
| Pivot Aggregation | Sum, Count | % of Row Total, Average |
| Chart Types | Bar, Line | Bar, Line, Column, Pie |
| Dynamic Features | Slicer → charts | Slicer → charts + dynamic text bar |
| Domain | Retail / Sales | Human Resources |

---

## 📂 Dataset

**Source:** IBM HR Analytics Employee Attrition & Performance
**Platform:** Kaggle — [IBM HR Analytics Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
**Records:** 1,470 employees
**Columns Used:** 19 of 35 available fields
**Key Fields:** Age, Attrition, Department, Gender, JobLevel, JobRole, MonthlyIncome, OverTime, TotalWorkingYears, WorkLifeBalance, YearsAtCompany

---

## 🛠️ Data Challenges Solved

- **35 columns reduced to 19 relevant fields** using Power Query's Remove Other Columns — keeping only what the analysis needed
- **Age grouping and Income banding** done inside Power Query using M language conditional logic — so new data auto-categorizes on refresh
- **MAXIFS/MINIFS unavailable in Excel 2016** — solved using AGGREGATE function with division-based filtering as a compatible alternative
- **Pivot Table % formatting** — used "Show Values As → % of Row Total" to convert raw counts into attrition rates without any helper formulas

> These challenges are documented intentionally — handling real constraints is a core analyst skill.

---

## 📈 What This Project Demonstrates

Beyond technical Excel skills, this project demonstrates:

- **Business domain knowledge** — understanding HR metrics like attrition rate, benchmark comparison, and retention windows
- **Analytical thinking** — the overtime finding (3x effect) challenges the common assumption that salary is the primary attrition driver
- **Data storytelling** — translating chart visuals into specific, quantified business language ("3x higher", "7x salary gap")
- **Design thinking** — color-coded KPI cards, dynamic text bar, and consistent visual theme across all sheets

---

## 👩‍💻 About

**Kirti** — BCA Graduate (Data Science & AI)

Building a data analytics portfolio targeting Data Analyst and Business Analyst roles across India.

**Portfolio Projects:**
- ✅ Sales Performance Dashboard (Excel) — Superstore dataset
- ✅ HR Analytics Dashboard (Excel) — IBM Attrition dataset
- 🔄 Financial P&L with What-If Analysis (Excel) — coming soon
- ⏳ Customer Segmentation Analysis (Tableau) — coming soon

📧 *[kirtisri.vin19@gmail.com]*
🔗 *[www.linkedin.com/in/kirti-srivastava-16a7a3290]*
🐙 *[[Add your GitHub profile URL](https://github.com/kirti-050)]*

---

## 📄 License

This project is for portfolio and educational purposes.
The IBM HR Analytics dataset is publicly available via Kaggle.
