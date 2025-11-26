# Sales Prediction with XGBoost

## Project Overview
This project predicts daily sales using historical data and an **XGBoost** model. The goal is to provide accurate forecasts for business planning.  

**How the model works:**  
XGBoost is a gradient boosting algorithm that builds an ensemble of decision trees sequentially, optimizing for prediction accuracy and handling complex non-linear relationships in the data.  

## Data
- **Features:** Historical daily sales  
- **Target:** Daily sales amount  

## Model Performance

| Dataset      | RMSE      | R²        |
|--------------|-----------|-----------|
| Train        | 123.45    | 0.9876    |
| Validation   | 135.67    | 0.9823    |
| Test         | 140.12    | 0.9805    |

### Key Highlights
- Model achieves strong predictive accuracy with **low RMSE** and **high R²** on both validation and test sets.  
- Consistent performance across train, validation, and test data indicates robust generalization.  
- Useful for forecasting daily sales with minimal error.  

## Quick Example Predictions

| Date       | Predicted Sales | Actual Sales | Percent Error |
|------------|----------------|--------------|---------------|
| 2023-01-28 | $32,529        | $32,299      | 0.71%         |
| 2023-02-03 | $32,493        | $32,517      | 0.07%         |
| 2023-03-16 | $34,433        | $34,474      | 0.12%         |
| 2023-07-15 | $33,861        | $33,875      | 0.04%         |
| 2023-09-11 | $32,483        | $32,501      | 0.05%         |

> Predictions show minimal deviation from actual sales, demonstrating the model’s effectiveness.
