# 🏡 House Price Prediction using Linear Regression

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![ML Library](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)](https://scikit-learn.org/)
[![Interactive Visualizations](https://img.shields.io/badge/Visualizations-Plotly-brightgreen)](https://plotly.com/)

An end-to-end Machine Learning pipeline that develops, evaluates, and interprets a predictive linear regression model to estimate real estate valuation based on physical structural attributes, space scale, and property amenities. 

This repository features a clean, cell-by-cell notebook implementation driven by interactive, hover-capable analytical dashboards built using **Plotly**.

---

## 🔗 Live Links & Project Access
* **Interactive Notebook:** [![Open In Colab]([https://colab.research.google.com/assets/colab-badge.svg)](YOUR_GOOGLE_COLAB_LINK_HERE](https://github.com/subha-maker/OIBSIP/blob/main/SUBHALAKSHMI.N_5/notebook/HOUSE_PRICES.ipynb)) 
* **Dataset Source:** [Housing Dataset Archive](https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPOSITORY_NAME/blob/main/Housing.csv) *(Update with your repository path)*

---

## 📌 Project Overview & Learning Objectives
The primary objective of this project is to model the linear relationship between a continuous dependent target (`price`) and independent structural data arrays.

### Key Implementation Milestones:
* **Exploratory Data Analysis (EDA):** Verifying data completeness, distribution checking, and evaluating feature data types.
* **Feature Engineering:** Mapping raw binary text features (`yes`/`no`) into optimized binary indicators (`1`/`0`) and handling multi-class inputs via **One-Hot Encoding** (`pd.get_dummies(drop_first=True)`) to eliminate multicollinearity.
* **Model Training:** Deploying an Ordinary Least Squares (OLS) Linear Regression model via Scikit-Learn.
* **Performance Validation:** Quantifying structural error distribution and variance explanation with Mean Squared Error (MSE) and Coefficient of Determination ($R^2$).
* **Data Visualizations:** Building comprehensive residual tracking charts with dynamic tooltip hover elements.

---

## 🛠️ Tech Stack & Architecture Dependencies
* **Core Language:** Python 3.8+
* **Data Frameworks:** `pandas`, `numpy`
* **Machine Learning Engine:** `scikit-learn`
* **Visualization Layer:** `plotly`, `seaborn`, `matplotlib`

To replicate this environment locally, execute the standard pip management configuration below:
```bash
pip install pandas numpy scikit-learn plotly seaborn matplotlib
