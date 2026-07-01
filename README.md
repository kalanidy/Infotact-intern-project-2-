# Osonye Onyemazuwa — Historical CLTV & Documentation
**Branch:** hiren  
**Project:** SaaS/E-Commerce Cohort Retention & Customer Lifetime Value (CLTV) Analysis  
**Organization:** Infotact Solutions  
## 🔗 Dataset Source
**Online Retail Dataset — Kaggle**
https://www.kaggle.com/datasets/vijayuv/onlineretail

> Raw data files are excluded from this repository per data privacy guidelines.  
> Download the dataset from the link above and place it in a local `data/` folder to run the notebooks.  

---

## 👤 About This Branch
This branch contains all contributions by Osonye Onyemazuwa to the team project.    
Tasks are distributed every week across all team members 
by the Team Lead to ensure balanced contribution 
and full project coverage.

---

## ✅ Week 1 — Data Cleaning & Validation
**Date Range:** 5th – 11th June 2026  
**Status:** ✅ Completed

### What Was Done:
- Handled missing values and removed duplicate rows
- Validated data types (dates, quantities, prices)
- Flagged and removed negative quantities and prices

### Key Output:
- Clean dataset ready for cohort analysis
- Saved as `cleaned_retail_data.csv`

### 💡 Business Implication:
> Over 27% of raw transactions were invalid — cancelled, missing
> customer data, or containing negative values. This highlights
> the critical importance of data validation before making
> any business decisions from raw transactional data.

---

## ✅ Week 2 — Absolute Retained Users
**Date Range:** 12th – 18th June 2026  
**Status:** ✅ Completed

### What Was Done:
- Verified and displayed absolute number of retained users
  for each Month 0, Month 1, Month 2 etc.
- Formatted CohortMonth index to readable date strings
  (e.g. 2010-12, 2011-01)
- Cross-checked absolute numbers are consistent and
  make sense across all cohorts
- Calculated percentage retention rates
- Saved all outputs locally

### Key Output:
- Retained users summary
- Absolute retained users matrix across all cohorts

### Key Results:
| Metric | Value |
|---|---|
| Overall Average Month 1 Retention | 13.30% |
| Biggest Drop Off | Month 0 → Month 1 (-86.70%) |
| Best Performing Cohort | December 2010 (19.72%) |
| Worst Performing Cohort | March 2011 (7.26%) |
| Month 12 Retention | 27.17% |

### 💡 Key Findings:

**Finding 1 — Massive Early Churn:**
> 86.70% of customers do not return after their first purchase.
> Only 13.30% of customers make a second purchase in the
> month following their first transaction.

**Finding 2 — Seasonal Cohort Performance:**
> The December 2010 cohort performed best at 19.72% Month 1
> retention — likely driven by Christmas shopping behaviour.
> The March 2011 cohort performed worst at just 7.26%.

**Finding 3 — Long-Term Loyal Customers:**
> Despite massive early churn, customers who survive past
> Month 3 show increasing retention — reaching 27.17% by Month 12.
> This indicates a highly valuable core group of loyal customers.

### 🎯 Recommendations:
| Recommendation | Action | Expected Impact |
|---|---|---|
| Re-engagement Email | Send automated email 7 days after first purchase | Reduce Month 1 churn by 15-20% |
| First Purchase Incentive | Offer 10% discount on second purchase | Increase Month 1 retention |
| December Campaign | Increase ad spend in November-December | Acquire higher quality cohorts |
| Loyalty Program | Reward customers who return past Month 3 | Protect long-term loyal customers |

---

## 🔄 Week 3 — Historical CLTV Calculation
**Date Range:** 24th – 29th June 2026  
**Status:** ✅ Completed

### What Was Done So Far:
- Added TotalRevenue column (Quantity x UnitPrice)
- Calculated AOV (Average Order Value) per customer
- Calculated Purchase Frequency per customer
- Computed Historical CLTV = AOV x Purchase Frequency
- Projected 12-Month CLTV per cohort segment
- Segmented customers into High, Mid and Low value groups
- Calculated maximum acceptable CAC (30% of CLTV)
- Performed Geographic CLTV analysis by country

