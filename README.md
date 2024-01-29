# Kaggle Playground Series - Season 4, Episode 1
https://www.kaggle.com/competitions/playground-series-s4e1/overview

Objective: to predict whether a customer continues with their account or closes it (e.g., churns).
Criteria: Submissions are evaluated on area under the ROC curve between the predicted probability and the observed target.

## Method
As the dataset was synthetically generated from another competion (https://www.kaggle.com/datasets/shubhammeshram579/bank-customer-churn-prediction), the original dataset was included during the training phase.
The additional data can help to improve training and generalization by providing a greater variance in data.

CustomerId and id were dropped.
Variables with missing data are either imputed using mean, or the most frequent.
With the high number of categories for Surname, target encoding was used. Else, ordinal encoding was performed on categorical variables as tree algorithms do not require one hot encoding.
As Age appeared to be slightly skewed, log transformation was used in a bid to improve training.
