# Customer Churn Prediction + Explainable ML

## Project Overview
This project predicts customer churn using Machine Learning and uses SHAP values to explain the "Why" behind every prediction.

## Workflow
1. **Preprocessing**: Cleans data and handles categorical encoding.
2. **Training**: Trains a Random Forest Classifier.
3. **Interpretability**: Uses SHAP to generate global and individual explanations.

## Key Insights (from SHAP)
- **Tenure**: New customers are the highest churn risk.
- **Contract Type**: Two-year contracts significantly reduce churn probability.
- **Fiber Optic**: Customers with Fiber Optic service are churning at higher rates, indicating a potential service issue.

## How to Run
1. Run `python src/data_preprocessing.py`
2. Run `python src/train_model.py`
3. Run `python src/explain_model.py`