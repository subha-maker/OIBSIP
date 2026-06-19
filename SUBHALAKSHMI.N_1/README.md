# 🛒 Retail Sales Analysis & Power BI Dashboard

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Power Bi](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)

## 📋 Project Overview
This repository hosts an end-to-end data analytics project featuring an extensive **Exploratory Data Analysis (EDA)** using Python and a highly interactive **Power BI Dashboard**. The goal is to transform raw retail transaction logs into actionable business intelligence by evaluating sales trends, understanding customer demographics, and measuring product category performance.

## 🎯 Project Objectives
* **Data Engineering & Hygiene:** Clean, preprocess, and type-cast raw transactional data.
* **Descriptive Analytics:** Extract underlying statistical properties and variations within the dataset.
* **Time-Series Analysis:** Map out monthly and seasonal sales fluctuations.
* **Customer Demographics:** Segment consumer behavior based on age groups and gender profiles.
* **Interactive Visualization:** Build an executive-facing dashboard in Power BI for data-driven strategy.

---

## 📊 Dataset Schema
The underlying data consists of transaction-level retail records with the following structural layout:

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| `Transaction ID` | Integer | Unique identifier for each sale |
| `Date` | Date | Timestamp of the transaction |
| `Customer ID` | String | Unique identifier for individual shoppers |
| `Gender` | Categorical | Customer demographic classification (Male/Female) |
| `Age` | Integer | Age of the customer |
| `Product Category` | Categorical | Department group of the item purchased |
| `Quantity` | Integer | Units purchased per transaction |
| `Price per Unit` | Decimal | Unit price of the product |
| `Total Amount` | Decimal | Total revenue generated ($Quantity \times \text{Price per Unit}$) |

---

## 🛠️ Methodology & Analytical Workflow

### 1. Data Loading & Wrangling
* Handled missing values, outliers, and structural anomalies via Python.
* Standardized features and handled date parsing to ensure chronological analytical precision.

### 2. Exploratory Data Analysis (EDA)
* Calculated primary statistical measures (Mean, Median, Mode, Standard Deviation) to benchmark product performance and consumer basket variations.

### 3. Chronological Time-Series Evaluation
* Aggregated revenue metrics across custom time horizons to detect seasonal demand drops and macro-level cyclical spikes.

### 4. Consumer Segmentation & Inventory Insights
* Grouped customers by demographic buckets to observe purchase distributions.
* Evaluated product velocity across distinct categories to classify high-volume vs. high-margin items.

---

## 🖥️ Power BI Dashboard Architecture
The interactive `.pbix` canvas provides cross-filtering and granular slicing capabilities across several visual modules:

* **Executive KPI Tiles:** Direct, high-visibility tracking for `Total Sales Gross`, `Average Transaction Value`, and `Total Items Sold`.
* **Temporal Patterns (Line Chart):** Tracks revenue trajectories over time to flag cyclical peaks.
* **Product Standings (Horizontal Bar Chart):** Comparative performance breakdown across distinct merchandise lines.
* **Demographic Spreads:**
  * Gender distribution rendered via a **Donut Chart**.
  * Age group performance evaluated via a **Clustered Column Chart**.
* **VIP Customer Ledger (Data Matrix):** Highlights top-tier, high-revenue contributing profiles.
* **Global Filters:** Sliceable by *Date Range, Product Category,* and *Gender*.

---

## 💡 Strategic Insights
* **Revenue Fluidity:** Retail revenue exhibits noticeable month-over-month volatility, pointing heavily toward specific seasonal peaks.
* **Basket Metrics:** The majority of consumers buy between `1 to 4` items per transaction, suggesting an opportunity for product bundle strategies.
* **Value Archetype:** Middle-aged buyers act as the primary revenue engine for this retail dataset.
* **Pareto Concentration:** A small cohort of high-value consumers accounts for a disproportionate share of the net gross revenue.

## 🚀 Actionable Recommendations
1. **Targeted VIP Marketing:** Create targeted retention strategies and exclusive loyalty programs for the highest-spending tier of customers.
2. **Dynamic Inventory Forecasting:** Align supply chain stock thresholds with the cyclical demands of top-selling categories to prevent stockouts.
3. **Seasonal Pricing Strategies:** Launch targeted promotions and dynamic pricing discounts aligned with historical seasonal surges.
4. **Demographic Product Alignment:** Adjust advertising and product bundle designs to match the preferences of the core middle-aged buyer demographic.

---

## 🧰 Tech Stack
* **Languages:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
* **BI Software:** Power BI Desktop

## 📂 Repository File Structure
```text
├── data/
│   └── retail_sales_dataset.csv     # Raw dataset
├── notebooks/
│   └── sales_analysis_eda.ipynb     # Python EDA and data cleaning script
├── dashboard/
│   └── retail_analytics_v1.pbix     # Compiled Power BI dashboard
└── README.md                        # Project documentation
