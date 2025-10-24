# ELEVATELABS Internship Series  
## Complete Machine Learning Data Pipeline: Titanic & Bangalore Housing

---

## Overview

This repository demonstrates the full workflow of data cleaning, exploratory data analysis, and supervised machine learning on real-world datasets. Each task below is self-contained and modular, allowing for fast onboarding, robust reproducibility, and strong professional documentation.

---

## Task 1: Data Cleaning and Preprocessing (Titanic Dataset)

### Objective

- Prepare the Titanic dataset for machine learning through robust cleaning and encoding steps.

### Workflow

- **Data Import & Inspection:** Loaded CSV; explored shape, column info, and nulls.
- **Missing Data Handling:** Imputed 'Age' (median), 'Embarked' (mode); dropped 'Cabin' due to excessive nulls.
- **Categorical Encoding:** Binary encoding for 'Sex', one-hot for 'Embarked'.
- **Feature Scaling:** Standardized numeric columns ('Age', 'Fare') for ML stability.
- **Outlier Removal:** Visualized distributions; filtered rows 3 SD above or below mean.
- **Output:** Produced a clean, normalized, model-ready `titanic_cleaned.csv`; performed train/test split.

### Files

- `task_1_cleaning.ipynb` – fully commented Jupyter/Colab notebook
- `titanic_cleaned.csv` – clean output

---

## Task 2: Exploratory Data Analysis (Titanic Dataset)

### Objective

- Discover trends, distributions, and relationships using visual and statistical EDA.

### Workflow

- **Summary Statistics:** Used `.describe()` and value counts for all columns.
- **Visualizations:** Histograms and boxplots for distributions, bar plots for categories.
- **Relationship Analysis:** Pair plots & correlation matrix to understand variable interaction.
- **Insights:**
  - Survival rate higher for females, first class, and younger passengers.
  - Fare and age distributions revealed both skew and outliers.
  - Multicollinearity identified between Pclass, Fare, and Age.
- **Notebook:** All charts and comments are in `task_2_eda.ipynb`.

### Files

- `task_2_eda.ipynb` – full EDA process

---

## Task 3: Advanced Regression Modeling (Bangalore House Prices)

### Objective

- Predict house prices in Bangalore with a pipeline that demonstrates senior-level applied ML, using both historic and 2025 datasets.

### Workflow

- **Dual Data Import:** Historic (main) and 2025 (latest) datasets from public sources/Google Drive.
- **Cleaning & Feature Engineering:** Imputed key columns, converted BHK, engineered price/sqft, and performed one-hot encoding of top locations.
- **Train/Test Split:** Built robust cross-validation environment; selected optimal features.
- **Modeling:** Trained and interpreted a linear regression model.
- **Evaluation:**
  - On historic data: R² ~0.38, MAE ~51.
  - On 2025 data: Model showed negative R², indicating distribution drift and the challenge of model generalization.
- **Visualization:** Scatter plots (actual vs predicted), residual distribution, feature importance reporting.
- **Conclusions:**
  - Model performance highlights both predictive strengths and pitfalls of using past data for future prices.
  - Demonstrates how data drift affects real-world deployment and the necessity for retraining.

### Files

- `bangalorepropertydataset.ipynb` – entire regression pipeline
- `Bengaluru_House_Data.csv` & `house_prices_bangalore.csv` – raw data

---

## How to Use

1. Clone this repo and download all `.ipynb` and data files.
2. Open any task notebook in Colab or Jupyter.
3. Update file paths if needed, then run all cells in order.
4. Review markdown outputs for insights and ready-to-use results.


---

### **Task 4: Hospital Readmission Prediction (Binary Classification)**

- **Objective:** Predict if a hospital patient will be readmitted within 30 days using logistic regression.
- **Dataset:** 5,000 training + 2,000 test samples; 8 features (age, diagnosis, procedures, etc.)
- **Class Imbalance:** 81.2% not readmitted, 18.8% readmitted (handled with class balancing)
- **Key Results:**
  - Optimal Threshold: 0.10 (for healthcare: maximize recall)
  - Recall at 0.10: 100% (catches all readmitted patients)
  - Test predictions: Generated for 2,000 unseen samples
  - Feature insights: Kidney disease & diabetes increase risk; skilled nursing discharge decreases it
- **Skills Demonstrated:** Binary classification, threshold tuning, precision-recall trade-offs, class imbalance handling, healthcare ML
- **Notebook:** `task_4_classification.ipynb`

---

---

## Contact

For questions, implementation details, or interview references,  
contact Carlton Kenny (Garden City University) or open a GitHub Issue.

---
