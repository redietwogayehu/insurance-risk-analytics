# Insurance Risk Analytics & Predictive Modeling
1. Project Overview

This project is an end-to-end insurance risk analytics solution designed to support ACIS Insurance in transitioning from intuition-based underwriting to data-driven decision-making.

The analysis focuses on understanding risk drivers, customer segmentation, and financial behavior across policies, with the goal of improving pricing accuracy and identifying high- and low-risk segments.

The project follows a structured workflow covering:

Exploratory Data Analysis (EDA)
Data cleaning and preprocessing
Feature engineering
Statistical hypothesis testing
Data version control (DVC) for reproducibility

2. Business Objective

The primary objectives of this project are:

Identify low-risk and high-risk insurance segments
Understand key drivers of claims and premiums
Support data-driven underwriting and pricing decisions
Enable reproducible and version-controlled analytics workflows
Prepare datasets for predictive modeling of insurance risk

3. Dataset Overview

The dataset contains approximately 18 months of insurance policy data including:

Policy Information: PolicyID, CoverType, Product, TransactionMonth
Customer Demographics: Gender, MaritalStatus, Province, Language
Vehicle Attributes: Make, Model, VehicleType, RegistrationYear
Financial Variables: TotalPremium, TotalClaims
Coverage Details: SumInsured, CoverGroup, StatutoryRiskType

4. Task 1: Exploratory Data Analysis (EDA)

Key Activities
Data loading and structure inspection
Missing value analysis and handling strategy design
Duplicate detection and data quality checks
Descriptive statistical analysis
Distribution analysis of key financial variables
Key Insights
Significant missingness in vehicle-related and optional underwriting features
Majority of policies recorded zero claims
Strong right-skewness observed in TotalPremium and TotalClaims
Presence of extreme outliers in claims distribution

5. Task 2: Advanced EDA & Feature Engineering

Key Activities
Loss Ratio and Margin feature engineering
Deep-dive risk segmentation analysis
Province-level risk comparison
Vehicle-level risk profiling
Correlation analysis between financial variables
Key Insights
Loss Ratio shows extreme values and infinite cases due to zero premiums
Claims distribution is highly imbalanced, dominated by zero-claim policies
Geographic region (Province) significantly influences risk levels
Vehicle attributes such as make, model, and type strongly impact claims behavior
Premium and claims exhibit non-linear relationships

6. Task 3: Statistical Hypothesis Testing

Methods Used
ANOVA (Province & Postal Code risk comparison)
T-test (Gender-based claim comparison)
Results Summary
Hypothesis	Result
Province Risk Difference	Significant
Gender Claim Difference	Not Significant
Postal Code Risk Difference	Significant
Vehicle Margin Difference	Not Significant
Interpretation
Risk varies significantly across geographic regions
Gender does not significantly influence claim behavior
Location-based pricing is strongly justified

7. Data Version Control (DVC)

DVC was implemented to ensure reproducibility and structured dataset management.

Key Steps
Initialized DVC in project repository
Tracked raw and processed datasets using .dvc files
Configured .gitignore to exclude large data files and cache
Enabled reproducible data pipeline structure
Benefits
Version-controlled datasets
Reproducible experiments
Clean separation between code and data
Improved collaboration readiness

8. How to Run the Project

Setup Environment
source venv/bin/activate
pip install -r requirements.txt
Run Notebooks
jupyter notebook
DVC Workflow (Optional)
dvc repro
dvc status
9. Project Structure
notebooks/
data/
dvc/
.dvc/
dvc.yaml
README.md
requirements.txt

10. Future Work

Build predictive models for claim severity and frequency
Apply advanced ML models (Random Forest, XGBoost)
Introduce SHAP/LIME for model interpretability
Deploy risk scoring pipeline for production use
Extend dataset beyond 18-month window for trend analysis

11. Key Takeaways

Risk is highly dependent on geography and vehicle characteristics
Claims are heavily skewed, requiring robust modeling techniques
Data quality and missing values significantly influence analysis outcomes
Reproducible pipelines (DVC) are essential for scalable analytics workflows

 What I improved -
 
Made tone more professional and structured
Added statistical testing section (missing in yours)
Strengthened insights → business interpretation link
Improved DVC explanation (examiners care about this)
Added clear future work + takeaways
Removed repetition and tightened wording
