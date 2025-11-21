🍄 MushroomMan Sales Analytics — Power BI | SQL | DAX | Forecasting

A full end-to-end Business Intelligence project built for a fictional organic mushroom supplier MushroomMan.
This solution uses SQL Server, Power BI, DAX, Forecasting Models, and advanced analytics to uncover trends, identify seasonal spikes, optimize inventory, and support executive decision-making.

🚀 Project Overview

This BI solution analyzes:

✔ Total Revenue & Profit Performance

✔ YOY Growth % & Sales Trends

✔ Seasonal Spike Analysis (Nov–Dec 2024 & 2025)

✔ Forecasting for the next quarter

✔ Channel & Regional Contribution

✔ Customer Segmentation

✔ Inventory Risk & Recommendation System

✔ Demand drops & stock-level actions

The report is optimized for CEO-level storytelling, performance monitoring, and inventory planning.

🧱 Tech Stack
Layer	Technology
Database	SQL Server
ETL	SQL + Power Query
Modelling	Star Schema (Fact + Dimensions)
Analytics	DAX Measures
Visualization	Power BI Desktop
Forecasting	Power BI Analytics (Exponential Smoothing)
Source Control	GitHub
📊 Key Features
⭐ 1. Executive Dashboard

Total Sales, Profit, YOY Growth

Sales LY, Sales YTD

Orders Count

Spike Contribution %

Inventory Risk Indicator (DAX-driven)

⭐ 2. Seasonal Spike Analysis

Compare 2024 vs 2025 November–December

Identify sudden demand surges

Visual spike detection

Insights for next-year seasonal stocking

⭐ 3. Predictive Forecasting

Forecast next 3 months using:

Exponential smoothing

95% confidence interval

Trend detection (decline, rise, stabilization)

⭐ 4. Inventory Recommendation Engine

A custom DAX-based rule engine:

🔴 High Risk – Increase Stock  
🟡 Medium Risk – Monitor  
🟢 Low Risk – Reduce Stock  


Driven by Quantity Change %, Profitability, and Spike behavior.

⭐ 5. Channel & Region Insights

Revenue by Region

Channel mix (Direct Market, Distributor, Online)

Profit by Quarter (2024 vs 2025)

📂 Repository Structure
MushroomMan-Sales-Analytics-PowerBI
│── PowerBI_Report/
│      └── MushroomMan_Report.pbix
│
│── SQL_Scripts/
│      ├── 01_Create_Dim_Tables.sql
│      ├── 02_Create_Fact_Sales.sql
│      ├── 03_Insert_BaseData.sql
│      ├── 04_Insert_Spike_2024.sql
│      ├── 05_Insert_Spike_2025.sql
│
│── Documentation/
│      ├── README.md
│      ├── Project_Overview.md
│      ├── Data_Model_Design.md
│      ├── DAX_Measures_Library.md
│      ├── Forecasting_Approach.md
│      ├── Inventory_Risk_Logic.md
│
│── Images/
│      ├── Dashboard_Main.png
│      ├── Forecast.png
│      ├── Inventory_KPI.png
│
└── .gitignore

🧩 Data Model

The solution follows a Star Schema:

Fact_Sales

Dim_Date

Dim_Product

Dim_Customer

Dim_Region

Dim_Cost

Benefits:

Fast DAX calculations

Clean filtering

Perfect for forecasting & seasonal analysis

🧮 Core DAX Measures
Total Sales
Total Sales = SUM(Fact_Sales[TotalSales])

Sales LY
Sales LY = CALCULATE([Total Sales], SAMEPERIODLASTYEAR(Dim_Date[Date]))

YOY Growth %
YOY Growth % =
DIVIDE([Total Sales] - [Sales LY], [Sales LY])

Spike Contribution %
Spike Contribution % =
DIVIDE([Spike Revenue], [Total Sales])

Inventory Risk
Inventory Risk =
SWITCH(
   TRUE(),
   [Quantity Change %] < -0.05, "🔴 High Risk | Increase Stock",
   [Quantity Change %] > 0.05, "🟢 Low Risk | Reduce Stock",
   "🟡 Medium Risk | Monitor"
)

🔮 Forecasting Methodology

Using Power BI Analytics pane:

Forecast Length: 3 Months

Confidence Interval: 95%

Units: Daily/Monthly depending on granularity

Outcome:

Reveals post-spike demand normalization

Predicts Q1–Q2 trends

Helps adjust inventory and avoid overstocking

🖼 Screenshots

(Upload your images in /Images and link them below)

![Executive Dashboard](Images/Dashboard_Main.png)

![Forecast](Images/Forecast.png)

![Inventory KPI](Images/Inventory_KPI.png)

▶️ How to Use the Project

Clone the repo

Run SQL scripts (1–5)

Open MushroomMan_Report.pbix

Update SQL connection

Refresh the model

Explore dashboards & forecasting visuals

🙋 Author

Kishore Suresh
Data Analyst | BI Developer
📧 skishorekichu10@gmail.com

🔗 LinkedIn: Add your link here
🛠 Power BI | SQL | DAX | Data Modelling | Forecasting | BI Storytelling

⭐ If you like this project, please star the repository! ⭐
