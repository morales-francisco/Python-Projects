# Classification + Clustering - Income Predictor #


## Introduction ##
The Us Adult income dataset was extracted by Barry Becker from the 1994 US Census Database. The data set consists of anonymous information such as occupation, age, native country, race, capital gain, capital loss, education, work class and more.
Each row is labelled as either having a salary greater than ">50K" or "<=50K". 

## Source ##
The data source is [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Adult).

## Objective ##
The objective from this project is to predict whether income exceeds $50K/yr based on census data.

## Conclusions ##

- In order to achieve the goal, a series of models were used: Logistic Regression, KNN, Naive Bayes.
When analyzing the target variable, I observed that the classes were unbalanced, so the most appropriate metric to compare the models would be the ROC curve and its AUC value. In the three cases I proposed a GridSearch + Cross Validation strategy, in order to find the best hyperparameters for each model. After training the models, I can say that the model with the best performance was KNN, however, as we already know, it has a higher computational cost.

- In addition to the classification model, a cluster analysis was performed to see if there are homogeneous groups of people. Kmeans, Hierarchical Clustering and DBSCAN models were tested. It was concluded that there is a number of clusters other than 2 that best describes the structure of the data and that is with cluster number = 4, this is seen in both hierarchical clustering and k-means. However, the best results are seen in k-means, since it defines the x and y boundaries that make the most sense for the observed variables. The clustering performed by DBSCAN is not optimal for the structure of the data. This is because the areas of the graph have different densities, being more densely populated at the extremes.
