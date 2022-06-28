# Credit_Risk_Analysis

## Overview

The purpose of this study was to create and train a machine learning model in order to accurately predict high risk loans using the dataset from LendingClub. To do so, I used the imbalanced-learn
and scikit-learn libraries by resampling. To oversample the data, I used RandomOversampler and SMOTE algorithms and to undersample, I used ClusterCentroids algorithm, and for the combination of
over and undersampling, I used SMOTEENN. To reduce bias, The BalancedRandomForestClassifier and EasyEnsembleClassifier were used to predict credit risk.

## Results

### Oversampling

#### Naive Oversampling Algorithm
	- Balanced Accuracy Score: 64.38%
	- High Risk Precision: 1%
	- High Risk Recall: 69%

##### Confusion Matrix
ADD IMAGE HERE

##### Classification Report
ADD IMAGE HERE

#### SMOTE Oversampling Algorithm
	- Balanced Accuracy Score: 66.29%
	- High Risk Precision: 1%
	- High Risk Recall: 63%

##### Confusion Matrix
ADD IMAGE HERE

##### Classification Report
ADD IMAGE HERE

### Undersampling

#### ClusterCentroids Algorithm
	- Balanced Accuracy Score: 54.47%
	- High Risk Precision: 1%
	- High Risk Recall: 69%

##### Confusion Matrix
ADD IMAGE HERE

##### Classification Report
ADD IMAGE HERE

### Combination Over and Undersampling

#### SMOTEENN Algorithm
	- Balanced Accuracy Score: 67.48%
	- High Risk Precision: 1%
	- High Risk Recall: 76%

##### Confusion Matrix
ADD IMAGE HERE

##### Classification Report
ADD IMAGE HERE

### Ensemble Learners

#### Balanced Random Forest Classifier Algorithm
	- Balanced Accuracy Score: 78.85%
	- High Risk Precision: 3%
	- High Risk Recall: 70%

##### Confusion Matrix
ADD IMAGE HERE

##### Classification Report
ADD IMAGE HERE

#### Easy Ensemble AdaBoost Classifier
	- Balanced Accuracy Score: 93.16%
	- High Risk Precision: 9%
	- High Risk Recall: 92%

##### Confusion Matrix
ADD IMAGE HERE

##### Classification Report
ADD IMAGE HERE

## Summary

The balanced accuracy scores for each of the models in descending order are:

Easy Ensemble AdaBoost Classifier: 93.16%
Balanced Random Forest Classifier Algorithm: 78.85%
SMOTEEN Algorithm: 67.48%
SMOTE Oversampling Algorithm: 66.28%
Naive Oversampling Algorithm: 64.38%
ClusterCentroids Algorithm: 54.47%

When it comes to loans, I'm sure banks, etc. are more cautious giving out loans to people that are high risk. High risk, meaning people might not be willing or not able to
pay back the money they borrowed. Even though all models predicted low and high risk loans, we only focused on the high risk loans. Looking at all of the balanced
accuracy scores for each model, it is clear that the Easy Ensemble AdaBoost Classifier was the best model. Looking at the confusion matrix of the Easy Ensemble AdaBoost Classifier, we
can see that it was only wrong 8 times, while all other models were wrong between 24-37 times. Because of this huge gap, I would think the Easy Ensemble AdaBoost Classifier would be 
the best model for this project.






























