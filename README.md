# Module_17_Challenge
Module 17 Challenge - Credit Risk Analysis

## Overview of Project
This project involves using Python, Juypter Notebooks, and a number of different machnie learning libraries to analyze data related to borrowers who have recieved a loan from a specific financial institution, in an attempt to identify those borrowers who are most likely to default on their loan. 

## Purpose of Analysis
The purpose of this challenge is to take a delimited text file containing a large number of fields of information about each borrower, and to then use 6 different machine learning libraries to and determine which algorithim is best able to identify those borrowers who later default on their loan.

## Results

- Random Oversampling

![Random Oversampling](/images/001_random_oversampling.png)

- SMOTE Oversampling

![SMOTE Oversampling](/images/002_SMOTE_oversampling.png)

- Undersampling

![Undersampling](/images/003_undersampling.png)

- Over and Undersampling

![Over and Undersampling](/images/004_over_and_under_sampling.png)

- Balanced Random Forest

![Balanced Random Forest](/images/005_balanced_random_forest.png)

 - Balanced Random Forest - Ranking of Feature Importance
  
![Balanced Random Forest - Ranking of Feature Importance](/images/005_feature_importance.png)

- AdaBoostClassifier

![AdaBoostClassifier](/images/006_AdaBoostClassifier.png)

## Sumary

The findings of our comparison of the various approaches is as follows:

![Summary Comparison](/images/007_summary_statistics.png)

Each model was very effective at accurately identifying loans which would not result in default, with few or no false-positives (a high level of precision); certain models (Balanced Random Forest and AdaBoost Classifier) were also able to identify the entire subset of loans which were ultimately low risk (a high level of recall).  However, given that the most important factor in the selection of a model for our purposes should be its ability to identify the greatest number of accounts at high risk (recall), the Random Oversampling and the Over- and Under-Sampling Models both identified the greatest number of high risk loans (74% and 73%, respectively) and would therefore be best suited for our use case - despite the fact that other models had higher AVERAGE precision, recall, and F1 scores.

### Caveat

Scaling was not used consistently across all, and the use of scaling may have an impact on the results ultimately achieved.  With additional time, additional testing should be undertaken to determine: 1.) if these results are consistent when other random seeds are used, 2.) for the models which used multiple estimators, experiments should be performed to determine how the results are impacted with greater and fewer numbers of estimators 3.) all models should be test both with and without the use of scaling and the results compared. 

