# Classification + Clustering (Scikit-learn) - Income Predictor #


## Introduction ##
The Us Adult income dataset was extracted by Barry Becker from the 1994 US Census Database. The data set consists of anonymous information such as occupation, age, native country, race, capital gain, capital loss, education, work class and more.
Each row is labelled as either having a salary greater than ">50K" or "<=50K". 

## Source ##
The data source is [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Adult).

## Objective ##
This project's goal is to predict, using census data, whether annual income exceeds $50,000.

## Conclusions ##

- Some models were applied, including Logistic Regression, KNN, and Naive Bayes, to reach the objective. The ROC curve and its AUC value would be the best way to compare the models since I discovered that the classes were unbalanced when I explored the target variable. I suggested a GridSearch + Cross Validation approach in each of the three situations to find the ideal hyperparameters for each model. I can say that after the models were trained, the KNN model performed the best, but as we are all aware, it has a higher computational expense.

- To determine whether there are any homogeneous groups of people, a cluster analysis was done in addition to the classification model. The models Kmeans, Hierarchical Clustering, and DBSCAN were probed. The option that best captures the structure of the data, as demonstrated by both hierarchical clustering and k-means, was determined to be four and two clusters. Though k-means defines the x and y boundaries that make the most sense for the observed variables, it produces the best results. DBSCAN's clustering is not the best option given the way the data are organized. This is due to the graph's different densities, with the extremes having higher population densities.
