# Credit_Risk_Analysis

## Overview of the analysis: Explain the purpose of this analysis.

## Purpose
The purpose of this challenge is to use different **Machine Learning Models** to test credit risk and also to evaluate the accuracy of the test. After utilizing different models the results will be compared to each other to determine which model performs the best for the given data set. 

## Background
For this assignment I need to employ different techniques to train and evaluate models with unbalanced classes. I will use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I will oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, I’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once I am done, I’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Results:

### Resampling Models to Predict Credit Risk

### Naive Random Oversamling

* First we split the data into testing and training

![image](https://user-images.githubusercontent.com/105535250/200156709-0cf01e3a-9f67-4de2-9fe8-b7ec4f61f638.png)

* Use the resampled data to train a logistic regression model.

![image](https://user-images.githubusercontent.com/105535250/200156872-f46954c4-6d9b-4ba0-bdf7-6b3691cd221a.png)

* Calculate the balanced accuracy score from sklearn.metrics.

![image](https://user-images.githubusercontent.com/105535250/200156833-a1d132e4-0157-4a4a-b961-d956ea8b4747.png)

* Print the confusion matrix from sklearn.metrics.

![image](https://user-images.githubusercontent.com/105535250/200156918-2f17f53a-d6f9-4788-a8e8-a9076afd71b5.png)

* Generate a classication report using the imbalanced_classification_report from imbalanced-learn.

![image](https://user-images.githubusercontent.com/105535250/200156952-8d1490ca-2a0d-478d-ac8a-9fae4da10d49.png)

Naive Random Oversampling showed a low precision for high_risk while a very high precision for low_risk points. It also showed a higher recall value in high_risk than in low_risk. It also has a decent accuracy.

### Smote Oversampling 

SMOTE Oversampling showed very similar values to Naive Random. A low precision for high_risk while a very high precision for low_risk points. With the main difference being the recall is low in high risk then low risk. It has a little higher accuracy then Naive Oversampling.

* Balance Accuracy score

![image](https://user-images.githubusercontent.com/105535250/200157226-4cbccd65-b726-414a-8062-81cffd39f95c.png)

* Classification Report

![image](https://user-images.githubusercontent.com/105535250/200157278-473ff9ed-df80-445e-9a1a-ecca1003e1aa.png)

### Undersampling
It showed a higher precision in low risk and low in high risk. Recall in high_risk is higher than low_risk while it has a similar accuracy as Smote Oversampling.

* Balance Accuracy

![image](https://user-images.githubusercontent.com/105535250/200157845-95a0dda5-ee08-4111-947b-f71a16610b5d.png)

* Classification Report

![image](https://user-images.githubusercontent.com/105535250/200157866-c1a5a987-8d80-4f5d-8dc9-3dc34c12dba5.png)

### Combination (Over and Under) sampling

The combined algorithm showed similar precision values as in other oversampling. It has a much higher recall for high_risk compared to low risk. It also has a decent accuracy.

* Balance Accuracy

![image](https://user-images.githubusercontent.com/105535250/200157911-d746bcdb-5f3b-4631-833d-bb7516b56014.png)

* Classification Report

![image](https://user-images.githubusercontent.com/105535250/200157932-17a93883-b5f2-4b08-884f-451bc4a21c87.png)

### Random Forest Classifier

Random forest algorithm shows that it has a higher accuracy than any of the previous algorithms while also having high recall and a higher precision score for low risk.

* Balance Accuracy

![image](https://user-images.githubusercontent.com/105535250/200158108-b90fe175-ffe2-4e4a-bd4b-d41a23325179.png)

* Classification Report

![image](https://user-images.githubusercontent.com/105535250/200158137-050455df-e00f-4c4e-a4c8-86b23f0b2eef.png)

### Easy Ensamble Adaboost Classifier

Easy Ensemble has the highest accuracy of any algorithm tested. the precision is lower in high risk while recall is lower in high risk than lower risk.

* Balance Accuracy

![image](https://user-images.githubusercontent.com/105535250/200158210-073b9016-325b-4de8-965d-bf32b67c28e8.png)

* Classification Report

![image](https://user-images.githubusercontent.com/105535250/200158231-a23f9d26-baf2-44c8-bbe0-1f44b134163b.png)

## Summary

When looking at the results of the testing, some models performed much better than others. For this dataset I found Easy Ensemble as a good algorithm to use due to the high recall, accuracy and precision scores when compared to all the other algorithms. We can avoid Combination (over and under)sampling as an algorithm due to having the lowest accuracy score. The rest of the algorithms were relativily comperable to one another.

