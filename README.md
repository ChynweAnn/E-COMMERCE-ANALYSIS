# E-COMMERCE-ANALYSIS

## Problem Statement
The business was experiencing fluctuating net margins despite high sales volume. This project was initiated to identify cost leakages in shipping logistics and evaluate the effectiveness of current discount strategies across different customer segments
Also, examines the performance of delivered and returned orders, assessing the impact of returns on overall profitability.

## Technical Stack & Skills
1) Excel: Power Query for data cleaning, Pivot Tables for initial discovery.
2) Power BI: DAX for complex measures
3) Key Skills: ETL (Extract, Transform, Load), Data Auditing, and Trend Analysis.

## Data Dictionary
1) Order Priority: Used to analyze the cost-to-speed trade-off.
2) Shipping Cost & Mode: Key variables for logistics optimization.
3) Customer Segment: Used for targeted demographic insights.
4) Returned Orders: Used to evaluate the impact of returned orders on the profitability.

## Key Analysis Highlight
The data examination helped identify the effect of returned orders on the business's profitability.

 1) There were no duplicate values
 2) Missing Values were found and handled.
 3) The examination shows High Dependency on Tech & Office Supplies
 4) Temporal Trends (Weekly/Monthly)-There is a massive spike in profit on Fridays ($0.29M) compared to the rest of the week, and January/October seem to be peak months.

<img width="936" height="443" alt="image" src="https://github.com/user-attachments/assets/b0d86eef-3545-4d24-9667-3080b54f98f8" />




 Management Performance Disparity: Pat is significantly outperforming all other regional managers, with $0.85M in profit, while Chris has $0.00M.
 
 <img width="279" height="212" alt="image" src="https://github.com/user-attachments/assets/0911ae66-18fa-4359-9d5b-21c95137f3a5" />






 Generational Wealth Gap in Sales: Gen X is the powerhouse
 
 <img width="280" height="215" alt="image" src="https://github.com/user-attachments/assets/01620dd1-f5d0-4c43-b635-a95afcda15ed" />










## ETL PROCESS 

* Extraction: Connected to e-commerce flat files (CSV/Excel) containing 8,000+ transactions.

* Transformation (Power Query): * Cleaned inconsistent naming in Product Categories.

* Handled missing values in BirthDate to ensure accurate age generation bins.

* Calculated a custom Total Cost column by merging Shipping Cost and Unit Price.

* Modeling: Created a Star Schema with a dedicated Date Table for time-intelligence analysis (Yearly/Monthly/Weekly trends).
  
* DAX :I developed custom measures to track underlying business health beyond just "Sales."

  
* xtage_loss
xtage_loss = DIVIDE([Total_loss],[Sum Of Profit])

*Total_loss
Total_loss = CALCULATE([Sum Of Profit],Sales_Transaction[Order Status]="Returned")

