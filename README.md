# powerbi-final-project
Interactive Power BI report for class project — visualizing procedure-level revenue trends over time with filters and calculated measures.
## 📁 Files Included
- [AA_Painovich.pbix](./AA_Painovich.pbix) – Final report for Sophia  
- [Draft for Validation.pbix](./Draft%20for%20Validation.pbix) – Team validation version. Final report for Riley
- [Final-MMC HB Method 2 Posted Charges.pbix](./Final-MMC%20HB%20Method%202%20Posted%20Charges.pbix) – Posted charges report  
- [MMC YTD and MTD Rev.pbix](./MMC%20YTD%20and%20MTD%20Rev.pbix) – Revenue trends (MTD/YTD)  
- [Tyler's Report.pbix](./Tyler%27s%20Report.pbix) – Final report for Tyler  
- `README.md` – Project overview and instructions (this file)

## How to Open the Dashboard
1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/).
2. Open Power BI Desktop and connect to the UIHC-provided semantic model.
3. Navigate to the `HSP_ACCOUNT` and `HSP_TRANSACTIONS` tables within the model to locate the relevant variables used in your report.
4. Use the slicers in the report to filter by service area, posting date, financial class, or aging bucket.
   
## Project Summary
This project supports the University of Iowa Health Care (UIHC) Data Analytics Team in transitioning reports from Tableau to Power BI for more centralized, governable reporting. Our goal was to replicate five operational reports using Power BI connected to UIHC's semantic model. These reports enable easier filtering, visualization, and user interaction, improving access to key metrics for revenue and collections oversight.

Final reports created:
1. MMC HB Method 2 Posted Charges  
2. MMC HB Aged Trial Balance – Details  
3. MMC HB Custom Payments and Adjustments – Details  
4. MMC HB Aged Trial Balance – Summary  
5. MMC HB Revenue – MTD and YTD  

## ⚙️ How the Data Was Processed
We used a secure, hospital-provided semantic model within Power BI that included over 100 interconnected tables containing financial and operational variables. We began by cross-referencing Excel screenshots of the original Tableau reports with semantic model fields to locate appropriate columns and filters.

Once data sources were identified, we used Power BI’s model view to establish relationships between tables and DAX formulas to build calculated measures for KPIs. Because the data was pre-cleaned and structured for analysis, most of the work focused on ensuring the outputs and layout matched the original reports. Reports were then validated against screenshots to ensure completeness and accuracy.

## ✅ How to Recreate or Modify
1. Open `PowerBI_Final.pbix` in Power BI Desktop.
2. If you'd like to use different data, go to **Transform Data > Edit Queries** to update the data source.
3. Ensure any new data follows the same structure (column names and types).
4. Click **Refresh** to update visuals.
5. Use slicers to interact with the report.

## Report Design Details

### 🔄 Mapping:Tableau Report → Power BI
We performed a detailed comparison between each original Tableau report and the semantic model fields available in Power BI. This involved:
- Cross-referencing column names from UIHC screenshots and Excel files.
- Matching calculated fields and KPIs using DAX expressions.
- Ensuring filter logic and layout mirrored the original reports to support user familiarity and continuity.

Key mappings included for each report:
- **Patient Account ID** → `HSP_ACCOUNT.ACCOUNT_ID`
- **Transaction Type & Amounts** → `HSP_TRANSACTIONS.TRANS_TYPE`, `TRANS_AMT`
- **Service Area Filters** → Applied using slicers tied to the `SERVICE_AREA` field

---

### 🛠️ Power BI Tools and Functions Used
We leveraged a variety of Power BI functions and visuals to recreate the original reports:

- **Matrix Table**: Used for cross-tab views (e.g., aging buckets vs. financial class)
- **Card Visuals**: Highlighted KPIs like total account balance or volume of overdue accounts
- **Slicers**: Enabled filtering by date, service area, and financial class
- **DAX Measures**:
  - `Total Balance = SUM(HSP_TRANSACTIONS.TRANS_AMT)`
  - `Overdue Accounts = CALCULATE(COUNTROWS(...), FILTER(...))`
- **Bookmarks & View Options**: To improve navigation and simulate interactive drilldowns

These tools were selected to best replicate the logic and usability of the original Tableau dashboards while taking advantage of Power BI’s native interactivity.


## 💡 Recommendations
- Schedule regular user reviews to ensure ongoing report effectiveness.
- Provide training for filter use and interpretation of KPIs.
- Consider future enhancements to incorporate additional metrics or automation logic.

---

*Created as part of the BAIS 3500 course at the University of Iowa.*
