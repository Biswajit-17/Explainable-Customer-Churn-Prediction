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

## Model Performance & Results 
The model was evaluated on a held-out test set (20% of the total data) to ensure generalization. While the primary focus of this project is Interpretability (XAI), the predictive engine maintains a solid performance baseline.
 ** Classification Report **
Metric	Class 0 (Loyal)	Class 1 (Churn)	Overall
Precision	0.83	0.63	79% Accuracy
Recall	0.90	0.48	0.73 Macro Avg
F1-Score	0.86	0.54	0.78 Weighted Avg


## How to Run
1. Run `python src/data_preprocessing.py`
2. Run `python src/train_model.py`
3. Run `python src/explain_model.py`
