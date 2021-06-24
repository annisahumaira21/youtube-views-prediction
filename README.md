# Youtube Views Prediction : Project Overview

- This project using dataset youtube_statistic.xlxs
- Do data preprocessing to optimize learning process of model
- Train model with 6 different algorithms and choose top 2 for next hyperparameter tuning
- Validate model with data test.

## Problem
viewers on youtube channel not didn't increase significantly. We want to know impactful features of this problem and fix it.

## Purpose:
to find out views of a channel youtube based on some characterictic to get insight what features can be improved.

## Data Preparation
- Fix missing value and duplicated data.
- Make new columns to count difference day from publish date until trending date.
- treatment outlier with log transform
- Do normalization and feature engineering

## Machine Learning Model
Because we want to predict target with numeric value, so we use Regression Model. Actually, we train model in 7 different algorithm and choose best model for next hypertuning. Here's the result:

| Model Eval | Linear | Ridge | Lasso | ElasticNet | Decision Tree | Random Forest | SVR |
| --- | --- | --- | --- | --- | --- | --- | --- | 
|MAE |0.26 | 0.59 |0.59 |0.24 |0.96 |0.17 |0.24 |
|RMSE |0.33 | 0.74 |0.74 |0.34 |0.96 |0.24 |0.31 |
|R2 | 0.81 | 0.05 | 0.05 |0.80 |0.96 |0.90 |0.83 |

Hypertuning Result:
| Model | MAE | RMSE| R2 | 
| --- | --- | --- | --- | 
| Random Forest |  |  |  | 

## Insight




