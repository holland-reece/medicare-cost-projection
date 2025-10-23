# 🧮 Cost Projection Model — 2022 Medicare Current Beneficiary Survey (Cost Supplement)

Author: [Holland Reece Brown](github.com/holland-reece)

Updated 2025-10-22 
Created 2025-07-07
  
Author: Holland Reece Brown  
🔗 [GitHub Profile](https://github.com/holland-reece) | 🌐 [Website](https://holland-reece.github.io/)  

## 📘 Project Overview

This project develops a cost projection model using data from the 2022 Medicare Current Beneficiary Survey (MCBS) Cost Supplement, published by the [Centers for Medicare & Medicaid Services (CMS)]( https://data.cms.gov/medicare-current-beneficiary-survey-mcbs/medicare-current-beneficiary-survey-cost-supplement).


The model estimates individual Medicare beneficiaries’ projected healthcare expenditures based on demographic, clinical, and cost-related variables — demonstrating __practical applications of machine learning on structured health economics data__.

## 🧩 Dataset Summary

Source: 2022 MCBS – Cost Supplement
Population: Medicare and Medicaid beneficiaries living in the community (not in assisted-living or institutional care)

### Key Dataset Features
- Demographic information (age, sex, race, income, insurance type)
- Annual healthcare expenditures and payment sources
- Out-of-pocket costs for co-payments, deductibles, and non-covered services
- Balanced Repeated Replication (BRR) weights for estimating variance, standard errors, and confidence intervals without access to protected health data

## ⚙️ Modeling Approach
### Model Type: Gradient Boosting Decision Tree (GBDT)

### Why GBDT:
- Handles multi-modal tabular data and categorical variables efficiently
- Captures complex nonlinear relationships and feature interactions
- Robust to missing or incomplete data, common in healthcare datasets
- Enables SHAP-based feature importance for transparent model interpretation

### Pipeline Highlights:
- Data cleaning and transformation (handling missing values, categorical encoding)
- Train-test split and cross-validation with BRR-weight integration
- Model training using gradient boosting (e.g., XGBoost or LightGBM)
- Performance evaluation via MAE / RMSE / R² metrics
- Feature importance and SHAP visualization