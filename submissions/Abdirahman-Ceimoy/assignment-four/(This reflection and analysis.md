🏠 House Price Prediction – Assignment Four
Overview

In this assignment, I implemented two regression models to predict house prices:

Linear Regression

Random Forest Regressor

The objective was to compare their performance and determine which model produces more accurate predictions.

Part A – Implementation
1. Data Preparation

Loaded cleaned dataset (99 rows, 13 columns).

Target variable: Price

Features: All columns except Price and LogPrice

Split data:

80% Training

20% Testing

random_state=42

2. Models Trained
Linear Regression

Trained using training data.

Used as a baseline model.

Assumes linear relationship between features and price.

Random Forest Regressor

n_estimators=100

random_state=42

Ensemble of decision trees.

Captures non-linear relationships.

Model Evaluation

Metrics used:

R² (Coefficient of Determination)

MAE (Mean Absolute Error)

MSE (Mean Squared Error)

RMSE (Root Mean Squared Error)

Linear Regression Results

R²: 0.8478

MAE: 63,085

RMSE: 75,624

Random Forest Results

R²: 0.8594

MAE: 52,524

RMSE: 72,686

Interpretation

Random Forest achieved:

Higher R²

Lower MAE

Lower RMSE

This means Random Forest explained more variance and produced smaller prediction errors overall.

Sanity Check

Example from test set:

Actual Price: 642,500

Linear Regression Prediction: 656,754

Random Forest Prediction: 789,031

In this example, Linear Regression was closer to the real value.
However, based on overall metrics across the test set, Random Forest performed better on average.

Understanding Random Forest

Random Forest is an ensemble model that builds multiple decision trees and averages their predictions.

For regression:

Each tree predicts a value.

Final prediction = average of all trees.

This reduces overfitting and improves generalization compared to a single model.

Final Conclusion

Based on R², MAE, and RMSE results, Random Forest performed better than Linear Regression in this task.

Although Linear Regression is simpler and easier to interpret, Random Forest provided:

Better overall accuracy

Lower prediction errors

Slightly stronger generalization

Therefore, Random Forest is the preferred model for this house price prediction task.