Interactive Power BI report for class project — visualizing procedure-level revenue trends over time with filters and calculated measures.

Files Included

Final-MMC HB Method 2 Posted Charges.pbix – Posted charges report

Final – MMC HB Custom Payments and Adjustments – Details.pbix – Custom payments and adjustments

Final - MMC HB Aged Trial Balance – Summary.pbix – Trial balance summary

Final - MMC HB Aged Trial Balance – Details.pbix – Trial balance detail

Final-MMC YTD and MTD Rev.pbix – Revenue trends (MTD/YTD)

WIP-MMC 340B Medicaid Patients.pbix – In-progress 340B report

WIP MMC HB Patient Days by Bed Charge and Service Data – Details.pbix – In-progress bed charge detail report

WIP-MMC HB HAR Admissions and Discharges.pbix – In-progress admissions and discharges report

README.md – Project overview and instructions (this file)

How to Open the Dashboard

Download and install Power BI Desktop.

Open Power BI Desktop and load the relevant .pbix file from the list above.

Use the slicers in the report to filter by service area, posting date, financial class, or aging bucket.

Project Summary

This project supports the University of Iowa Health Care (UIHC) Data Analytics Team in transitioning reports from Tableau to Power BI for more centralized, governable reporting. Our goal was to replicate five operational reports using Power BI connected to UIHC's semantic model. These reports enable easier filtering, visualization, and user interaction, improving access to key metrics for revenue and collections oversight.

Final reports created:

MMC HB Method 2 Posted Charges

MMC HB Aged Trial Balance – Details

MMC HB Custom Payments and Adjustments – Details

MMC HB Aged Trial Balance – Summary

MMC HB Revenue – MTD and YTD

How the Data Was Processed

We used a secure, hospital-provided semantic model within Power BI that included over 100 interconnected tables containing financial and operational variables. We began by cross-referencing Excel screenshots of the original Tableau reports with semantic model fields to locate appropriate columns and filters.

Once data sources were identified, we used Power BI’s model view to establish relationships between tables and DAX formulas to build calculated measures for KPIs. Because the data was pre-cleaned and structured for analysis, most of the work focused on ensuring the outputs and layout matched the original reports. Reports were then validated against screenshots to ensure completeness and accuracy.

Methodology and Challenges

Our process included:

Reviewing existing reports and aligning semantic model fields accordingly

Building visuals to mirror the format and layout of legacy Tableau reports

Creating calculated measures using DAX where needed

Incorporating filters and slicers to improve usability

Partner testing and cross-validation to ensure data logic was accurate

Challenges included:

Gaining access to Power BI and the semantic model due to system security

Navigating unfamiliar healthcare terminology

Interpreting a large volume of interrelated variables

Building measures without formal documentation

Support from our sponsors and consistent team collaboration helped us overcome these technical hurdles.

How to Recreate or Modify

Open any .pbix file in Power BI Desktop.

If you'd like to use different data, go to Transform Data > Edit Queries to update the data source.

Ensure any new data follows the same structure (column names and types).

Click Refresh to update visuals.

Use slicers to interact with the report.

Refer to the Appendix in our final report for detailed variable mapping by report.

Report Design Details

Mapping: Tableau Report → Power BI

Patient Account ID → HSP_ACCOUNT.ACCOUNT_ID

Transaction Type & Amounts → HSP_TRANSACTIONS.TRANS_TYPE, TRANS_AMT

Service Area Filters → Applied using slicers tied to the SERVICE_AREA field

Power BI Tools and Functions Used

We leveraged a variety of Power BI functions and visuals to recreate the original reports:

Matrix Table: Used for cross-tab views (e.g., aging buckets vs. financial class)

Regular Table: Used for detailed row-level transaction listings

Card Visuals: Highlighted KPIs like total account balance or volume of overdue accounts

Slicers: Enabled filtering by date, service area, and financial class

DAX Measures:

Total Balance = SUM(HSP_TRANSACTIONS.TRANS_AMT)

Overdue Accounts = CALCULATE(COUNTROWS(...), FILTER(...))

Bookmarks & View Options: To improve navigation and simulate interactive drilldowns

These tools were selected to best replicate the logic and usability of the original Tableau dashboards while taking advantage of Power BI’s native interactivity.

Recommendations

Schedule regular user reviews to ensure ongoing report effectiveness.

Provide training for filter use and interpretation of KPIs.

Consider future enhancements to incorporate additional metrics or automation logic.

Created as part of the BAIS 3500 course at the University of Iowa.