### Key Results:
| Metric | Value |
|---|---|
| Total Customers Analysed | 4,338 |
| Overall Mean CLTV | £2,048 |
| Median CLTV | £668 |
| Min CLTV | £3.75 |
| Max CLTV | £280,206 |
| Overall Mean 12-Month CLTV | £24,584 |
| Overall Mean Max CAC | £7,375 |

### Customer Segmentation:
| Segment | 12-Month CLTV | Max CAC | Customers |
|---|---|---|---|
| High Value | £77,835 | £23,350 | 1,085 |
| Mid Value | £9,168 | £2,750 | 2,168 |
| Low Value | £2,136 | £640 | 1,085 |

### Top 5 Countries by Average CLTV:
| Country | Average CLTV |
|---|---|
| Netherlands | £246,720 |
| EIRE | £135,489 |
| Australia | £76,919 |
| Singapore | £21,279 |
| Sweden | £14,774 |

### 💡 Key Findings:

**Finding 1 — High Value Customers:**
> Only 25% of customers (1,085) fall into the High Value segment
> but they generate an average 12-Month CLTV of £77,835 —
> nearly 9x more than Mid Value customers.
> These customers are critical to protect and retain.

**Finding 2 — Geographic Concentration:**
> Netherlands and EIRE customers generate significantly higher
> CLTV than the United Kingdom despite the UK having far more
> customers. International customers represent a high-value
> but underutilised market segment.

**Finding 3 — CAC Efficiency:**
> The business can afford to spend up to £23,350 to acquire
> a High Value customer while remaining profitable.
> Low Value customers only justify a maximum CAC of £640.

### 🎯 Recommendations:
| Recommendation | Action | Expected Impact |
|---|---|---|
| Protect High Value Customers | VIP program for top 25% | Reduce churn in most valuable segment |
| Target Netherlands & EIRE | Increase marketing in high CLTV countries | Higher ROI on acquisition spend |
| Optimize CAC by Segment | Set separate ad budgets per segment | Avoid overspending on Low Value acquisition |
| Upsell Mid Value Customers | Target 2,168 Mid Value customers | Move them into High Value segment |

### Dependency Note:
> AOV and Purchase Frequency inputs were derived  
> independently pending other members' outputs.  
> Fallback calculations are clearly flagged in the notebook  
> and will be replaced once team outputs are available.

---

## 🔄 Week 4 — README & Business Implications Report
**Date Range:** 30th June – 4th July 2026  
**Status:** 🔄 In Progress

### What Was Done So Far:
- Extracted real business findings from all weeks
- Started final project README
- Added Week 1 & 2 business implications

### In Progress:
- Week 3 CLTV findings documentation
- Strategic recommendations report
- Final repo structure organisation

### Planned Deliverables:
- Complete project README with all business implications
- Data-backed recommendations to reduce churn
- Final GitHub repo structure organised and verified

---

## 📁 Folder Structure:

```
hiren/
│
├── week 1/
│   └── data_cleaning_validation.ipynb - Data Cleaning & Validation
│
├── week 2/
│   └── absolute_retained_users.ipynb - Absolute Retained Users
│
├── week 3/
│   └── hiren_cltv.ipynb - Historical CLTV & Documentation
|
├── week 4/
│   └── README.md
|
├── outputs/
│   ├── .gitkeep
│
├── .gitignore
|
└── README.md
```

---

## 📊 Dataset Info
| Detail | Value |
|---|---|
| Source | Online Retail Dataset — Kaggle |
| Rows | 392,692 |
| Columns | 10 |
| Key Columns | CustomerID, InvoiceNo, Quantity, UnitPrice, InvoiceDate, CohortMonth |

---

## 🛠️ Tools & Libraries
- Python 3
- Pandas
- NumPy
- os
- Jupyter Notebook
- Git & GitHub

---

## 📌 Notes
- Tasks are assigned weekly by the Team Lead
- All commits are made to the **hiren** branch only
- Final outputs are saved in the `outputs/` folder
- Team Lead handles merging into main branch
