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

## Date
1 July

## Task
Create a single cohort retention decay line chart in Power BI.

## Work Done
- Created Customer Cohort table.
- Merged cohort data with the retail dataset.
- Calculated `CohortIndex`.
- Created `Retained Customers` measure.
- Built a single cohort retention line chart.
- Added chart title and axis labels.

## Tools
- Power BI
- Power Query
- DAX

## Output
A line chart showing customer retention for a single cohort over time.

## Next
Overlay multiple cohort retention curves on one chart.

# Member B - Multi Cohort Retention Comparison

## Date
2 July

## Task
Overlay multiple cohort retention curves on a single line chart for side-by-side comparison.

## Work Done
- Removed the single cohort filter.
- Added `CohortMonth` as the chart legend.
- Displayed multiple cohort retention curves.
- Compared customer retention across different cohorts.
- Improved chart readability for analysis.

## Tools
- Power BI
- Power Query
- DAX

## Output
A multi-line retention chart comparing customer retention behavior across multiple customer cohorts.

# Member B - Chart Formatting

## Date
3 July

## Task
Improve the formatting and presentation of retention charts.

## Work Done
- Updated chart titles.
- Added axis labels.
- Enabled markers.
- Improved line width.
- Added gridlines.
- Formatted legends.
- Improved dashboard layout.

## Tools
- Power BI

## Output
Professional and presentation-ready customer retention charts