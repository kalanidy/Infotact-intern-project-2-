# Retention Decay Line Charts - Member B

## Project
Infotact Intern Project 2 - Week 3

## Branch
member-b

## Date
30 June

## Task
Load retention dataset and set up the Power BI environment for retention decay visualization.

## Objective
Prepare the retail transaction dataset for cohort retention analysis by importing it into Power BI, validating the data, and creating the required preprocessing steps for future visualization.

## Work Completed

- Imported the cleaned retail transaction dataset into Power BI.
- Promoted the first row as column headers.
- Assigned appropriate data types to all columns.
- Filtered invalid or blank Customer IDs (if present).
- Created the `InvoiceMonth` column from `InvoiceDate`.
- Loaded the transformed data into the Power BI data model.
- Saved the Power BI report for future visualization tasks.

## Dataset

Retail transaction dataset containing:

- Invoice Number
- Stock Code
- Product Description
- Quantity
- Invoice Date
- Unit Price
- Customer ID
- Country

## Tools Used

- Microsoft Power BI Desktop
- Power Query Editor

## Deliverables

- Retention_Decay.pbix
- Cleaned retail dataset
- Power Query transformations

## Next Task (1 July)

Create a single cohort retention decay line chart using the prepared dataset.

## Git Commit

```bash
git commit -m "viz: load retention matrix and set up Power BI environment (fixes #18)"
```

## Author

A. Kalanidy
Infotact Data Analytics Internship