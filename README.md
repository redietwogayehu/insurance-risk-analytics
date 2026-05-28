# Insurance Risk Analytics & Predictive Modeling

## Project Overview

This project focuses on end-to-end insurance risk analytics using historical insurance policy and claims data. The objective is to identify risk drivers, evaluate customer and vehicle risk behavior, perform statistical hypothesis testing, and develop predictive models that support data-driven underwriting and premium optimization decisions.

The project follows a structured machine learning workflow including:

* Exploratory Data Analysis (EDA)
* Data Cleaning & Feature Engineering
* Statistical Hypothesis Testing
* Predictive Modeling
* Risk-Based Pricing Insights
* Data Version Control (DVC)
* Reproducible Git Workflow

---

# Business Objective

ACIS Insurance is transitioning from intuition-based pricing strategies toward evidence-driven risk analytics during an aggressive growth phase.

The primary business objectives are:

* Identify low-risk and high-risk insurance segments
* Understand factors influencing claims and profitability
* Improve underwriting and pricing strategies
* Support risk-based premium optimization
* Build predictive models for claims and insurance risk

Key business metrics analyzed:

* **Loss Ratio**
* **Margin**
* **Claim Frequency**
* **Claim Severity**

---

# Dataset Overview

The dataset contains approximately 1 million insurance policy records collected over an 18-month period.

### Included Features

* Policy information
* Customer demographic data
* Geographic information
* Vehicle characteristics
* Premium and claims data
* Coverage and underwriting details

### Example Variables

* `PolicyID`
* `Province`
* `PostalCode`
* `VehicleType`
* `make`
* `Model`
* `RegistrationYear`
* `SumInsured`
* `TotalPremium`
* `TotalClaims`

---

# Project Structure

```bash
insurance-risk-analytics/
│
├── data/
├── notebooks/
├── figures/
├── .dvc/
├── README.md
├── requirements.txt
└── dvc.yaml
```

---

# Task 1 — Exploratory Data Analysis (EDA)

## Activities Completed

* Data loading and inspection
* Missing value analysis
* Duplicate validation
* Data type review
* Descriptive statistics
* Univariate analysis
* Bivariate analysis
* Geographic risk analysis
* Correlation analysis

## Key Insights

* Significant missing values existed in optional underwriting features
* Premium and claims distributions were heavily right-skewed
* Most policies generated zero claims
* Extreme claim outliers were identified
* Province-level differences in Loss Ratio indicated geographic risk variation
* Certain vehicle categories showed higher claim behavior

## Visualizations Created

* Missing value analysis
* Histograms
* Boxplots
* Correlation heatmaps
* Scatter plots
* Province-level comparisons
* Loss ratio distributions

---

# Task 2 — Advanced EDA & Feature Engineering

## Activities Completed

* Loss Ratio analysis
* Margin calculation
* Feature-level risk analysis
* Premium vs claims comparison
* Vehicle risk profiling
* Customer segment analysis

## Engineered Features

### Loss Ratio

```python
LossRatio = TotalClaims / TotalPremium
```

### Margin

```python
Margin = TotalPremium - TotalClaims
```

## Key Findings

* LossRatio contained significant outliers and infinite values
* Claims data was highly imbalanced
* Vehicle characteristics influenced claim behavior
* Premium values varied significantly across geographic regions

---

# Task 3 — Statistical Hypothesis Testing

## Implemented Statistical Tests

* ANOVA
* Independent t-tests
* Statistical significance testing

## Hypotheses Evaluated

1. Province Risk Difference
2. Gender Claim Difference
3. Postal Code Risk Difference
4. Vehicle Margin Difference

## Key Findings

| Hypothesis                  | Test Used | Result                    |
| --------------------------- | --------- | ------------------------- |
| Province Risk Difference    | ANOVA     | Statistically Significant |
| Gender Claim Difference     | t-test    | Not Significant           |
| Postal Code Risk Difference | ANOVA     | Statistically Significant |
| Vehicle Margin Difference   | ANOVA     | Not Significant           |

## Example Statistical Result

| Metric                    | Value    |
| ------------------------- | -------- |
| Province Risk p-value     | 0.000004 |
| Gender Difference p-value | 0.836857 |
| Postal Code p-value       | 0.005937 |

These results indicate that geographic segmentation has a stronger impact on insurance risk than gender-based segmentation.

---

# Task 4 — Predictive Modeling & Risk-Based Pricing

## Modeling Objectives

* Predict insurance claim severity
* Identify major risk-driving features
* Support risk-based pricing strategies

## Models Implemented

* Linear Regression
* Random Forest Regressor
* XGBoost Regressor

## Evaluation Metrics

* RMSE
* MAE
* R² Score

## Feature Importance Analysis

Feature importance analysis identified the most influential variables affecting insurance claims, including:

* SumInsured
* Province
* VehicleType
* RegistrationYear
* cubiccapacity

These features provide valuable insight for underwriting optimization and premium adjustment strategies.

## Explainability

Model interpretability techniques such as feature importance analysis were used to improve transparency of risk predictions and business decision-making.

---

# Data Version Control (DVC)

DVC was integrated to ensure reproducibility and proper dataset version management.

## DVC Activities

* Initialized DVC
* Tracked datasets using `.dvc` files
* Configured `.gitignore`
* Maintained reproducible data workflows
* Tracked cleaned datasets separately from raw datasets

## Benefits

* Reproducible experiments
* Dataset version tracking
* Improved collaboration
* Cleaner Git repository management

---

# Git Workflow

A structured Git branching workflow was used throughout development.

## Branches Used

* `main`
* `task-1`
* `task-2`
* `task-3`
* `task-4`

## Activities Managed Through Git

* EDA development
* DVC integration
* Statistical testing
* Model experimentation
* Final reporting

---

# How to Run the Project

## 1. Clone Repository

```bash
git clone <repository-url>
cd insurance-risk-analytics
```

## 2. Create Virtual Environment

```bash
python -m venv .venv
source .venv/bin/activate
```

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## 4. Pull DVC Data

```bash
dvc pull
```

## 5. Launch Jupyter Notebook

```bash
jupyter notebook
```

---

# Key Business Recommendations

Based on the analysis:

* Geographic-based pricing should be prioritized due to statistically significant provincial risk differences
* High-risk vehicle categories may require stricter underwriting controls
* Low-risk customer segments can be targeted for growth and retention campaigns
* Dynamic pricing models should incorporate vehicle and geographic variables

---

# Limitations

* Some features contained significant missing values
* The dataset covered only approximately 18 months
* Extreme outliers may affect model stability
* Certain customer behaviors may not be fully represented

---

# Future Work

* Deploy predictive models into production
* Implement SHAP/LIME explainability analysis
* Develop dynamic premium pricing systems
* Expand dataset coverage across additional periods
* Explore deep learning approaches for risk prediction

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* DVC
* Git & GitHub

---
