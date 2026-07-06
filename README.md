# Cruise Customer Satisfaction Prediction using XGBoost
Predicting cruise customer satisfaction using machine learning and explaining model decisions with SHAP.

---

## Overview

This project builds an end-to-end machine learning pipeline to predict customer satisfaction scores for cruise bookings using operational, booking, and customer-related features.

Instead of treating the model as a black box, SHAP (SHapley Additive exPlanations) is used to understand **why** the model makes each prediction and which factors influence customer satisfaction.

---

## Objectives

- Predict customer satisfaction scores
- Identify the factors influencing satisfaction
- Explain model predictions using SHAP
- Provide business insights for cruise operators

---

## Dataset

The dataset contains **77,040 cruise booking records** with information such as:

- Booking Lead Time
- Cruise Ship
- Cruise Company
- Route Type
- Suite Type
- Booking Source
- Guest Country
- Number of Cabins
- Crew Size
- Occupancy Rate
- Booking Revenue
- Average Guest Spending
- Travel Date
- Booking Date
- Customer Satisfaction Score (Target)

---

## Data Preprocessing

The following preprocessing steps were performed:

- Removed unnecessary identifier columns
- Converted travel and booking dates into `datetime`
- Extracted:
  - Year
  - Month
  - Day
  - Day of Week
  - Quarter
- One-hot encoded categorical variables
- Created feature matrix and target variable
- Train-Test Split (80/20)

---

## Model

**Algorithm**

- XGBoost Regressor

### Why XGBoost?

- Excellent performance on structured/tabular datasets
- Handles nonlinear relationships
- Robust against overfitting
- Provides feature importance
- Compatible with SHAP explainability

---

## Model Explainability

This project uses **SHAP (SHapley Additive exPlanations)** to interpret model predictions.

The following analyses were performed:

- Feature Importance
- SHAP Summary Plot
- SHAP Waterfall Plot

These analyses reveal how individual features influence customer satisfaction predictions.

---

## Key Insights

Some important findings include:

- Average guest spending strongly influences predicted satisfaction.
- Cruise route significantly impacts customer satisfaction.
- Crew size contributes positively to customer experience.
- Booking lead time plays an important role in prediction.
---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- SHAP
- Matplotlib
---

## Project Structure

```
Cruise-Satisfaction-Prediction/
│
├── data/
│   └── reporte_cruceros_revenue_management.csv
│
├── notebook.ipynb
├── README.md
└── figures/
    ├── feature_importance.png
    ├── shap_summary.png
    └── shap_waterfall.png
```
---
## Metrics and thier results
Mean Absolute Error: 0.10878753550698828
Mean Squared Error: 0.018560833394158264
Root Mean Squared Error: 0.13623814955495492
R2 Score: 0.7422748348752446

---
## Cross Validation Scores
[0.73368548 0.73606519 0.73337367 0.73796181 0.73217981]

---
## Future Improvements

- Hyperparameter optimization
- Compare with Random Forest and CatBoost
- Deploy using Streamlit
- Predict satisfaction before voyage completion
- Add interactive SHAP dashboard
---
## What I Learned

Through this project I learned:

- Feature engineering for tabular datasets
- XGBoost regression
- Cross-validation
- Model evaluation using MAE, RMSE, and R²
- Feature importance analysis
- SHAP explainability for tree-based models
- Translating machine learning outputs into business insights
---