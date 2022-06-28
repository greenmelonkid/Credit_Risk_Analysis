# Credit_Risk_Analysis

## Overview

The purpose of this study was to create and train a machine learning model in order to accurately predict high risk loans using the dataset from LendingClub. To do so, I used the imbalanced-learn and scikit-learn libraries by resampling. To oversample the data, I used RandomOversampler and SMOTE algorithms and to undersample, I used ClusterCentroids algorithm, and for the combination of over and undersampling, I used SMOTEENN. To reduce bias, The BalancedRandomForestClassifier and EasyEnsembleClassifier were used to predict credit risk.

## Results

### Oversampling

#### Naive Oversampling Algorithm
	- Balanced Accuracy Score: 64.38%
	- High Risk Precision: 1%
	- High Risk Recall: 69%

##### Confusion Matrix
![naive confusion matrix](https://user-images.githubusercontent.com/99292945/176093881-fc8e3dec-9299-46ea-8953-706a9f88f9e5.png)

##### Classification Report
![naive classification report](https://user-images.githubusercontent.com/99292945/176093935-46a4d53f-e592-4bd7-a619-cfdb5ccd391f.png)

#### SMOTE Oversampling Algorithm
	- Balanced Accuracy Score: 66.29%
	- High Risk Precision: 1%
	- High Risk Recall: 63%

##### Confusion Matrix
![SMOTE confusion matrix](https://user-images.githubusercontent.com/99292945/176093964-4f16419a-76de-4d4c-9759-85adb04e4ddc.png)

##### Classification Report
![SMOTE classification report](https://user-images.githubusercontent.com/99292945/176093981-9b6336d9-a3a0-4684-804d-5b334b834317.png)

### Undersampling

#### ClusterCentroids Algorithm
	- Balanced Accuracy Score: 54.47%
	- High Risk Precision: 1%
	- High Risk Recall: 69%

##### Confusion Matrix
![clustercentroids confusion matrix](https://user-images.githubusercontent.com/99292945/176094116-ddfdc8d9-bf38-493b-aabd-4aa656f22a17.png)

##### Classification Report
![clustercentroids classification report](https://user-images.githubusercontent.com/99292945/176094143-db150d74-2479-4206-8f61-220d340b07c6.png)

### Combination Over and Undersampling

#### SMOTEENN Algorithm
	- Balanced Accuracy Score: 67.48%
	- High Risk Precision: 1%
	- High Risk Recall: 76%

##### Confusion Matrix
![SMOTEEN confusion matrix](https://user-images.githubusercontent.com/99292945/176094165-9ece84e4-7af1-41c1-bace-dadd8bb982d2.png)

##### Classification Report
![SMOTEEN classification report](https://user-images.githubusercontent.com/99292945/176094172-b17dc9fe-2dd7-4620-869b-483e29896f66.png)

### Ensemble Learners

#### Balanced Random Forest Classifier Algorithm
	- Balanced Accuracy Score: 78.85%
	- High Risk Precision: 3%
	- High Risk Recall: 70%

##### Confusion Matrix
![random forest confusion matrix](https://user-images.githubusercontent.com/99292945/176094203-59afa560-3463-4c77-b81e-3e586a71d583.png)

##### Classification Report
![random forest classification report](https://user-images.githubusercontent.com/99292945/176094216-b11d3bca-6247-4bea-b796-c8c94203fab9.png)

#### Easy Ensemble AdaBoost Classifier
	- Balanced Accuracy Score: 93.16%
	- High Risk Precision: 9%
	- High Risk Recall: 92%

##### Confusion Matrix
![ADA boost confusion matrix](https://user-images.githubusercontent.com/99292945/176094233-7ee73d1a-6fb5-4bb3-8a1a-a73a66cd4f84.png)

##### Classification Report
![ada boost classification report](https://user-images.githubusercontent.com/99292945/176094242-c82491e1-9e59-4178-8404-48de9ef76b2c.png)

## Summary

The balanced accuracy scores for each of the models in descending order are:

Easy Ensemble AdaBoost Classifier: 93.16%
Balanced Random Forest Classifier Algorithm: 78.85%
SMOTEEN Algorithm: 67.48%
SMOTE Oversampling Algorithm: 66.28%
Naive Oversampling Algorithm: 64.38%
ClusterCentroids Algorithm: 54.47%

When it comes to loans, I'm sure banks, etc. are more cautious giving out loans to people that are high risk. High risk, meaning people might not be willing or not able to pay back the money they borrowed. Even though all models predicted low and high risk loans, we only focused on the high risk loans. Looking at all of the balanced accuracy scores for each model, it is clear that the Easy Ensemble AdaBoost Classifier was the best model. Looking at the confusion matrix of the Easy Ensemble AdaBoost Classifier, we can see that it was only wrong 8 times, while all other models were wrong between 24-37 times. Because of this huge gap, I would think the Easy Ensemble AdaBoost Classifier would be the best model for this project.
