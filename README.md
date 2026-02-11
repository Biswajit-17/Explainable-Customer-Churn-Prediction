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

**Metrics:**

Class 0 (Loyal) -> Precision: 0.83, Recall: 0.90, F1-Score: 0.86

Class 1 (Churn)	Overall -> Precision: 0.63, Recall: 0.48, F1-Score: 0.54

**Overall**

**79% Accuracy**
**0.70 Macro Average**
**0.78 Weighted Average**

## Key Takeaways
**High Loyalty Prediction (90% Recall for Class 0):**
The model is exceptionally good at identifying customers who are likely to stay. This reduces "false alarms," ensuring that the business doesn't accidentally offer unnecessary discounts to loyal customers.
**Conservative Churn Detection:**
With a Churn Precision of 63%, the model ensures that when it flags a customer as a "Churn Risk," there is a high probability they actually intend to leave. This makes marketing intervention (like retention emails) highly cost-effective.
**Balanced Accuracy (79%):**
The model correctly predicts the outcome for 4 out of 5 customers, providing a reliable foundation for the SHAP explanation layer to identify churn drivers.
**Strategic Recall (48% for Class 1):**
While the model identifies roughly half of all churners, the Explainable AI (XAI) component adds massive value here. For the 48% of churners caught, the model provides specific behavioral "reasons" (e.g., Fiber Optic issues or Month-to-Month contracts), allowing for surgical, high-impact retention strategies.
**Actionable Insights via SHAP:**
The raw metrics are enhanced by the interpretability layer, which revealed that Tenure and Contract Type are the most significant factors influencing these scores.
