# 📊 CoreVista Group – Financial Performance Dashboard (Power BI)

A business-ready Profit & Loss dashboard created in Power BI to track and analyze key financial metrics like Revenue, Net Profit, COGS, and Operating Expenses over time. This solution simulates a real-world scenario for financial storytelling, trend monitoring, and executive reporting.

---

## 📌 Table of Contents:

- [Problem Statement](#problem-statement)
- [Datasource](#datasource)
- [Data Preparation](#data-preparation)
- [Data Modeling](#data-modeling)
- [Data Analysis (DAX)](#data-analysis-dax)
- [Data Visualization (Dashboard)](#data-visualization-dashboard)
- [Insights](#insights)
- [Recommendation](#recommendation)

---

## 🔍 Problem Statement

The goal is to build a dynamic P&L dashboard for a fictional company, **CoreVista Group**, that allows users to monitor financial performance across months and years, compare against previous periods, and identify key cost drivers.

Key questions this dashboard helps answer:
- How is the company performing financially this year vs last year?
- Which expense areas are impacting profit most?
- How do Revenue and Net Profit trend over time?

---

## 🌐 Datasource

- **Source**: Simulated P&L dataset  
- **Format**: Excel → imported into Power BI  
- **Structure**:
  - `P&L Table` (fact)
  - `Dim P&L` (line item descriptions)
  - `Calendar` (date dimension)

---

## 🧹 Data Preparation

Steps taken in Power Query:
- Cleaned nulls and unnecessary columns
- Converted `Date` to proper date format
- Extracted Year, Month, Month-Year columns
- Added conditional logic for groupings (e.g., Financial Category)

---

## 🏗️ Data Modeling

| Table        | Role                 |
|--------------|----------------------|
| `P&L Table`  | Fact table with Amount, Date, Line Items |
| `Dim P&L`    | Dimension table for financial categories |
| `Calendar`   | Date table for YTD, MoM, and YoY analysis |

Relationships:
- One-to-many from `Calendar[Date]` → `P&L Table[Date]`
- One-to-many from `Dim P&L[Index]` → `P&L Table[Index]`

---

## 🧠 Data Analysis (DAX)

Created custom measures including:
- **[Revenue]**, **[COGS]**, **[Gross Profit]**
- **[Net Profit]** = Revenue - COGS - Expenses
- **[YTD Revenue]**, **[Revenue LY]**, **[Revenue YoY %]**
- **[MoM %]** for key metrics
- **[Expense to Revenue %]**

Used `CALCULATE`, `SAMEPERIODLASTYEAR`, `TOTALYTD`, `PREVIOUSMONTH`, and `DIVIDE` extensively.

---

## 📊 Data Visualization (Dashboard)

### 📘 Financial Overview

![Financial Overview](https://github.com/user-attachments/assets/89249d9b-ce46-46cc-bb1b-bf3365c80665)

---

### 📘 Last Year Analysis

![Last Year Analysis](https://github.com/user-attachments/assets/f81a89ba-cc4b-4f27-88dc-d867d5eed354)

---

### 📘 Income Statement

![income statement](https://github.com/user-attachments/assets/a92d0dd7-a996-47a3-ade9-0bafe5504312)

---

## 🔎 Insights

- Net Profit steadily increased over Q3–Q4
- Operating Expenses are the largest non-COGS driver
- 2023 Revenue outperformed 2022 by 12%
- December saw a sharp revenue spike (+40% MoM)
- Taxes and D&A remain stable across periods

---

## ✅ Recommendation

- Focus on managing Operating Expenses, especially during high-revenue months
- Monitor COGS ratio to maintain Gross Margin
- Automate revenue forecasting with historical YoY/MoM patterns
- Extend dashboard to include Budget vs Actuals and Cash Flow

---

## 📁 Files

| File                                    | Description                      |
|-----------------------------------------|----------------------------------|
| `corevista-financial-dashboard.pbix`    | Main Power BI report             |
| `screenshots/`                          | Visual previews of dashboard     |
| `README.md`                             | Project documentation            |

---

## 📌 License

Open source for educational and portfolio use. Attribution appreciated.  
Do not redistribute commercially without permission.

---

##  Author

**Paul Olulana**  
Data Analyst  
Connect on [LinkedIn](https://www.linkedin.com/in/oluwafemi-paul-3a7272265/)
