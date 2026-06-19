# 🛒 Customer Segmentation Analysis using K-Means Clustering

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![ML Framework](https://img.shields.io/badge/machine%20learning-scikit--learn-orange.svg)](https://scikit-learn.org/)
[![Data Visualization](https://img.shields.io/badge/visualization-seaborn%20%7C%20matplotlib-teal.svg)](https://seaborn.pydata.org/)

An end-to-end data science project performing behavioral and demographic customer segmentation for an e-commerce platform. Using **Unsupervised Machine Learning (K-Means Clustering)** and **Dimensionality Reduction (PCA)**, this analysis groups 2,205 consumers into distinct actionable marketing personas.

---

## 📌 Project Overview & Objectives
The goal of this analysis is to replace broad mass-marketing strategies with targeted data-driven campaigns. By clustering customer purchase data, channel metrics, and one-hot encoded demographics, we extract distinct customer profiles to:
* Optimize **marketing spend** by aligning promotional offers with specific consumer interests.
* Identify high-value cohorts (**VIP customers**) to focus on luxury cross-selling.
* Discover price-sensitive groups to engage with tailored discount bundles.

---

## 📊 Dataset Description
The underlying dataset consists of **2,205 observations and 39 columns**. Key features tracked include:
* **Socio-Demographics:** Household `Income`, `Age`, `Customer_Days` (enrollment age), and engineered binary matrices for Education Levels (`education_PhD`, `education_Graduation`, etc.) and Marital Statuses (`marital_Married`, `marital_Single`, etc.).
* **Spending Habits:** Spending in the last 2 years on individual categories (`MntWines`, `MntMeatProducts`, `MntFruits`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds`) and cumulative spending (`MntTotal`).
* **Purchasing Channels:** Order distributions via `NumWebPurchases`, `NumCatalogPurchases`, `NumStorePurchases`, and coupon usage (`NumDealsPurchases`).

---

## 🛠️ Tech Stack & Methodology



1. **Exploratory Data Analysis (EDA):** Checking integrity constraints, removing constant features (like `Z_CostContact`, `Z_Revenue`).
2. **Feature Scaling:** Normalizing features with `StandardScaler` to ensure metrics with massive ranges (e.g., `Income`) do not obscure lower-range values (e.g., website visit metrics).
3. **Hyperparameter Tuning:** Running an iterative sweep to evaluate **Within-Cluster Sum of Squares (WCSS)** and mapping the **Elbow Curve** to isolate the optimal $K$.
4. **Clustering & Dim-Reduction:** Deploying `KMeans++` initialization and mapping coordinates to a 2D space using **Principal Component Analysis (PCA)**.
5. **Customer Profiling:** Evaluating cluster behavioral averages against product categories to name and design individual personas.

---

## 📈 Key Visualizations

Your notebook produces four core publication-quality plots:

### 1. The Elbow Optimization Curve
* **File:** `elbow_method.png`
* **Insight:** Identifies the statistical point of diminishing returns (inflection point), justifying the choice of cluster count.

### 2. PCA Cluster Separation Map
* **File:** `pca_clusters.png`
* **Insight:** Compresses the 12-dimensional feature space into a 2D coordinate view to visually verify that clusters are separated cleanly without problematic overlapping.

### 3. Economic Context Map (Income vs. Spending)
* **File:** `income_vs_spend.png`
* **Insight:** Combines financial revenue with digital purchasing velocity (bubble sizes) to trace wealth-to-spending thresholds.

### 4. Product Spending Breakdown (Wallet Share Allocation)
* **File:** `product_spending_breakdown.png`
* **Insight:** A cross-category grouped bar chart mapping out exactly how much each cluster drops on specific item types (Wines vs. Meats vs. Sweets).

---

## 🎯 Generated Persona Segments & Strategic Action Plan

Based on the statistical averages, the customer base separates cleanly into three targetable groups:

### 🔹 Cluster 0: Value-Driven / Budget Shoppers
* **Profile:** Lower annual household income, minimized product-specific budgets, but high interaction rate with standard promotional coupon deals (`NumDealsPurchases`).
* **Strategy:** Deploy automated price-drop notifications, low-threshold spending coupons, and frequent clearance updates.

### 🔹 Cluster 1: Balanced Mid-Tier Shoppers
* **Profile:** Average income bracket, standard consistent web/store activity, purchasing predictable amounts across general household goods.
* **Strategy:** Introduce cross-category reward bundles (e.g., buy Wine, get Sweets at half price) and platform loyalty enrollment incentives.

### 🔹 Cluster 2: Affluent Premium Shoppers
* **Profile:** Highest income segment, disproportionately high expenditure metrics (`MntTotal`), especially in high-margin goods like Wines and Meats. Prefer purchasing through catalog or direct channel options.
* **Strategy:** Provide priority early access to new specialty stock, exclusive tier memberships, and high-end personalized direct outreach.

---

## 🚀 How to Run the Analysis Locally

### 1. Clone the repository
```bash
git clone [https://github.com/YOUR_USERNAME/customer-segmentation-analysis.git](https://github.com/YOUR_USERNAME/customer-segmentation-analysis.git)
cd customer-segmentation-analysis
