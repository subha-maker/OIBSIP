# 📊 Advanced Data Cleaning & Interactive Exploratory Data Analysis (EDA)

[![Python Version](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/)
[![Data Engineering](https://img.shields.io/badge/data%20engineering-pandas%20%7C%20numpy-orange.svg)](https://pandas.pydata.org/)
[![Interactive Visualization](https://img.shields.io/badge/visualization-plotly-teal.svg)](https://plotly.com/)

An end-to-end data engineering and analytics project executing a defensive, multi-stage data-cleansing pipeline on the raw New York City Airbnb ecosystem dataset (48,895 observations). This workflow resolves critical schema irregularities, treats operational anomalies, ensures absolute data integrity, and extracts high-fidelity spatial-economic insights using browser-native interactive visualizations.

---

## 📌 Project Overview & Objectives
Raw, unstructured operational transaction ledgers invariably contain data gaps, improper formatting, and systematic errors that severely bias downstream predictive modeling and descriptive statistics. This project establishes an automated, production-grade Extract-Transform-Load (ETL) pipeline to transform messy data into an audited, business-ready repository.

The primary engineering and analytical objectives are to:
* **Enforce Strict Data Governance:** Implement defensive profiling validations to standardize column storage schemas and check data boundaries.
* **Resolve Missing Structural Fields:** Apply context-driven conditional imputations to preserve maximum matrix row count instead of using arbitrary row truncation.
* **Sanitize Systematic Anomalies:** Isolate structural data entries (such as economically impossible $0 listing prices) and correct them using granular, localized parameters.
* **Uncover Real Estate Market Intelligence:** Extract spatial inventory distributions and pricing elasticities across borough segments to drive actionable asset optimization.

---

## 📊 Dataset Description
The source dataset consists of **48,895 observations and 16 tracking attributes** capturing the 2019 NYC hospitality landscape. Key features include:
* **Asset Demographics & Identity:** Unique index numbers (`id`), naming descriptions (`name`), host profiles (`host_id`, `host_name`), and categorical matrices tracking regional groups (`neighbourhood_group`) and localized sectors (`neighbourhood`).
* **Geospatial & Spatial Metrics:** Exact physical coordinates (`latitude`, `longitude`) alongside structural accommodation classifications (`room_type`).
* **Financial & Reservation Parameters:** Operational market prices per night (`price`), booking thresholds (`minimum_nights`), customer interaction tracking (`number_of_reviews`, `last_review`, `reviews_per_month`), host market share volume (`calculated_host_listings_count`), and yearly booking windows (`availability_365`).

---

## 🛠️ Tech Stack & Methodology

1. **Schema Profiling & Structural Audit:** Validating data types, analyzing memory configurations, and evaluating null data footprints.
2. **Operational Deduplication:** Evaluating multi-feature row-level overlaps to catch and remove redundant observations, protecting calculations from artificially skewed standard deviations.
3. **Contextual Imputation:** Cross-referencing dependent features to assign logical fallbacks to blank descriptive entries (`NaN` objects) without row loss.
4. **Parameter Standardization:** Re-parsing string text date inputs into uniform datetime objects to make chronological time-series analysis seamless.
5. **Outlier Mitigation:** Calculating localized median values across custom grouped metrics to repair processing errors and normalize skewed ranges.

---

## 📈 Key Interactive Visualizations
The analysis produces four core publication-quality, browser-native Plotly graphs featuring fully responsive hover states and dynamic multi-variable tooltips:

### 1. Market Inventory Mix (Interactive Donut Chart)
* **Insight:** Breaks down proportional available property selections across New York City to map out current market supply shares. Hovering over sectors instantly displays absolute asset counts and percentage distributions.

### 2. Regional Valuation Map (Interactive Scaled Bar Chart)
* **Insight:** Compares mean financial pricing benchmarks across the five core borough centers, sorting the data to immediately isolate high-premium real estate zones.

### 3. Operational Metric Feature Correlations (Interactive Matrix Heatmap)
* **Insight:** Computes a full Pearson correlation matrix across numerical dimensions to isolate connections between pricing, booking rules, and user interaction rates.

### 4. Consumer Demand Elasticity Curve (Interactive Scatter Plot)
* **Insight:** Plots cost metrics against total historical review volume (sampled at 5,000 points for browser performance) to view changes in consumer demand across pricing tiers.

---

## 🎯 Cell-by-Cell Notebook Implementation

### **Cell 1: Initialization & Baseline Profiling**
```python
import pandas as pd
import numpy as np
import plotly.express as px
import plotly.graph_objects as go

# Ingest raw operational dataset
df = pd.read_csv('AB_NYC_2019.csv')

# Execute layout profiles and initial dimension summaries
print("=== Framework Structural Audit ===")
df.info()
print(f"\nDimensions Found: Rows: {df.shape[0]} | Columns: {df.shape[1]}")
