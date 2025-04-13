# Predicting Customer Purchase Behavior | End-to-End ML Project

A complete machine learning case study using real-world customer behavioral data. Covers ETL, EDA, feature engineering, model training, hyperparameter tuning (GridSearchCV), and performance evaluation. 

---

## Phase 1: Data Cleaning (ETL)

I began by importing the raw dataset and understanding its structure. After confirming that there were no missing values, I identified and converted several numerical columns to categorical types (e.g., `Gender`, `LoyaltyProgram`, `ProductCategory`, and `PurchaseStatus`). Finally, the cleaned dataset was saved for reuse in future steps.

**Notebook:** [`01_data_cleaning.ipynb`](notebooks/01_data_cleaning.ipynb)  
**Cleaned File:** `data/processed/cleaned_customer_data.csv`

---

## Phase 2: Exploratory Data Analysis (EDA)

In this phase, I performed univariate and bivariate analysis to explore patterns and relationships in the data.

### Univariate Analysis:
- **TimeSpentOnWebsite**: Slight positive trend; peak engagement near 45 minutes.
- **AnnualIncome**: Surprisingly balanced; no transformation needed.
- **NumberOfPurchases**: Spike at 20 suggests a possible system cap.
- **DiscountsAvailed**: Fairly even distribution across all bins.
- **Age**: Bimodal pattern with peaks in younger and older ranges.

### Bivariate Analysis (vs PurchaseStatus):
- **TimeSpentOnWebsite**: Clear increase in median time for purchasers.
- **AnnualIncome**: Purchasers had notably higher income.
- **DiscountsAvailed**: Slightly more discounts used by purchasers.

**Notebook:** [`02_exploratory_data_analysis.ipynb`](notebooks/02_exploratory_data_analysis.ipynb)

---

## Phase 3: Modeling and Evaluation

After preparing the features and encoding categorical variables, I split the dataset and trained a baseline `RandomForestClassifier`.  
The baseline model achieved:

- **Accuracy**: 92%
- **F1 Score (Purchase class)**: 0.90

I then used **GridSearchCV** to optimize key hyperparameters such as `n_estimators`, `max_depth`, `min_samples_split`, and `min_samples_leaf`.  
The tuned model improved performance further:

- **Accuracy**: 93%
- **F1 Score (Purchase class)**: 0.91
- **Precision (Purchase class)**: 0.94

This confirmed that the features were meaningful and the model generalized well.  

I would consider this version production-ready for business insights or deployment.

**Notebook:** [`03_modeling_pipeline.ipynb`](notebooks/03_modeling_pipeline.ipynb)
