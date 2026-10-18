# CRM Sales Opportunities Dashboard (Excel: Power Query + Power Pivot)

Excel dashboard on a CRM sales pipeline dataset (8,800 opportunities), built with Power Query for cleaning, a Power Pivot data model with DAX measures, pivot tables, charts, and slicers.

## Dashboard

![Dashboard top](1_dashboard_top.png)
![Dashboard charts](2_dashboard_charts.png)

## What I did
- Power Query: loaded 4 CSV files (Sales_Pipeline, Accounts, Products, Sales_Teams), promoted headers, set data types, replaced blank accounts with "Not Available", and removed empty columns
- Power Pivot: built a 4-table data model with one-to-many relationships (Sales_Pipeline to Accounts, Products, and Sales_Teams)
- DAX measures: Total Opportunities, Won Opportunity, Lost Opportunity, Win Rate, Lost Rate, Won Value, and Total Pipeline Value
- Dashboard: pivot tables, 5 charts, and 4 slicers (Sales Agent, Regional Office, Product, Deal Stage)
- Tested refresh: after adding a record to the source data, Refresh All updated the dashboard

## Key findings
- 8,800 opportunities: 4,238 Won (48.16% of all opportunities), 2,473 Lost, 1,589 Engaging, and 500 Prospecting
- Won deal value is about 10.01M. GTXPro is the top product (3.51M) and West is the top region (3.57M)
- Top sales agent is Darcel Schlecht with about 1.15M in won value
- About 1,425 opportunities have no account recorded and are labelled "Not Available"

## Power Query steps
![Sales_Pipeline query](5_power_query_sales_pipeline.png)
![Accounts query](6_power_query_accounts.png)
![Products query](7_power_query_products.png)
![Sales_Teams query](8_power_query_sales_teams.png)

## Data model and measures
![Data model](3_data_model.png)
![Measures](4_power_pivot_measures.png)

## MIS analysis (pivot tables)
![MIS analysis 1](9_mis_analysis_1.png)
![MIS analysis 2](10_mis_analysis_2.png)

## Notes
- Win Rate is Won opportunities divided by all opportunities (including open Engaging and Prospecting deals)
- Total Pipeline Value and Won Value are the same here, because only Won deals have a close value

## Files
- `CRM_Sales_Opportunities_Dashboard.xlsx`: Excel file with the dashboard, pivots, and data model
- `Sales_Pipeline.csv`, `Accounts.csv`, `Products.csv`, `Sales_Teams.csv`: source data

## How to refresh
The file opens with the data already loaded. To refresh it on another computer, download the CSV files, then update the file paths in Power Query (Data > Queries & Connections > right-click a query > Edit > Source) and click Refresh All.

## Tools
Excel, Power Query, Power Pivot, DAX, Pivot Tables, Slicers
