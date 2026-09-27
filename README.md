# DSN AI Bootcamp 2026 — Dashboard Audit & Data Analytics

> **Data Analytics Track | Audit the Dashboard**

A transaction-level data quality audit, dashboard review, and corrected management reporting project completed as part of the **DSN AI Bootcamp 2026 Data Analytics Track**.

The project independently reviews a retail management dashboard and its underlying transaction data, identifies data-quality and calculation issues, tests management's stated conclusions, and produces a corrected Excel dashboard supported by validated analysis.

---

## Project Overview

Management had already received a dashboard containing conclusions about:

- Market profitability
- Category performance
- Discounting
- Sales trends
- Return rates
- Revenue reliability

Rather than reproducing the existing dashboard, this project followed an **audit-first approach**:

**Raw Data → Data Quality Audit → Cleaning & Validation → Claim Testing → Corrected Analysis → Corrected Dashboard → Recommendations**

The objective was to determine what the supplied data actually supports and identify conclusions that should not be relied upon without further validation.

---

## Business Questions

The project audited eight management claims:

1. Is Abuja the most profitable market?
2. Is Electronics the strongest-performing category, and does that justify allocating more budget to it?
3. Does higher discounting improve profitability?
4. Does the Online channel have the lowest return rate?
5. Is August the strongest sales month?
6. Is Lagos underperforming compared with other markets?
7. Can the reported Revenue field be used directly for decision-making?
8. Is the original dashboard sufficiently reliable for management action without further cleaning?

The analysis also addressed five final management questions concerning the most misleading conclusion, the most material correction, business risk, performance drivers, and recommended next actions.

---

# Tools & Methods

### Tools

- Microsoft Excel
- Excel formulas
- Excel structured tables
- Standard Excel charts
- Data validation
- Descriptive analysis

### Analytical methods

- Duplicate detection
- Label standardization
- Missing-value investigation
- Revenue reconciliation
- Product-level cost validation
- Profit calculation
- Market analysis
- Category analysis
- Channel return analysis
- Monthly trend analysis
- Discount-margin analysis
- Management claim auditing

The corrected dashboard was built in **Microsoft Excel using standard tables and charts**. No Power BI or PivotChart-based dashboard was used.

---

# Dataset Audit

## Initial Dataset

| Metric | Result |
|---|---:|
| Raw rows | 432 |
| Unique transactions | 420 |
| Duplicate rows identified | 12 |
| Missing unit-cost records | 31 |
| Revenue mismatches | 22 |

---

## Data Quality Issues Identified

### 1. Duplicate Transactions

The raw dataset contained **432 rows but only 420 unique transaction IDs**.

The 12 duplicated records were exact copies of existing transactions.

These duplicates were removed so that the same transaction would not be counted twice in revenue, profit, units, or other performance calculations.

---

### 2. Inconsistent Market Labels

The same market appeared under inconsistent labels, including:

- `Lagos`
- `Lagos `
- `LAGOS`

These values were standardized to:

`Lagos`

Similar inconsistencies were found in product category labels, including variations of:

- `Accessories`
- `Accessories `
- `accessories`
- `Accessory`

These were standardized to:

`Accessories`

---

### 3. Missing Product Costs

There were **31 cleaned transaction records with missing Cost_Per_Unit_NGN values**.

The available records showed a consistent observed unit cost for each affected product.

The missing costs were therefore provisionally imputed using the corresponding observed product-level cost.

Every imputed record was flagged so that the assumption remained visible during analysis.

### Product-Level Costs Used

| Product | Observed Unit Cost |
|---|---:|
| Backpack | ₦16,000 |
| Blender | ₦28,000 |
| Earbuds | ₦19,000 |
| Electric Kettle | ₦15,000 |
| Phone Case | ₦3,500 |
| Power Bank | ₦15,000 |
| Smartphone | ₦112,000 |
| Standing Fan | ₦39,000 |
| USB Cable | ₦2,200 |

---

### 4. Revenue Calculation Discrepancies

Revenue was independently validated using:

`Units × Unit Price × (1 − Discount)`

After deduplication:

- **420 unique transactions** remained
- **22 transactions** failed revenue validation

Across those 22 mismatches, the reported revenue was **₦309,755 lower** than the independently calculated revenue.

The calculated revenue was therefore used for the corrected analysis, while the original reported revenue was retained for audit comparison.

---

# Corrected Results

## Overall Performance

| Metric | Corrected Result |
|---|---:|
| Corrected Revenue | ₦46,679,725 |
| Corrected Profit | ₦14,590,425 |
| Return Rate | 8.60% |
| Average Discount | 17.10% |
| Unique Transactions | 420 |

### Data Quality Indicators

| Issue | Count |
|---|---:|
| Duplicate rows removed | 12 |
| Costs imputed | 31 |
| Revenue mismatches | 22 |

> Corrected profit incorporates the documented product-level cost imputation described in this project.

---

# Management Claim Audit

