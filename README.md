# powerbi-final-project

Interactive Power BI report for class project — visualizing procedure-level revenue trends over time with filters and calculated measures.

## Files Included

- [Final – MMC HB Aged Trial Balance – Details.pbix](./Final%20–%20MMC%20HB%20Aged%20Trial%20Balance%20–%20Details.pbix) – Details report for aged trial balances  
- [Final – MMC HB Aged Trial Balance – Summary.pbix](./Final%20–%20MMC%20HB%20Aged%20Trial%20Balance%20–%20Summary.pbix) – Summary version of aged trial balances  
- [Final – MMC HB Custom Payments and Adjustments – Details.pbix](./Final%20–%20MMC%20HB%20Custom%20Payments%20and%20Adjustments%20–%20Details.pbix) – Adjustment and payments report  
- [Final-MMC HB Method 2 Posted Charges.pbix](./Final-MMC%20HB%20Method%202%20Posted%20Charges.pbix) – Posted charges report  
- [Final-MMC YTD and MTD Rev.pbix](./Final-MMC%20YTD%20and%20MTD%20Rev.pbix) – Revenue trends (MTD/YTD)  
- [WIP-MMC HB HAR Admissions and Discharges.pbix](./WIP-MMC%20HB%20HAR%20Admissions%20and%20Discharges.pbix) – In-progress HAR-level admissions and discharges  
- [WIP-MMC 340B Medicaid Patients.pbix](./WIP-MMC%20340B%20Medicaid%20Patients.pbix) – In-progress 340B eligibility and Medicaid patient report  
- [WIP MMC HB Patient Days by Bed Charge and Service Data – Details.pbix](./WIP%20MMC%20HB%20Patient%20Days%20by%20Bed%20Charge%20and%20Service%20Data%20–%20Details.pbix) – In-progress bed charge and service days report  
- `README.md` – Project overview and instructions (this file)

## How to Open the Dashboard

1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/).
2. Open any `.pbix` file in Power BI Desktop.
3. Use the slicers in the report to filter by service area, posting date, financial class, or aging bucket.

## Project Summary

This project supports the University of Iowa Health Care (UIHC) Data Analytics Team in transitioning reports from Tableau to Power BI for more centralized, governable reporting. Our goal was to replicate five operational reports using Power BI connected to UIHC's semantic model. These reports enable easier filtering, visualization, and user interaction, improving access to key metrics for revenue and collections oversight.

Final reports created:

1. MMC HB Method 2 Posted Charges  
2. MMC HB Aged Trial Balance – Details  
3. MMC HB Custom Payments and Adjustments – Details  
4. MMC HB Aged Trial Balance – Summary  
5. MMC HB Revenue – MTD and YTD

In-progress reports:

1. MMC HB HAR Admissions and Discharges  
2. MMC 340B Medicaid Patients  
3. MMC HB Patient Days by Bed Charge and Service Area  

## How the Data Was Processed

We used a secure, hospital-provided semantic model within Power BI that included over 100 interconnected tables containing financial and operational variables. We began by cross-referencing Excel screenshots of the original Tableau reports with semantic model fields to locate appropriate columns and filters.

Once data sources were identified, we used Power BI’s model view to establish relationships between tables and DAX formulas to build calculated measures for KPIs. Because the data was pre-cleaned and structured for analysis, most of the work focused on ensuring the outputs and layout matched the original reports. Reports were then validated against screenshots to ensure completeness and accuracy.

Note: Most reports used the `HSP_ACCOUNT` and `HSP_TRANSACTIONS` tables.

## Methodology & Challenges

Our process included:

- Reviewing existing reports and aligning semantic model fields accordingly  
- Building visuals to mirror the format and layout of legacy Tableau reports  
- Creating calculated measures using DAX where needed  
- Incorporating filters and slicers to improve usability  
- Partner testing and cross-validation to ensure data logic was accurate  

Challenges included:

- Gaining access to Power BI and the semantic model due to system security  
- Navigating unfamiliar healthcare terminology  
- Interpreting a large volume of interrelated variables  
- Building measures without formal documentation  

Support from our sponsors and consistent team collaboration helped us overcome these technical hurdles.

## How to Recreate or Modify

1. Open the `.pbix` file in Power BI Desktop.  
2. If you'd like to use different data, go to **Transform Data > Edit Queries** to update the data source.  
3. Ensure any new data follows the same structure (column names and types).  
4. Click **Refresh** to update visuals.  
5. Use slicers to interact with the report.  
6. Refer to the project appendix for detailed variable mapping between Tableau and Power BI for each individual report.

## Report Design Details

### Mapping: Tableau Report → Power BI

| Tableau Column                        | Power BI Field Used                        |
|--------------------------------------|--------------------------------------------|
| Patient Account ID                   | `HSP_ACCOUNT.ACCOUNT_ID`                   |
| Transaction Type & Amounts          | `HSP_TRANSACTIONS.TRANS_TYPE`, `TRANS_AMT` |
| Service Area Filters                 | Applied



