# Integrating Classification, Survival, and Causal Inference Models for Breast Cancer Prognosis

## Data
This project is based on publicly available data from the Rotterdam Breast Cancer Study, an observational cohort comprising 2982 patients diagnosed with primary breast cancer. The cohort includes patients treated across multiple hospitals, with extended follow-up allowing for the analysis of both short- and long-term clinical outcomes.

## Goal
Overall aim:
* Evaluate prognosis and treatment effects in breast cancer using observational cohort data.

Specific objectives:
1) Identify key predictors of recurrence and mortality using classification models.
2) Assess time-to-event dynamics through survival analysis.
3) Estimate the causal effect of adjuvant hormonal therapy while accounting for confounding.

## Tech stack
* Python 
* Pandas
* NumPy
* Matplotlib
* Seaborn
* statsmodels
* lifelines
* Scikit-learn
* Scikit-survival

## Conclusions
Data preprocessing included log-transformation of lymph nodes, encoding of categorical variables, standardization of continuous predictors, and creation of nonlinear (age²) and interaction terms.

Built and compared:
* Regularized Logistic Regression for recurrence (ROC–AUC = 0.744) and mortality prediction (ROC–AUC = 0.82).
* Cox Proportional Hazards models for recurrence-free (C-index = 0.74) and overall survival (C-index = 0.72).
* Causal outcome regression to estimate the average treatment effect of hormonal therapy (risk difference ≈ −0.15 (CI: from -0.20 to -0.09) for recurrence, −0.10 for mortality (CI: from -0.15 to -0.05)).

Hyperparameters were tuned via cross-validation, and model assumptions (including proportional hazards and overlap) were assessed. The project demonstrates the integration of predictive modeling, survival analysis, and causal inference within a unified healthcare data pipeline.
