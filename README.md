<div align="center">
  
# Executive Financial Health Hub

### An end-to-end consumer finance analytics project — dataset → analysis → executive dashboards

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-KPI%20Measures-5E5E5E?style=for-the-badge)
![Data Modeling](https://img.shields.io/badge/Data%20Modeling-Relationships-2F855A?style=for-the-badge)
![Looker Studio](https://img.shields.io/badge/Looker%20Studio-4285F4?style=for-the-badge)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Dataset](https://img.shields.io/badge/Records-250-147D64?style=for-the-badge)
![Currency](https://img.shields.io/badge/Currency-INR-orange?style=for-the-badge)

> An executive overview of household income, expenses, savings behavior, financial confidence, and regional differences across 250 survey respondents in India.

</div>

## Table of Contents

- [Live Demos](#live-demos)
- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Project Objectives](#project-objectives)
- [Data Source](#data-source)
- [Dataset Overview](#dataset-overview)
- [Dashboard Features](#dashboard-features)
- [Key Business Metrics](#key-business-metrics)
- [Metric Formulas](#metric-formulas)
- [Key Takeaways](#key-takeaways)
- [Where and How This Can Be Used](#where-and-how-this-can-be-used)
- [Tech Stack](#tech-stack)
- [Skills Demonstrated](#skills-demonstrated)
- [Repository Structure](#repository-structure)
- [How to Run](#how-to-run)
- [Notes and Limitations](#notes-and-limitations)
- [Author](#author)
- [License](#license)


## Project Overview

The Executive Financial Health Hub summarizes consumer financial survey data in an interactive dashboard. It brings income, expense, savings, confidence, and demographic views together to support fast, exploratory analysis.

## Dashboard preview

<img width="731" height="463" alt="image" src="https://github.com/user-attachments/assets/df8b5926-3e33-439a-9c14-a80e3a9a2b00" />


## Live Demos

- **Power BI:**  See `/Dashboard` folder (`.pbix` file) 
- **Tableau Public:** [Executive Financial Health Hub](https://public.tableau.com/app/profile/ajit.jha/viz/Executive_Financial_Health_Hub_v2/ExecutiveFinancialHealthHub?publish=yes)
- **Looker Studio:** [Open the shared report](https://datastudio.google.com/s/u6LD9DYi5bY) (Google sign-in may be required).

## Data Source

- **Source:** [Consumer Financial Behavior & Expense SurveyI — Kaggle](https://www.kaggle.com/datasets/ajitjha01/consumer-financial-behavior-and-expense-surveyi)
- **File:** `financial_consumer_survey_data.csv`
- **Coverage:** 250 respondents in India; 11 descriptive and financial fields.
- **License:** CC0: Public Domain, as stated on the Kaggle dataset page.

The dataset includes age, gender, region, income group, employment status, primary expense category, monthly income, monthly savings, and financial confidence score. Monetary values are in Indian rupees (INR).

## Dataset Overview

The Kaggle listing describes 250 unique respondents and 11 descriptive/financial fields. The fields cover demographic characteristics, income and employment groups, primary expense category, monthly income, monthly savings, and a self-reported financial-confidence score. Confirm the downloaded CSV's actual column names and units before reproducing the dashboard.

> The source CSV is not included in this starter repository. Download it from Kaggle and place it in `data/` if you want a local copy. Check Kaggle's current terms and attribution guidance before redistributing dataset files.

## Project Objectives

- Summarize financial health indicators in an executive-friendly dashboard.
- Compare income, expenses, and savings patterns across demographic and regional groups.
- Explore how reported financial confidence relates to savings behavior.
- Publish the analysis in Tableau Public and Looker Studio for interactive viewing.

## Business Problem

Households, financial-service providers, and policy teams often have plenty of transaction or survey data but lack a quick, coherent way to understand whether people can meet expenses, build savings, and feel financially secure. Looking at income alone can hide important differences: two groups with similar earnings may have very different expense burdens, savings habits, or confidence levels.

This project turns a small consumer-finance survey into an executive-level view of those questions. It brings income, estimated expenses, savings, demographic cohorts, geography, and self-reported financial confidence into one place so a user can spot patterns worth investigating.

### Questions the dashboard helps answer

- How do income and expenses vary by age, income band, and region?
- Which expense categories are most commonly identified as a primary cost?
- What does the reported savings rate look like across the sample and across cohorts?
- Do savings propensity and financial confidence appear to move together?
- Which segments may merit closer research or targeted financial-wellness support?

The dashboard is descriptive: it helps surface trends and formulate follow-up questions. It does not establish why a pattern exists or prove that one factor causes another.

## Why This Project Was Created

The goal is to demonstrate how a public dataset can be translated into a practical business-intelligence artifact—not just a collection of charts. The project packages key indicators into a single-page executive dashboard, adds demographic and regional context, and makes it possible to explore groups with filters and cohort comparisons.

It also provides a portfolio example of an end-to-end analytics workflow: identify a business question, inspect a dataset, define useful measures, communicate findings visually, and publish the analysis in three business-intelligence platforms: **Power BI, Tableau, and Looker Studio**. Building the same dashboard across these tools helps compare their calculation syntax and reporting capabilities.

## Where and How This Can Be Used

- **Personal-finance and financial-wellness teams:** Explore which survey segments report different savings or confidence patterns and use the results to shape questions for user research.
- **Banks, fintechs, and financial educators:** Use the dashboard as an exploratory starting point for discussing budgeting, saving behavior, and financial confidence—not as a customer-level decision engine.
- **Research and policy teams:** Quickly compare descriptive patterns by region or demographic group, then validate them using larger, representative studies and appropriate methods.
- **Business-intelligence portfolios and training:** Demonstrate KPI design, segmentation, dashboard layout, filter use, and cross-platform reporting.
- **Classroom or workshop discussions:** Practice interpreting survey data, identifying limitations, and turning charts into testable follow-up questions.

### Important usage boundaries

The dataset has 250 survey respondents and should not be treated as representative of all Indian consumers. The dashboard is not suitable for credit approval, eligibility decisions, individual risk scoring, pricing, or other high-impact decisions. It contains descriptive survey data and should not be used to make unsupported causal claims. Any operational use would require validation, a fit-for-purpose and representative dataset, privacy and fairness review, and domain-appropriate governance.

## Dashboard Features

- KPI cards for average income, average expenses, savings rate, confidence score, and sample size.
- Income-versus-expense comparisons by cohort.
- Expense category distribution.
- Financial confidence compared with savings propensity.
- Regional income disparity.
- Demographic cohort matrix and income-group root-cause exploration.
- Interactive income-group and age-group filters.

## Key Business Metrics

| Metric | Value shown |
|---|---:|
| Average income | ₹87.01K |
| Average expenses | ₹67.48K |
| Savings rate | 22.45% |
| Confidence score | 5.22 |
| Respondents | 250 |

Values are reproduced from the dashboard screenshot; refer to the live dashboards for current calculations and filter-dependent results.

## Metric Formulas

The formulas below document common definitions for the KPI cards. Replace field names with the exact column names in your downloaded CSV/model. In Power BI, the examples assume a table named `FinancialSurvey`. In Tableau and Looker Studio, create calculated fields with the corresponding expressions.

### Average monthly income

- **Business definition:** Arithmetic mean of respondents' monthly income.
- **Power BI (DAX):** `Average Income = AVERAGE(FinancialSurvey[Monthly_Income_INR])`
- **Tableau:** `AVG([Monthly_Income_INR])`
- **Looker Studio:** `AVG(Monthly_Income_INR)`

### Average monthly expenses

- **Business definition:** Arithmetic mean of respondents' monthly expenses.
- **Power BI (DAX):** `Average Expenses = AVERAGE(FinancialSurvey[Monthly_Expenses_INR])`
- **Tableau:** `AVG([Monthly_Expenses_INR])`
- **Looker Studio:** `AVG(Monthly_Expenses_INR)`

### Savings rate

A common portfolio-level definition is total savings divided by total income. This is an income-weighted rate. Use this definition consistently in all three dashboards if it matches the published KPI.

- **Power BI (DAX):** `Savings Rate = DIVIDE(SUM(FinancialSurvey[Monthly_Savings_INR]), SUM(FinancialSurvey[Monthly_Income_INR]))`
- **Tableau:** `SUM([Monthly_Savings_INR]) / SUM([Monthly_Income_INR])`
- **Looker Studio:** `SUM(Monthly_Savings_INR) / SUM(Monthly_Income_INR)`

Format the result as a percentage. Another valid measure is the average of each respondent's individual savings rate (`Monthly_Savings_INR / Monthly_Income_INR`). That answers a different question and may produce a different figure; confirm which method generated the dashboard's 22.45% before claiming an exact match.

### Average financial confidence score

- **Power BI (DAX):** `Average Confidence = AVERAGE(FinancialSurvey[Financial_Confidence_Score])`
- **Tableau:** `AVG([Financial_Confidence_Score])`
- **Looker Studio:** `AVG(Financial_Confidence_Score)`

### Respondent count (Size N)

Count unique respondent IDs so duplicate rows do not inflate the sample size.

- **Power BI (DAX):** `Respondent Count = DISTINCTCOUNT(FinancialSurvey[Respondent_ID])`
- **Tableau:** `COUNTD([Respondent_ID])`
- **Looker Studio:** `COUNT_DISTINCT(Respondent_ID)`

> **Validate the source schema:** The Kaggle listing describes 11 fields, but verify exact CSV column headers—especially the monthly-expense and confidence fields—before pasting these formulas. Apply the same filters and null-handling in Power BI, Tableau, and Looker Studio to keep results comparable.

## Key Takeaways

The dashboard screenshot reports an average monthly income of ₹87.01K, average monthly expenses of ₹67.48K, a 22.45% savings rate, an average confidence score of 5.22, and a sample size of 250. These are descriptive dashboard outputs, not conclusions about the wider population. Explore the live reports and validate calculations against the source data before drawing further conclusions.

## Tech Stack

- **Data source:** Kaggle CSV dataset
- **Business intelligence and visualization:** Power BI, Tableau Public, and Looker Studio
- **Currency / locale:** Indian rupees (INR)

## Skills Demonstrated

- Translating a business question into dashboard views and KPIs
- Exploratory segmentation by demographics, income groups, and region
- Data visualization and executive dashboard communication
- Publishing and documenting interactive BI reports
- Stating limitations and avoiding unsupported causal or population-level claims

## Repository Structure

```text
Executive Financial Health Hub/
│
├── data set/
│   ├── financial_consumer_survey_data.csv
│
│
├── Dashboard/
│   └── Executive Financial Health Hub.pbix
│   └── Executive Financial Health Hub.twbx
│
│
├── screenshots/
│   ├── powerbi dashboard.png
│   ├── tableau dashboard.png
│   ├── looker dashboard.png
│
└── README.md
│
└── License
```

## How to Run

1. Download the CSV from the [Kaggle dataset page](https://www.kaggle.com/datasets/ajitjha01/consumer-financial-behavior-and-expense-surveyi).
2. Put the file at `data/financial_consumer_survey_data.csv`.
3. Open either live dashboard using the links above. For your own dashboard copy, connect the CSV in Tableau or Looker Studio and recreate the views described here.

### 1. Clone the Repository via Terminal
Open your terminal or command prompt and run the following commands to download and navigate into the project:
```bash
git clone https://github.com
cd 250-Executive-Financial-Health-Hub
```

### 2. Download the Documents Manually
If you do not want to use Git, you can download the project documents manually from the browser:
* Go to the GitHub repository URL: https://github.com
* Click on the green **"Code"** button located at the top right of the file list.
* Select **"Download ZIP"** from the dropdown menu.
* Extract the downloaded ZIP file to your preferred local folder.


## Suggested analysis questions

- How does savings propensity vary across income and age groups?
- Which expense categories account for the largest share of reported spending?
- Do respondents with higher financial confidence also save a larger portion of income?
- How does average income differ across the five regions?
- How do employment status and income group relate to financial outcomes?

## Notes and Limitations

- This is a descriptive analysis of a 250-person survey dataset, not a representative estimate of all Indian households.
- Survey responses and derived dashboard metrics should not be interpreted as financial advice or causal evidence.
- Validate field definitions and calculations against the source CSV before reproducing or extending the dashboard.

# Author

**Ajit Jha**

Analytics Professional | Research & Business Intelligence

### Core Areas

`Data Analytics` • `Business Intelligence` • `Python` • `SQL` • `Power BI` • `Tableau` • `Looker Studio` • `Neo4j` • `Graph Analytics`

---

⭐ **If you find this project useful, feel free to explore the dashboards, data model, and Neo4j graph implementation.**
- **GitHub:** [Ajitjha3095](https://github.com/Ajitjha3095)
- **LinkedIn:** [Ajit Jha](https://www.linkedin.com/in/ajitjha01/)

## License

This project is licensed under the **MIT License**.  
See the [LICENSE](LICENSE) file for details.
