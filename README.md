# ubuntu-insurance-claims-analysis
End-to-end analytics: Used MySQL on Databricks for cleaning + EDA of 527 claims, then Power BI to uncover R11.96M losses and deliver R4.86M/year savings plan for Ubuntu Insurance

## End-to-End Analytics Pipeline

**1. Data Exploration - MySQL on Databricks**  
Started by investigating the raw dataset to understand structure, data types, distributions, and quality issues. Queried row counts, checked for duplicates, and profiled key fields such as claim amounts, dates, and policy types to get a feel for the data before cleaning. [`01_RAW_data_exploration_databricks.pdf`]


**2. Data Cleaning  - MySQL on Databricks**  
Full process documented with code and results screenshots:

- [`02_sql_data_cleaning_databricks.pdf`] - SQL scripts for null handling, date standardization, outlier removal, and deduplication based on exploration findings

**Key SQL outputs**: Cleaned 527 claims and created aggregated views for fraud_by_province, loss_ratio_by_product, claims_by_age_group used in Power BI.

**3. Visualization & Business Insights - Power BI + DAX**
- Built a star-schema data model and DAX measures for loss ratios, fraud percent, and claims frequency
- Interactive dashboard with drill-through by province, product, and age for the executive team
- 6-slide board presentation with quantified R4.86M per year turnaround plan
  ## Key Findings from 527 Claims
Total loss: **R11.96M over 21 months = R535K/month**

| Finding | Impact |
| --- | --- |
| **Life policies** pay R47 in claims per R1 premium | -R4.49M loss |
| **KZN Home claims** = 71% of all fraud cases | -R2.18M fraud total |
| **Ages 25-44** = 63% of all losses | -R7.55M loss |

##  Recommendations Delivered
**Total Savings: R405K/month = R4.86M per year**

1. **Pause + Redesign Life/Funeral** → Save R249K/mo
2. **Biometric Checks for KZN Home** → Save R71K/mo  
3. **Age-Based Pricing for 25-44** → Save R85K/mo

##  Dashboard Preview
<img width="616" height="444" alt="Lelethu_Bala_dfa_final_project_Dashboard_Screenshot" src="https://github.com/user-attachments/assets/2107fdad-2bf4-4a51-a1ea-350ffda7d2af" />

