# SaaS/E-Commerce Cohort Retention & Customer Lifetime Value (CLTV) Analysis
**Organization:** Infotact Solutions  
**Program:** Data Analytics Internship — Project 2  
**Batch:** 18    -     **Group:** 4  
**Dataset:** Online Retail Dataset (Kaggle)  
**Analysis Period:** December 2010 — December 2011  

---

## 📋 Project Overview
This project performs a deep-dive Cohort Analysis to understand 
user retention patterns and calculate Customer Lifetime Value (CLTV) 
for an e-commerce business. By grouping customers based on their 
acquisition month, we identify exactly when customers churn and 
provide data-backed recommendations to improve retention and 
maximize profitability.

### ❓ Business Problem
Acquiring new customers is up to **5 times more expensive** than 
retaining existing ones. High-growth businesses often focus on 
rapid customer acquisition but fail to track whether those customers 
actually stick around. This analysis answers three critical questions:

- When do customers typically stop purchasing?
- Which customer segments and geographic regions generate the most value?
- What is the maximum amount we should spend to acquire a customer profitably?

---

## 🎯 Project Objectives
1. Build a Cohort Retention Matrix showing absolute and percentage retained users
2. Calculate Historical and 12-Month Projected CLTV per customer and cohort segment
3. Segment customers into High, Mid and Low value groups
4. Calculate maximum acceptable Customer Acquisition Cost (CAC)
5. Visualize retention trends using heatmaps and decay curves
6. Provide strategic data-backed recommendations to reduce churn

---

## 👥 Team Structure

| Member | Branch | Role |
|---|---|---|
| Kalanidy A | kalanidy | Team Lead |
| Khatri Yash Manishbhai | yash | Team Member |
| Sontipala Siva Shankar | siva | Team Member |
| Osonye Onyemazuwa | hiren | Team Member |

### Weekly Task Distribution:

| Week | Yash | Hiren | Kalanidy | Siva |
|---|---|---|---|---|
| Week 1 | Data Ingestion & Filtering | Data Cleaning & Validation | Cohort Month Calculation | Documentation |
| Week 2 | Cohort Retention Matrix | Absolute Retained Users | Percentage Retention Rate & Documentation | Cohort Grouping (groupby) |
| Week 3 | Purchase Frequency | Historical CLTV & Documentation | Revenue Calculation & Cohort Segmentation | AOV Calculation |
| Week 4 | Cohort Retention Heatmap | README & Business Implications | Retention Decay Line Charts | Full Notebook Integration and cleanup |

---

## 🔗 Dataset Source
**Online Retail Dataset — Kaggle**  
https://www.kaggle.com/datasets/vijayuv/onlineretail

| Detail | Value |
|---|---|
| Original Records | 541,909 rows |
| Cleaned Records | 392,692 rows |
| Records Removed | 149,217 rows (27.3%) |
| Columns | 8 |
| Date Range | December 2010 — December 2011 |
| Unique Customers | 4,338 |
| Key Columns | CustomerID, InvoiceNo, Quantity, UnitPrice, InvoiceDate, Country, CohortMonth |

> ⚠️ Raw data files are excluded from this repository per data privacy guidelines.  
> Download the dataset from the Kaggle link above and place it in a local `data/` folder.

---

## 📊 Week 1: Data Cleaning & Validation

### What Was Done:
- Filtered out all cancelled transactions (invoices starting with 'C')
- Removed rows with missing CustomerIDs
- Validated and converted data types (dates, quantities, prices)
- Flagged and removed all negative quantities and prices
- Calculated CohortMonth (month of first purchase) for every unique customer
- Calculated TransactionMonth and CohortIndex for cohort tracking

### Results After Cleaning:
| Metric | Value |
|---|---|
| Original Dataset | 541,909 rows |
| After Removing Cancelled Transactions | ~530,000 rows |
| After Removing Null CustomerIDs | 392,692 rows |
| Records Removed | 149,217 rows (27.3%) |
| Unique Customers | 4,338 |

### 💡 Business Implication:
> Over 27% of raw transactions were invalid — cancelled, missing customer
> data, or containing negative values. This highlights the critical
> importance of data validation before making any business decisions
> from raw transactional data. A business making decisions on uncleaned
> data risks misallocating resources based on false information.

---

## 📊 Week 2: Cohort Retention Analysis

### What Was Done:
- Grouped customers into cohorts based on first purchase month
- Built absolute retention matrix using Pandas pivot_table
- Formatted CohortMonth to readable date strings (e.g. 2010-12, 2011-01)
- Verified absolute numbers are consistent across all cohorts
- Calculated percentage retention rates per cohort per month

### Key Retention Results:
| Metric | Value |
|---|---|
| Overall Average Month 1 Retention | 13.30% |
| Biggest Drop Off | Month 0 → Month 1 (-86.70%) |
| Best Performing Cohort | December 2010 (19.72%) |
| Worst Performing Cohort | March 2011 (7.26%) |
| Month 12 Retention | 27.17% |

