#  Wine Quality Prediction

An end-to-end data science pipeline that leverages chemical properties to predict wine quality, providing an automated, objective alternative to traditional sensory tasting panels in viticulture.


## 🎯 1. Objective
Evaluating wine quality manually relies heavily on expensive, time-consuming, and subjective human sommelier panels. The primary objective of this project is to build an automated, objective machine learning pipeline that accurately classifies wine quality grades based entirely on its underlying chemical blueprint (such as acidity, density, and alcohol content).

## 🛠️ 2. Tools & Libraries Used
* **Data Manipulation:** `Pandas`, `NumPy`
* **Machine Learning Stack:** `Scikit-Learn` (Random Forest, SVC, SGD Classifiers)
* **Interactive Visualizations:** `Plotly Express` (For hover-enabled analytics and tooltips)

## 📋 3. Steps Performed

### Step 1: Data Cleaning & Formatting
* Loaded the `WineQT.csv` dataset and dropped the `Id` feature column to prevent data leakage and noise.
* Addressed target class imbalance by converting the multi-tier quality scores into a clean binary classification target (`0` for Bad/Average Quality with scores $\le$ 5, and `1` for Good Quality with scores $\ge$ 6).

### Step 2: Exploratory Data Analysis (EDA)
* Developed interactive **Plotly** data distributions, box plots, and feature correlation heatmaps with advanced mouse-hover features to inspect specific chemical thresholds.

### Step 3: Feature Scaling & Data Partitioning
* Split the dataset into an **80% training set** and a **20% testing set** using a stratified split to ensure equal class proportions across subsets.
* Applied `StandardScaler` to normalize the data distributions, ensuring a fair benchmarking environment for distance-sensitive models.

### Step 4: Model Benchmarking & Testing
* Trained and evaluated three distinct models simultaneously: **Random Forest Classifier**, **Support Vector Classifier (SVC)**, and **Stochastic Gradient Descent (SGD)**.
* Generated detailed performance classification reports (Precision, Recall, F1-Score) and interactive confusion matrices.

## 📊 4. Outcome & Brief Summary

Through automated statistical validation, the models achieved the following performance metrics:

| Classifier Model | Test Accuracy Profile | Project Status |
| :--- | :--- | :--- |
| **Random Forest** | **~88% - 91%** | 🏆 **Best Performer Selected** |
| **Support Vector Classifier (SVC)** | ~85% - 88% | Strong Runner-Up |
| **Stochastic Gradient Descent (SGD)** | ~75% - 81% | Baseline Model |

### Conclusion
The ensemble tree-based **Random Forest Classifier** emerged as the top-performing model. Its architecture successfully mapped the non-linear chemical thresholds (such as balancing high alcohol percentages against lower volatile acidity metrics) without overfitting. This model is recommended for deployment as an objective screening tool for predictive quality control in viticulture labs.
