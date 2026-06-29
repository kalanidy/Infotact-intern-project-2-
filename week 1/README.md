## Week 1: Data Cleaning and Validation

### Project Objective

The objective of this project is to prepare the Online Retail dataset for Cohort Analysis by ensuring data quality, consistency, and completeness.

### Team Responsibilities

#### Member A – Data Ingestion & Filtering

* Loaded the Online Retail dataset into a Pandas DataFrame.
* Removed refunded/cancelled transactions (InvoiceNo starting with 'C').
* Removed rows with missing CustomerID values.

#### Member B – Data Cleaning & Validation

* Handled missing values.
* Removed duplicate records.
* Validated data types (InvoiceDate, Quantity, UnitPrice).
* Removed records containing negative quantities or prices.

#### Member C – Cohort Month Calculation

* Extracted transaction month from InvoiceDate.
* Calculated each customer's first purchase month (Cohort Month).
* Merged Cohort Month back into the dataset.

#### Member D – Documentation & QA

* Documented all cleaning and preprocessing steps.
* Verified row counts before and after cleaning.
* Performed validation checks.
* Prepared summary reports for Week 1.

### Dataset

Online Retail Dataset

### Dataset Source

* Kaggle

### Dataset Link

* https://www.kaggle.com/datasets/vijayuv/onlineretail

### Tools Used

* Python
* Pandas
* Jupyter Notebook
* GitHub

### Week 1 Deliverables

* Cleaned dataset
* Validation report
* Cohort preparation documentation
* GitHub commit history
