# ELEVATELABS
# Data Cleaning and Preprocessing for ML - Titanic Dataset

## Objective

This repository demonstrates a practical, step-wise approach to preparing raw tabular data for machine learning, using the Titanic passenger dataset as an example. The workflow is built for reliability and clarity, following proven industry methods.

## Workflow Summary

1. **Data Import and Inspection**
   - Loaded Titanic CSV from public source.
   - Verified shape, column types, and missing value counts.

2. **Missing Value Handling**
   - Imputed 'Age' using median for stability against outliers.
   - Imputed 'Embarked' using the mode (most frequent value).
   - Dropped 'Cabin' due to excessive missing rates.

3. **Categorical Encoding**
   - Converted binary 'Sex' column to numerical format.
   - One-hot encoded 'Embarked' for model compatibility.
   - Dropped high-cardinality columns 'Name' and 'Ticket'.

4. **Feature Scaling**
   - Standardized 'Age' and 'Fare' to zero mean, unit variance for algorithmic consistency.

5. **Outlier Detection and Removal**
   - Visualized 'Age' and 'Fare' with boxplots.
   - Removed records beyond 3 standard deviations from mean.

6. **Output and Preparation**
   - Cleaned dataset exported for downstream modeling.
   - Train/test split performed for reproducibility.

## Design Choices

- **Imputation:** Median preferred for 'Age' to minimize bias from typical outlier ages.
- **Encoding:** Label encoding for clear binary features, One-hot for 3-class categorical.
- **Dropping Features:** 'Cabin', 'Name', 'Ticket' are left out for baseline tabular ML tasks—advanced features can be built as needed.
- **Scaling:** StandardScaler chosen for compatibility with most ML models.

## Reproducibility

All steps are modular and explained in the Jupyter/Colab notebook.  
Simply run notebook cells sequentially to reproduce results.

## Files

- `task_1_cleaning.ipynb` — Complete notebook with explanations and code.
- `titanic_cleaned.csv` — Output after cleaning and preprocessing.

## Getting Started

1. Clone the repository.
2. Open `task_1_cleaning.ipynb` in Colab or Jupyter.
3. Run cells and inspect outputs interactively.

## Contact

For questions about methodology or internship requirements, reach out on GitHub Issues or by email.

