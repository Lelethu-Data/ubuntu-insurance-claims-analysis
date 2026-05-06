# ubuntu-insurance-claims-analysis
End-to-end analytics: Used MySQL on Databricks for cleaning + EDA of 527 claims, then Power BI to uncover R11.96M losses and deliver R4.86M/year savings plan for Ubuntu Insurance

## End-to-End Analytics Pipeline

**1. Data Exploration - MySQL on Databricks**  
Started by investigating the raw dataset to understand structure, data types, distributions, and quality issues. Queried row counts, checked for duplicates, and profiled key fields such as claim amounts, dates, and policy types to get a feel for the data before cleaning. [`01_RAW_data_exploration_databricks_pdf']


**2. Data Cleaning & EDA - MySQL on Databricks**  
Full process documented with code and results screenshots:

- [`02_sql_data_cleaning_databricks.pdf`](documentation/01_Data_Cleaning_Databricks.pdf) - SQL scripts for null handling, date standardization, outlier removal, deduplication based on exploration findings
- [02_EDA_Databricks.pdf](documentation/02_EDA_Databricks.pdf) - Exploratory analysis: fraud rates by province, loss ratios by product, age group distributions

**Key SQL outputs**: Cleaned 527 claims and created aggregated views for fraud_by_province, loss_ratio_by_product, claims_by_age_group used in Power BI.

**3. Visualization & Business Insights - Power BI + DAX**
- Built star-schema data model and DAX measures for loss ratios, fraud percent, claims frequency
- Interactive dashboard with drill-through by province, product, and age for executive team
- 6-slide board presentation with quantified R4.86M per year turnaround plan
