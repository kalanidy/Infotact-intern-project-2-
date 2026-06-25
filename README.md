# Osonye Onyemazuwa — Historical CLTV & Documentation
**Branch:** hiren  
**Project:** SaaS/E-Commerce Cohort Retention & Customer Lifetime Value (CLTV) Analysis  
**Organization:** Infotact Solutions  
**Dataset:** Online Retail Dataset (Kaggle)  

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

---

## ✅ Week 2 — Absolute Retained Users
**Date Range:** 12th – 18th June 2026  
**Status:** ✅ Completed

### What Was Done:
- Verified and displayed absolute number of retained users
  for each Month 0, Month 1, Month 2 etc.
- Formatted CohortMonth index to readable date strings
  (e.g. 2010-12, 2011-01)
- Cross-checked absolute numbers are consistent
  and make sense across all cohorts

### Key Output:
- Retained users summary
- Absolute retained users matrix across all cohorts

---

## 🔄 Week 3 — Historical CLTV Calculation
**Date Range:** 24th – 29th June 2026  
**Status:** 🔄 In Progress

### What Was Done So Far:
- Added TotalRevenue column (Quantity x UnitPrice)
- Calculated AOV (Average Order Value) per customer
- Calculated Purchase Frequency per customer
- Computed Historical CLTV = AOV x Purchase Frequency

### In Progress:
- 12-Month CLTV Projection
- Customer Segmentation (High / Mid / Low Value)
- CAC Calculation
- Full markdown documentation
- CSV export

### Key Results (so far):
| Metric | Value |
|---|---|
| Total Customers | 4,338 |
| Mean CLTV | £2,048 |
| Median CLTV | £668 |
| Min CLTV | £3.75 |
| Max CLTV | £280,206 |

### Dependency Note:
> AOV and Purchase Frequency inputs were derived  
> independently pending other members' outputs.  
> Fallback calculations are clearly flagged in the notebook  
> and will be replaced once team outputs are available.

---

## ⏳ Week 4 — To Be Assigned
**Date Range:** 26th June – 4th July 2026  
**Status:** ⏳ Upcoming

### Planned Tasks:
- Task will be assigned by Team Lead at the start of Week 4
- Final integration and reporting expected this week
- Preparation for Final Review presentation

---
## 📁 Folder Structure

```
hiren/
│
├── Week1/
│   └── Untitled.ipynb - Data Cleaning & Validation
│
├── week2/
│   └── WEEK2WORKHIRENUPDATED.ipynb - Absolute Retained Users
│
├── week3/
│   └── hiren_cltv.ipynb - Historical CLTV & Documentation
│
├── outputs/
│   ├── retained_users_summary.csv
│   ├── total_retained_per_month.csv
│   └── hiren_cltv.csv
│
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
- Jupyter Notebook
- Git & GitHub

---

## 📌 Notes
- Tasks are assigned weekly by the Team Leead
- All commits are made to the **hiren** branch only
- Final outputs are saved in the `outputs/` folder
- Kalanidy (Team Lead) handles merging into main branch
