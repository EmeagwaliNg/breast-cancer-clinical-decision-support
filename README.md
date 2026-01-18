# Predictive Modeling for Clinical Decision Support  
## Breast Cancer Screening Using Logistic Regression

### Overview
Early detection of breast cancer significantly improves patient survival.  
This project demonstrates an interpretable, high-performance predictive model designed to support clinical decision-making during initial breast cancer screening.

The focus is not just prediction accuracy, but **clinical reliability, transparency, and ethical modeling practices**.

---

## Business Problem
Clinicians often evaluate multiple tumor characteristics simultaneously.  
Manual interpretation of high-dimensional diagnostic data can be time-consuming and variable across practitioners.

**Goal:**  
Develop a transparent screening model that estimates malignancy risk and serves as a secondary decision-support tool for clinicians.

---

## Dataset
- **Name:** Breast Cancer Wisconsin Diagnostic Dataset
- **Source:** UCI Machine Learning Repository / scikit-learn
- **Sample Size:** 569 patients
- **Outcome:** Malignant vs Benign tumor diagnosis
- **Features:** Tumor radius, texture, perimeter, smoothness, concavity, symmetry, etc.

> This dataset is used as a **methodological demonstration** of a clinically relevant modeling pipeline.

---

## Methodology
- Exploratory Data Analysis & Descriptive Statistics
- Correlation Analysis
- Logistic Regression (statsmodels)
- Odds Ratio Interpretation
- Model Evaluation:
  - Confusion Matrix
  - Precision & Recall
  - ROC Curve and AUC

---

## Model Choice
Logistic regression was selected for its **interpretability**, a critical requirement in healthcare settings where clinicians must understand *why* a prediction is made.

Odds ratios provide direct insight into how tumor features influence malignancy risk.

---

## Key Results
- **High recall (sensitivity)** for malignant cases, minimizing missed diagnoses
- **Strong AUC (>0.95)** indicating excellent discrimination
- **Mean radius** identified as the strongest predictor of malignancy

---

## Handling Statistical Challenges
A quasi-separation warning was observed, indicating near-perfect separation by some predictors.

This was addressed by:
- Selecting clinically relevant features
- Avoiding unnecessary high-dimensional predictors
- Conducting robustness checks with penalized regression

---

## Ethics & Trust
- Dataset is fully anonymized and publicly available
- Modeling choices prioritize transparency over black-box accuracy
- Bias awareness considered, with limitations acknowledged where demographic data were unavailable

---

## Tools & Technologies
- Python
- pandas, numpy
- statsmodels
- scikit-learn
- matplotlib, seaborn

---

## Future Work
- External validation on real clinical datasets
- Cross-validation and calibration analysis
- Deployment via FastAPI for real-time screening support
- Integration with electronic health records (EHRs)

---

## Disclaimer
This model is intended for **decision support only** and does not replace professional medical diagnosis.

---

## How to Run
```bash
pip install -r requirements.txt