### 📉 Key Finding 1 — Massive Early Churn:
> **86.70% of customers do not return after their first purchase.** 
> Only 13.30% of customers make a second purchase in the month 
> following their first transaction. This is the single biggest 
> retention problem for this business.

### 📉 Key Finding 2 — Seasonal Cohort Performance:
> The **December 2010 cohort** performed best with 19.72% Month 1 
> retention — likely driven by Christmas shopping behaviour where 
> customers returned for post-holiday purchases.  
> The **March 2011 cohort** performed worst at just 7.26% — 
> suggesting seasonal drop-off after the holiday period.

### 📈 Key Finding 3 — Long-Term Loyal Customers:
> Despite the massive early churn, customers who survive past Month 3
> show **increasing** retention — reaching **27.17% by Month 12.** 
> This indicates a core group of highly loyal customers who are 
> extremely valuable to the business.

### 🎯 Retention Recommendations:
| Recommendation | Action | Expected Impact |
|---|---|---|
| Re-engagement Email | Automated email 7 days after first purchase | Reduce Month 1 churn by 15-20% |
| First Purchase Incentive | 10% discount on second purchase | Increase Month 1 retention |
| December Campaign | Increase ad spend in November-December | Acquire higher quality cohorts |
| Loyalty Program | Reward customers returning past Month 3 | Protect long-term loyal customers |

---

## 📊 Week 3: Customer Lifetime Value (CLTV) Calculation

### What Was Done:
- Calculated TotalRevenue per transaction (Quantity x UnitPrice)
- Calculated Average Order Value (AOV) per customer
- Calculated Purchase Frequency per customer
- Computed Historical CLTV = AOV x Purchase Frequency
- Projected 12-Month CLTV per cohort segment
- Segmented customers into High, Mid and Low value groups
- Calculated maximum acceptable CAC (30% of 12-Month CLTV)
- Performed Geographic CLTV analysis by country

### Key CLTV Results:
| Metric | Value |
|---|---|
| Total Customers Analysed | 4,338 |
| Overall Mean Historical CLTV | $2,048 |
| Median CLTV | $668 |
| Min CLTV | $3.75 |
| Max CLTV | $280,206 |
| Overall Mean 12-Month CLTV | $24,584 |
| Overall Mean Max CAC | $7,375 |

### Customer Segmentation by CLTV:
| Segment | 12-Month CLTV | Max CAC | Customer Count |
|---|---|---|---|
| High Value | $77,835 | $23,350 | 1,085 (25%) |
| Mid Value | $9,168 | $2,750 | 2,168 (50%) |
| Low Value | $2,136 | $640 | 1,085 (25%) |

### Top 10 Countries by Average CLTV:
| Rank | Country | Average CLTV |
|---|---|---|
| 1 | Netherlands | $246,720 |
| 2 | EIRE | $135,489 |
| 3 | Australia | $76,919 |
| 4 | Singapore | $21,279 |
| 5 | Sweden | $14,774 |
| 6 | Japan | $14,054 |
| 7 | United Kingdom | $7,780 |
| 8 | Norway | $7,424 |
| 9 | France | $6,082 |
| 10 | Germany |$5,484 |

### 💡 Key Finding 1 — High Value Customer Concentration:
> Only **25% of customers (1,085)** fall into the High Value segment 
> but generate an average 12-Month CLTV of **$77,835** — nearly 9x 
> more than Mid Value customers. These customers are critical to 
> protect and retain at all costs.

### 💡 Key Finding 2 — Geographic Concentration:
> **Netherlands and EIRE** customers generate significantly higher 
> CLTV than the United Kingdom despite the UK having far more customers. 
> International customers represent a high-value but underutilised 
> market segment with massive growth potential.

### 💡 Key Finding 3 — CAC Efficiency by Segment:
> The business can afford to spend up to **$23,350** to acquire 
> a High Value customer while remaining profitable. 
> Low Value customers only justify a maximum CAC of **$640.** 
> Mixing these budgets leads to significant marketing waste.

### 🎯 CLTV Recommendations:
| Recommendation | Action | Expected Impact |
|---|---|---|
| Protect High Value Customers | VIP program for top 25% | Reduce churn in most valuable segment |
| Target Netherlands & EIRE | Increase marketing in high CLTV regions | Higher ROI on acquisition spend |
| Optimize CAC by Segment | Set separate ad budgets per segment | Avoid overspending on Low Value |
| Upsell Mid Value Customers | Target 2,168 Mid Value customers | Move them into High Value segment |
| Geographic Expansion | Focus on Singapore, Sweden, Japan | Untapped high CLTV markets |

---

## 📊 Week 4: Visualization & Strategic Insights

