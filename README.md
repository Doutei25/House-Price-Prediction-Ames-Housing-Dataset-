# House-Price-Prediction-Ames-Housing-Dataset-
The project follows an end-to-end data science workflow, from data loading and cleaning to feature engineering, modeling, evaluation, and final submission.
Methodology
1️⃣ Data Loading

Loaded train.csv and test.csv

Verified dataset dimensions and data types

2️⃣ Data Cleaning & Missing Values

Handled missing values based on domain meaning:

Categorical features (e.g., PoolQC, Alley, Fence): filled with "None"

Numerical features:

LotFrontage: filled using median by neighborhood

Others: filled with median or zero where appropriate

3️⃣ Outlier Analysis

Used skewness analysis and visual inspection

Log-transformed highly skewed numerical features

Target variable SalePrice log-transformed using log1p

4️⃣ Feature Engineering

Separation of numerical and categorical features

One-Hot Encoding for categorical variables

Scaling handled internally by tree-based models

5️⃣ Modeling

Implemented a pipeline-based approach for consistency

Models explored:

Gradient Boosting Regressor

HistGradientBoostingRegressor (for NaN robustness)

Final model trained on full training data

6️⃣ Model Evaluation

Cross-validation using RMSE (log scale)

Achieved strong correlation between actual and predicted prices

Validation RMSE ≈ 0.11 – 0.13

7️⃣ Prediction & Submission

Predictions generated on test dataset

Inverse log transformation applied (expm1)

Submission file created in required Kaggle format

📊 Results Summary
Metric	Value
Validation RMSE (log)	~0.11
Correlation (Actual vs Predicted)	~0.99
Model Type	Gradient Boosting
Features Used	All cleaned & encoded features
