# Youtube Views Prediction : Project Overview

- The data provides youtube channel in details such as publish date, trending date, views, title, like, dislike, comment, tags, description etc.
- Do data preprocessing to optimize learning process of model
- Train model with 7 different algorithms and choose best model for next hyperparameter tuning
- From the model, find out which features play an important role in predicting views. 

## Data Preparation
- Fix missing value and duplicated data.
- Make new columns to count difference day from publish date until trending date.
- treatment outlier with log transform to reduce outliers without deleting data.
- Do standardization and feature engineering.

## Machine Learning Model
Before train the model, split the data into train set & test set (80:20). Trained the model with 7 different algorithms and evaluated them.The model was trained with:

| Model Eval | Linear | Ridge | Lasso | ElasticNet | Decision Tree | Random Forest | SVR |
| --- | --- | --- | --- | --- | --- | --- | --- | 
|MAE |0.26 | 0.26 |0.59 |0.59 |0.24 |0.17 |0.24 |
|RMSE |0.33 | 0.33 |0.74 |0.74 |0.34  |0.24 |0.31 |
|R2 | 0.81 | 0.81| 0.05 |0.05 |0.80 |0.90 |0.83 |

From the table above, best performance was obtained using random forest, with the lowest RMSE of 0.24 and the lowest R2 score of 0.90. Next we will do hyperparameter tuning.
Hypertuning Result are shown below.

| Model | MAE | RMSE| R2 | 
| --- | --- | --- | --- | 
| Random Forest | 0.18 | 0.24 |0.90 | 

the results are not much different, looks like before hypertuning. Next, we will find out which features play an important role in predicting views. The results of feature importance are shown below.

![alt_text](https://github.com/annisahumaira21/youtube-views-prediction/blob/main/feature%20importance%20RF.JPG)<br>

Based on the feature importance score above, it can be seen that features dislikes, likes, desc_len are the top importance features that we can focus on to get more views. Other features such as comments_disabled, ratings_disabled, or video_error have very low feature importance scores. 