### Cohort Retention Heatmap
*(To be updated with findings from Yash)*

> Visualization shows retention rates across all cohorts 
> using a colour-coded heatmap built with Seaborn/Power BI.

### Retention Decay Line Charts
**Tool:** Power BI  
**Cohort Analysed:** December 2010 cohort

#### Key Findings:
- Original cohort size at Month 0: 644 customers
- Retention dropped sharply to 122 customers by Month 1
- This represents a **~79% drop** in the first month alone
- Retention stabilized between Month 2 and Month 5 at around 120-150 customers
- A minor downward fluctuation was observed at **Month 6** and **Month 7** before recovery
- Despite the Month 7 dip, an overall gradual recovery trend continued
- By Month 12 retained customers increased to approximately 200 customers
- This suggests a loyal core group of customers who become increasingly 
  engaged over time

#### 💡 Business Implication:
> The December 2010 cohort shows the classic e-commerce retention pattern —
> massive early churn followed by stabilization among loyal customers.
> The minor dip at Month 7 may indicate a **seasonal drop-off** possibly
> linked to summer spending behaviour or competitor promotions.
> The overall recovery trend from Month 5 to Month 12 is encouraging
> and suggests customers who survive past Month 5 are highly likely
> to remain long-term loyal customers.

#### 🎯 Recommendations:
> 1. Focus retention efforts on the critical **first 30 days** after
>    acquisition to reduce the massive Month 0 → Month 1 drop.
> 2. Implement a targeted **Month 7 re-engagement campaign** to address
>    the seasonal dip and prevent further churn at that point.
> 3. Reward customers who reach **Month 5+** with a loyalty incentive
>    to accelerate the recovery trend.

---

## 🎯 Overall Strategic Recommendations

Based on the full analysis across all 4 weeks:

### Priority 1 — Fix Early Churn (Urgent)
> **86.70% churn after first purchase is the #1 business problem.** 
> Implement an automated re-engagement email sequence triggered 
> 7 days after a customer's first purchase with a 10% discount 
> incentive for their second purchase.

### Priority 2 — Protect High Value Customers
> 25% of customers generate the vast majority of revenue.  
> Implement a VIP loyalty program with exclusive benefits 
> for customers with 12-Month CLTV above £19,927 (75th percentile).

### Priority 3 — Optimize Marketing Spend by Segment
> Never spend more than £23,350 acquiring a High Value customer 
> and never more than £640 acquiring a Low Value customer.  
> Set separate acquisition budgets per customer segment.

### Priority 4 — Geographic Expansion
> Netherlands (£246,720 avg CLTV) and EIRE (£135,489 avg CLTV) 
> customers are 31x and 17x more valuable than UK customers.  
> Increase marketing investment in these markets immediately.

### Priority 5 — Seasonal Campaign Strategy
> December cohorts consistently outperform all other months.  
> Maximise acquisition budget in November-December every year 
> to acquire the highest quality highest retention cohorts.

### Priority 6 — 30-Day Onboarding Sequence (Urgent)
> The December 2010 cohort shows ~79% of customers churn within
> the first month. Implement a structured 30-day onboarding sequence
> with weekly email touchpoints to guide new customers through
> their critical first 4 weeks after acquisition.  
> A customer retained past Month 1 is significantly more likely
> to become a long-term loyal customer.

### Priority 7 — Month 7 Re-engagement Campaign
> Data shows a minor but consistent downward fluctuation at Month 6 and
> month 7 across cohorts — possibly linked to seasonal spending behaviour
> or competitor promotions during that period.  
> Implement a targeted re-engagement campaign at Month 6 with
> exclusive offers to prevent this predictable churn point.

---

## 📁 Repository Structure

```
main/
│
├── yash/
|   ├── week 1/
|   ├── week 2/
|   ├── week 3/
│   └── week 4/
│
├── hiren/
|   ├── week 1/
|   ├── week 2/
|   ├── week 3/
│   └── week 4/
|
├── kalanidy/
|   ├── week 1/
|   ├── week 2/
|   ├── week 3/
│   └── week 4/
|
├── siva/
|   ├── week 1/
|   ├── week 2/
|   ├── week 3/
│   └── week 4/
│
└── README.md
```

---

## 🛠️ Tools & Libraries
| Tool | Purpose |
|---|---|
| Python 3 | Core programming language |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical computations |
| OS | File and directory management |
| Seaborn | Cohort retention heatmap |
| Matplotlib | Retention decay line charts |
| Power BI | Interactive dashboard |
| Jupyter Notebook | Interactive development |
| Git & GitHub | Version control and collaboration |

---

## 📌 Important Notes
- All commits made to individual branches only
- Raw CSV data files excluded from GitHub via .gitignore
- Team Lead (Kalanidy) or hiren handles merging into main branch
- Final Review: 5th — 10th July 2026