| # | Management Claim | Verdict | Corrected Finding |
|---|---|---|---|
| 1 | Abuja is the most profitable market | **Incorrect** | Lagos had the highest corrected profit at ₦4,579,900, while Abuja had ₦1,698,100. |
| 2 | Electronics is the strongest category and should receive more budget | **Misleading** | Electronics led revenue and profit, but Accessories had the highest profit margin at 46.76%. Revenue alone does not establish the budget recommendation. |
| 3 | Higher discounting is improving profitability | **Incorrect** | Observed profit margin declined from 35.69% at 0% discount to 15.29% at 25% discount. |
| 4 | Online has the lowest return rate | **Incorrect** | In-store had the lowest return rate at 6.44%. Online was 9.70% and WhatsApp was 11.90%. |
| 5 | August is the strongest sales month | **Incorrect** | May was the strongest month at ₦7,008,500. August was the weakest at ₦3,167,425. |
| 6 | Lagos is underperforming | **Incorrect** | Lagos recorded the highest corrected revenue and profit. |
| 7 | Reported Revenue can be used directly | **Incorrect** | 22 of 420 unique transactions failed independent revenue validation. |
| 8 | The dashboard is sufficiently reliable without further cleaning | **Incorrect** | Duplicate records, inconsistent labels, missing costs, and revenue discrepancies required correction. |

---

# Corrected Market Performance

| Market | Corrected Profit |
|---|---:|
| Lagos | ₦4,579,900 |
| Kano | ₦3,243,600 |
| Ibadan | ₦2,730,325 |
| Port Harcourt | ₦2,338,500 |
| Abuja | ₦1,698,100 |

Lagos recorded the highest corrected profit, while Abuja recorded the lowest corrected profit among the five markets.

---

# Corrected Category Performance

| Category | Revenue | Profit | Profit Margin |
|---|---:|---:|---:|
| Electronics | ₦29,346,500 | ₦8,986,500 | 30.62% |
| Home | ₦13,206,300 | ₦3,674,300 | 27.82% |
| Accessories | ₦4,126,925 | ₦1,929,625 | **46.76%** |

Electronics generated the largest absolute revenue and profit.

However, Accessories recorded the highest profit margin.

This distinction matters when evaluating the original recommendation to allocate additional budget primarily based on category performance.

---

# Channel Return Performance

| Channel | Return Rate |
|---|---:|
| In-store | 6.44% |
| Online | 9.70% |
| WhatsApp | 11.90% |

The corrected analysis does not support the original claim that Online had the lowest return rate.

---

# Monthly Revenue Performance

| Month | Corrected Revenue |
|---|---:|
| January | ₦6,722,250 |
| February | ₦5,364,300 |
| March | ₦6,298,725 |
| April | ₦6,343,000 |
| May | ₦7,008,500 |
| June | ₦5,397,250 |
| July | ₦6,378,275 |
| August | ₦3,167,425 |

May recorded the highest corrected monthly revenue.

August recorded the lowest.

---

# Discount & Profitability Analysis

Observed profit margin by discount level:

| Discount | Profit Margin |
|---:|---:|
| 0% | 35.69% |
| 5% | 33.01% |
| 10% | 28.45% |
| 15% | 27.14% |
| 20% | 20.79% |
| 25% | 15.29% |

The dataset shows an association between higher discount levels and lower observed profit margins.

This is an **observational relationship**, not proof that discounting alone causes the decline.

---

# Key Analytical Insights

### 1. The original dashboard contained unsupported conclusions

Several management claims contradicted the corrected analysis, while the Electronics budget claim was considered misleading because the recommendation could not be established from revenue alone.

### 2. Revenue validation materially affected the analysis

The reported Revenue field contained discrepancies in 22 unique transactions.

Independent recalculation produced corrected revenue of:

**₦46,679,725**

### 3. Revenue leadership and margin leadership were different

Electronics generated the highest absolute revenue and profit.

Accessories generated the highest profit margin at:

**46.76%**

### 4. Discounting requires margin consideration

Observed profit margin declined across the discount levels in the dataset.

Higher discounting should therefore not automatically be interpreted as better performance.

### 5. Data quality directly affects business analysis

Duplicate records, inconsistent labels, missing costs, and calculation discrepancies can change management conclusions.

Data validation should therefore occur before performance decisions are made.

---

# Final Management Questions

## 1. Most misleading original conclusion

The conclusion that **higher discounting was improving profitability** was particularly misleading because the corrected analysis showed observed profit margin declining from **35.69% at 0% discount to 15.29% at 25% discount**.

---

## 2. Most material change after correction

The most material change was the reliability of revenue and profit calculations.

After deduplication:

- Reported revenue: **₦46,369,970**
- Corrected calculated revenue: **₦46,679,725**
- Difference: **₦309,755**

Corrected profit was:

**₦14,590,425**

---

## 3. Greatest business risk

Acting on unvalidated revenue figures and the assumption that higher discounts improve profitability could lead to pricing and resource-allocation decisions that reduce margins or rely on inaccurate performance measurements.

---

## 4. Important performance driver

The analysis highlights the relationship between **sales volume, revenue, profitability, and discounting**.

Electronics generated substantial revenue and profit, but its higher absolute performance should be considered alongside profit margin and return performance.

---

## 5. Recommended Actions

### 1. Review the discounting strategy

Evaluate discount levels against profit margins rather than assuming deeper discounts improve performance.

### 2. Use multiple performance measures for budget allocation

Evaluate:

- Revenue
- Absolute profit
- Profit margin
- Return rate

rather than relying on revenue alone.

### 3. Strengthen transaction-level data controls

Future reporting should include checks for:

- Duplicate transaction IDs
- Inconsistent market and category labels
- Missing product costs
- Revenue calculation mismatches
- Other reconciliation exceptions

---

# Corrected Dashboard

The final dashboard was developed in Microsoft Excel and focuses on:

- Overall business KPIs
- Market performance
- Category performance
- Monthly revenue trends
- Channel return rates
- Profitability
- Data-quality indicators

### Dashboard Preview

![Audited Management Dashboard](assets/dashboard_overview.jpg)
