# insurance-risk-analytics

# Insurance Risk Analytics & Predictive Modeling

## 1. Project Overview
This project focuses on analyzing insurance risk data to identify key risk drivers, understand customer and vehicle profiles, and prepare data for predictive modeling.

The work is structured into multiple tasks covering data exploration, cleaning, feature engineering, and reproducibility using DVC.

---

## 2. Business Objective
The main objective is to:
- Identify low and high-risk insurance segments
- Understand factors influencing claims and premiums
- Derive insights to support underwriting decisions
- Prepare data for future predictive modeling

---

## 3. Dataset Overview
The dataset contains insurance policy and claims information including:
- Policy details (PolicyID, CoverType, Product)
- Customer demographics (Gender, MaritalStatus, Province)
- Vehicle information (make, model, year, type)
- Financial metrics (TotalPremium, TotalClaims)

---

## 4. Task 1: Exploratory Data Analysis (EDA)

Key activities:
- Data loading and inspection
- Missing value analysis
- Duplicate checks
- Summary statistics of numerical features
- Understanding distributions of premiums and claims

Key insights:
- Significant missing values in vehicle-related attributes
- Most policies have zero claims
- Strong skewness in premium and claims distribution

---

## 5. Task 2: Advanced EDA / Feature Analysis

Key activities:
- Deeper analysis of risk indicators
- Examination of Loss Ratio distribution
- Comparison between TotalPremium and TotalClaims
- Feature-level statistical summaries

Key insights:
- LossRatio contains extreme values and infinity cases
- Claims are highly imbalanced (majority are zero)
- Premium distribution is heavily right-skewed

---
## Task 3: Hypothesis Testing
Implemented:
- ANOVA tests
- Independent t-tests
- Statistical significance evaluation
- Final hypothesis summary table

Key Findings:
- Province-level risk differences were statistically significant
- PostalCode differences were statistically significant
- Gender-based claim differences were not statistically significant

## 6. DVC Setup

Data Version Control (DVC) was initialized to ensure reproducibility of datasets and pipelines.

Steps used:
- Initialized DVC in project
- Tracked dataset using `dvc add`
- Maintained `.dvc` metadata files in Git
- Ensured large data files are not committed directly to Git

---

## 7. How to Run the Project

```bash
# activate environment
source venv/bin/activate

# install dependencies
pip install -r requirements.txt

# run notebooks
jupyter notebook
