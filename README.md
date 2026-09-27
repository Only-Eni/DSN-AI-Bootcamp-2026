DSN AI Bootcamp 2026 — Dashboard Audit & Data Analytics
Data Analytics Track | Audit the Dashboard
A transaction-level data quality, dashboard audit, and corrected management reporting project completed as part of the DSN AI Bootcamp 2026 Data Analytics Track.
The project independently reviews a management dashboard and its underlying retail transaction data, identifies data-quality and calculation issues, tests the management's stated conclusions, and produces a corrected Excel dashboard supported by validated analysis.
Project Overview
The original management dashboard presented conclusions about market profitability, category performance, discounting, sales trends, return rates, and data reliability.
Rather than reproducing those conclusions, this project follows an audit-first approach:
Raw data → Data-quality audit → Cleaning & validation → Claim testing → Corrected analysis → Corrected dashboard → Management recommendations
The objective was to determine what the data actually supports, what requires correction, and which management conclusions should not be relied upon without further validation.
Business Questions
The analysis addresses eight management claims:
Is Abuja the most profitable market?
Is Electronics the strongest-performing category, and does that justify allocating more budget to it?
Does higher discounting improve profitability?
Does the Online channel have the lowest return rate?
Is August the strongest sales month?
Is Lagos underperforming compared with other markets?
Can the reported Revenue field be used directly for decision-making?
Is the original dashboard sufficiently reliable for management action without further cleaning?
The project also answers five final management questions concerning the most misleading conclusion, the most material correction, business risk, performance drivers, and next actions.
Tools
Microsoft Excel — data cleaning, validation, analysis, dashboard development
Excel formulas / structured tables — transaction-level calculations and validation
Data-quality audit techniques — duplicate detection, label standardization, missing-value review, calculation reconciliation
No Power BI or PivotChart-based dashboard was used. The corrected dashboard was developed using standard Excel tables and charts.
Dataset Audit
Initial Dataset
Metric
Result
Raw rows
432
Unique transactions
420
Duplicate rows identified
12
Missing unit-cost records
31
Revenue mismatches after validation
22
The 12 duplicate rows were exact duplicate transaction records and were removed before the main analysis.
Data-quality Issues Identified
1. Duplicate transactions
The raw dataset contained 432 rows but only 420 unique transaction IDs.
The duplicated records were exact copies. They were removed so that the same transaction would not be counted twice in revenue, profit, units, or other performance calculations.
2. Inconsistent market/state labels
The same market appeared under inconsistent labels, including:
Lagos
Lagos 
LAGOS
These were standardized to a single Lagos category.
Similar category-label inconsistencies were also identified and standardized, including variations of Accessories.
3. Missing product costs
There were 31 cleaned transaction records with missing Cost_Per_Unit_NGN values.
The observed unit cost for each affected product was consistent within the available records. The missing values were therefore provisionally imputed using the corresponding observed product-level cost, and the affected records were flagged as imputed.
4. Revenue calculation discrepancies
Revenue was independently validated using:
Units × Unit Price × (1 − Discount)
After deduplication, 22 of the 420 unique transactions did not reconcile between the reported Revenue field and the independently calculated revenue.
Across those mismatches:
Deduplicated reported revenue: ₦46,369,970
Corrected calculated revenue: ₦46,679,725
Difference: ₦309,755
This demonstrated that the reported Revenue field could not be treated as automatically reliable.
Corrected Results
Overall Performance
Metric
Corrected Result
Corrected Revenue
₦46,679,725
Corrected Profit
₦14,590,425
Return Rate
8.60%
Average Discount
17.10%
Unique Transactions
420
Important methodology note: Corrected profit incorporates the documented product-level cost imputation described above. Imputed records remain identifiable in the working analysis.
Management Claim Audit
#
Management Claim
Verdict
Corrected Finding
1
Abuja is the most profitable market
Incorrect
Lagos had the highest corrected profit at ₦4,579,900; Abuja had ₦1,698,100.
2
Electronics is the strongest category and should receive more budget
Misleading
Electronics led revenue and profit, but Accessories had the highest margin at 46.76%. Revenue alone does not establish the budget recommendation.
3
Higher discounting is improving profitability
Incorrect
Observed profit margin declined from 35.69% at 0% discount to 15.29% at 25%.
4
Online has the lowest return rate
Incorrect
In-store had the lowest return rate at 6.44%; Online was 9.70% and WhatsApp 11.90%.
5
August is the strongest sales month
Incorrect
May was strongest at ₦7,008,500; August was weakest at ₦3,167,425.
6
Lagos is underperforming
Incorrect
Lagos had the highest corrected revenue and profit: ₦13,692,700 revenue and ₦4,579,900 profit.
7
Reported Revenue can be used directly
Incorrect
22 of 420 unique transactions failed independent revenue validation.
8
Dashboard is sufficiently reliable without further cleaning
Incorrect
Duplicates, inconsistent labels, missing costs, and revenue discrepancies required correction before decision-making.
Corrected Market Performance
Market
Corrected Profit
Lagos
₦4,579,900
Kano
₦3,243,600
Ibadan
₦2,730,325
Port Harcourt
₦2,338,500
Abuja
₦1,698,100
Lagos was the strongest market by corrected profit, while Abuja recorded the lowest corrected profit.
Corrected Category Performance
Category
Revenue
Profit
Profit Margin
Electronics
₦29,346,500
₦8,986,500
30.62%
Home
₦13,206,300
₦3,674,300
27.82%
Accessories
₦4,126,925
₦1,929,625
46.76%
Electronics generated the largest absolute revenue and profit. However, Accessories produced the highest profit margin. This distinction is important when evaluating the original recommendation to allocate additional budget based primarily on category revenue.
Channel Return Performance
Channel
Return Rate
In-store
6.44%
Online
9.70%
WhatsApp
11.90%
The corrected analysis shows that In-store, not Online, had the lowest return rate.
Monthly Revenue Performance
Month
Corrected Revenue
January
₦6,722,250
February
₦5,364,300
March
₦6,298,725
April
₦6,343,000
May
₦7,008,500
June
₦5,397,250
July
₦6,378,275
August
₦3,167,425
May was the strongest sales month in the corrected analysis, while August was the weakest.
Discount & Profitability Analysis
Observed profit margin by discount level:
Discount
Profit Margin
0%
35.69%
5%
33.01%
10%
28.45%
15%
27.14%
20%
20.79%
25%
15.29%
The observed data shows progressively lower profit margins at higher discount levels.
This is treated as an observed association, not proof of causation. The dataset supports challenging the original claim that higher discounting improves profitability, but it does not by itself establish a causal relationship.
Corrected Dashboard
The final dashboard was designed to retain the general visual pattern of the management dashboard while correcting the underlying analysis.
Dashboard components
Total Revenue KPI
Corrected Profit KPI
Return Rate KPI
Average Discount KPI
Data Quality summary
Market Profitability table and chart
Monthly Revenue table and trend chart
Channel Return Rate table and chart
Category Revenue table and chart
Audited Management Summary
Data-quality indicators displayed on the dashboard
12 duplicates removed
31 costs imputed
22 revenue mismatches identified
The detailed transaction-level audit remains in the supporting Excel workbook rather than overcrowding the management dashboard.
Key Analytical Insights
1. The original dashboard contained conclusions that were not supported by the corrected data
Five of the management claims directly contradicted the corrected analysis, while the Electronics/budget claim was considered misleading because its recommendation could not be established from revenue alone.
2. Revenue validation materially affected the analysis
The reported Revenue field contained discrepancies in 22 unique transactions. Independent recalculation produced corrected revenue of ₦46,679,725.
3. Revenue leadership and margin leadership were different
Electronics led total revenue and profit, but Accessories had the highest profit margin at 46.76%.
4. Discounting requires margin consideration
Observed profit margin declined across the discount levels in the dataset. Higher discounting should therefore not automatically be interpreted as better performance.
5. Data quality is part of business analysis
Duplicate records, inconsistent labels, missing costs, and calculation discrepancies can change management conclusions. Data validation should therefore happen before performance decisions are made.
Management Recommendations
1. Review the discounting strategy
Management should evaluate discount levels against margin outcomes rather than assuming that deeper discounts improve profitability.
2. Evaluate budget allocation using multiple performance measures
Revenue should not be the only basis for budget allocation. Management should consider revenue, absolute profit, profit margin, and return performance together.
3. Strengthen transaction-level data controls
Future reporting should include automated or documented checks for:
duplicate transaction IDs
inconsistent category/market labels
missing product costs
revenue calculation mismatches
other reconciliation exceptions
Limitations & Analytical Notes
The analysis is based only on the supplied dataset and does not establish business causality.
The relationship between discount levels and profit margin is observational.
Missing product costs were imputed using consistent observed product-level costs and flagged accordingly.
Unusual transaction quantities were not automatically removed simply because they appeared high; unusual values require supporting evidence before being classified as errors.
The corrected dashboard is intended to communicate the evidence supported by the supplied transaction data, not to replace additional operational investigation where required.
Repository Structure
Recommended GitHub repository structure:
dsn-ai-bootcamp-2026-dashboard-audit/
│
├── README.md
│
├── data/
│   └── README.md
│
├── dashboard/
│   ├── DSN_Bootcamp_Corrected_Dashboard.xlsx
│   └── dashboard_preview.png
│
├── analysis/
│   ├── data_quality_audit.md
│   ├── claim_audit.md
│   └── corrected_analysis.md
│
├── submission/
│   └── answer_submission_sheet.pdf
│
├── assets/
│   ├── dashboard_overview.png
│   ├── market_performance.png
│   ├── category_performance.png
│   ├── monthly_trend.png
│   └── channel_returns.png
│
└── docs/
    ├── methodology.md
    ├── data_dictionary.md
    └── limitations.md
Recommended handling of the raw dataset
If the DSN Bootcamp dataset is distributed only for the challenge or is not explicitly licensed for public redistribution, do not upload the raw dataset to GitHub.
Instead, data/README.md can state:
The raw dataset was supplied as part of the DSN AI Bootcamp 2026 Data Analytics Track and is not included in this repository. The repository contains the methodology, analysis documentation, and corrected dashboard outputs produced from the supplied dataset.
Project Deliverables
The final repository should contain or link to:
Corrected Excel dashboard
Dashboard screenshot/preview
Data-quality audit documentation
Management claim audit
Corrected analysis
Submission/answer sheet, where appropriate
Methodology and limitations
Clear documentation of assumptions and corrections
Project Outcome
This project demonstrates an audit-first approach to analytics: validate the data before validating the story.
The key lesson from the analysis is that a polished dashboard can still communicate unreliable conclusions when the underlying data and calculations have not been independently validated.
The corrected analysis replaces unsupported management conclusions with evidence-based findings and makes the assumptions, data-quality issues, and limitations visible to decision-makers.
