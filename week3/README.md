# Week 3 — Historical CLTV Calculation & Documentation
**Member:** Osonye Onyemazuwa (branch: hiren)    
**Project:** SaaS/E-Commerce Cohort Retention & CLTV Analysis  
**Organization:** Infotact Solutions  
**Date Range:** 24th – 29th June 2026  
**Status:** 🔄 In Progress  

---

## 🎯 Objective
Calculate the Historical Customer Lifetime Value (CLTV) for each customer  
using AOV (Average Order Value) and Purchase Frequency derived from  
the Online Retail Dataset.

### Core Formula:
> **CLTV = AOV x Purchase Frequency**

---

## 📋 Task Breakdown

| Day | Date | Task | Status |
|---|---|---|---|
| Day 1 | 24th June | Calculate Historical CLTV | ✅ Done |
| Day 2 | 25th June | Project 12-Month CLTV | ⏳ Upcoming |
| Day 3 | 26th June | Customer Segmentation | ⏳ Upcoming |
| Day 4 | 27th June | CAC Calculation | ⏳ Upcoming |
| Day 5 | 28th June | Markdown Documentation | ⏳ Upcoming |
| Day 6 | 29th June | Save CSV & Final Cleanup | ⏳ Upcoming |

---

## 📓 Notebook
**File:** `hiren_cltv.ipynb`

### Steps Covered:
- **Step 1:** Import Libraries & Load Dataset
- **Step 2:** Calculate TotalRevenue (Quantity x UnitPrice)
- **Step 3:** Calculate AOV per customer
- **Step 4:** Calculate Purchase Frequency per customer
- **Step 5:** Compute Historical CLTV = AOV x Purchase Frequency
- **Step 6:** Project 12-Month CLTV ⏳
- **Step 7:** Segment customers (High / Mid / Low Value) ⏳
- **Step 8:** Calculate Maximum Acceptable CAC ⏳
- **Step 9:** Save final output to CSV ⏳

---

## 📊 Key Results (Day 1)

| Metric | Value |
|---|---|
| Total Customers Processed | 4,338 |
| Mean CLTV | £2,048 |
| Median CLTV | £668 |
| Min CLTV | £3.75 |
| Max CLTV | £280,206 |
| Std Deviation | £8,985 |

---

## 📁 Files in This Folder

| File | Description |
|---|---|
| `hiren_cltv.ipynb` | Main CLTV calculation notebook |

---

## ⚠️ Dependency Notes
> **AOV** is officially assigned to Member B (branch: Siva).  
> **Purchase Frequency** is officially assigned to Member C (branch: yash).  
> Both were derived independently here to avoid blocking progress.  
> Fallback calculations are clearly flagged inside the notebook  
> and will be replaced with team outputs once available.

---

## 🛠️ Libraries Used
- Python 3
- Pandas
- NumPy

---

## ➡️ Next Steps
- Complete Days 2–6 tasks as scheduled
- Replace fallback AOV and Purchase Frequency with team outputs
- Save final `hiren_cltv.csv` to `outputs/` folder
- Link results into Week 4 master notebook
