# Classification (Scikit-learn + Tensorflow) - Bank Personal Loan #


## Introduction ##
This case is about a bank whose management wants to explore ways of converting its liability customers to personal loan customers (while retaining them as depositors). A campaign that the bank ran last year for liability customers showed a healthy conversion rate of over 9% success. This has encouraged the retail marketing department to devise campaigns with better target marketing to increase the success ratio with minimal budget.

## Source ##
The data source is [Kaggle](https://www.kaggle.com/datasets/teertha/personal-loan-modeling).

## Objective ##
The classification goal is to predict the likelihood of a liability customer buying personal loans.

## Conclusions ##

Analyzing the structure of the dataset that was used for the training, I noticed a disparity in the objective variable distribution (“No” in 90% and “Yes” in the remaining 10%). Taking this into account, I change the accuracy metric to measure the model’s performance by the F1-score, since it allows harmonizing the disparity of the objective variable. After my analysis, I could observe that the most classic ML model, such as logistic regression, does not perform as well as the rest. In fourth place is the MLP model (an input layer, two hidden layers with 128 neurons each, and a dense output layer to make the prediction), which presents a considerable difference from the logistic regression model. Yet still, it is a little below the rest of the models. Analyzing the 3 most optimal models (Decision Tree, Random Forest, XGBoost) , I do not show a marked difference in performance. The model selection will not vary by performance, so will be determined by an economic factor and the availability of the resources (implementation cost, training, processing, etc.) to make the decision.
