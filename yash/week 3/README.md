28 Jun — Add markdown documentation



\# Member C — Purchase Frequency Analysis



\## Objective

This analysis calculates how frequently each customer purchases from the online retail dataset.



\## Dataset

The analysis uses the cleaned retail dataset containing invoice, customer, transaction date, cohort, quantity, and price information.



\## Methodology



\### 1. Customer Purchase Frequency

Purchase frequency is calculated as the number of unique invoices for each customer.



Formula:



Purchase Frequency = Number of Unique Invoice Numbers per Customer



\### 2. Cohort-Level Purchase Frequency

Customers are grouped using their Cohort Month. The average purchase frequency is calculated for every cohort.



\### 3. Customer Frequency Segments

Customers are divided into three groups:



\- Low Frequency: 1 purchase

\- Medium Frequency: 2 to 4 purchases

\- High Frequency: 5 or more purchases



\### 4. Validation

The analysis validates that:

\- Every customer appears only once in the frequency table.

\- Customer counts match across all outputs.

\- No duplicate Customer ID values exist.

\- Segment totals match the total number of unique customers.



\## Output Files



\- customer\_purchase\_frequency.csv

\- cohort\_purchase\_frequency.csv

\- customer\_frequency\_segments.csv

\- frequency\_segment\_summary.csv

\- validation\_results.csv



\## Contribution

Member C prepared purchase frequency metrics for use in Customer Lifetime Value analysis by Member D.

