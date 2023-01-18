# Classification (Scikit-learn + Tensorflow) - Bank Personal Loan #


## Introduction ##
This case is about a bank whose management wants to explore ways of converting its liability customers to personal loan customers (while retaining them as depositors). A campaign that the bank ran last year for liability customers showed a healthy conversion rate of over 9% success. This has encouraged the retail marketing department to devise campaigns with better target marketing to increase the success ratio with minimal budget.

## Source ##
The data source is [Kaggle](https://www.kaggle.com/datasets/teertha/personal-loan-modeling).

## Objective ##
The classification goal is to predict whether a liability customer will purchase personal loans.

## Conclusions ##

When I examined the dataset's structure, I discovered a discrepancy in the distribution of the objective variable ("No" in 90% of the cases and "Yes" in the remaining 10%). Due to the F1-score's ability to harmonize the disparity of the objective variable, I change the accuracy metric to evaluate the model's performance in light of this. After conducting my analysis, I discovered that the logistic regression model, which is the most traditional ML model, does not perform as well as the others. The MLP model, which differs significantly from the logistic regression model and is in fourth place, has an input layer, two hidden layers with 128 neurons each, and a dense output layer for making predictions. But even so, it falls short of the other models in some ways. I find no discernible performance difference when comparing the three best models (Decision Tree, Random Forest, and XGBoost). The decision to use one model over another will not be based on performance; rather, it will be based on economic considerations and the availability of resources (implementation costs, training, processing, etc.) to make the choice.
