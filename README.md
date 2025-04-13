# customer-purchase-prediction (Work in progress)

-  Proposed directory structure"

customer-purchase-prediction/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
├── src/
├── README.md
└── .gitignore


# Customer Purchase Prediction

This project predicts whether a customer will make a purchase based on their profile and online behavior.  
It is structured end-to-end from data ingestion to model tuning and evaluation, and is designed as a portfolio-quality case study.

---

## Phase 1: Data Cleaning (ETL)

We began by importing the raw dataset and understanding its structure. After confirming that there were no missing values, we identified and converted several numerical columns to categorical types (e.g., `Gender`, `LoyaltyProgram`, `ProductCategory`, and `PurchaseStatus`). Finally, the cleaned dataset was saved for reuse in future steps.

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

Notebook: [`02_exploratory_data_analysis.ipynb`](notebooks/02_exploratory_data_analysis.ipynb)

