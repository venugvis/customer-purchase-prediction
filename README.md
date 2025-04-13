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
