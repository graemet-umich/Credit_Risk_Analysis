# Credit Risk Analysis
Assess various models on their ability to predict credit risk

## Overview

This study is an analysis of credit card risk. Lending companies would like to be able to predict risk and so understand to whom they should lend.

When one considers an analysis of credit card risk, there are many more "low risk" applicants than "high risk" applicants. This situation is referred to as an unbalanced classification problem, and a different set of algorithms is necessary to meaningfully address this problem.

Here data is obtained from LendingClub, a peer to peer lending services company. The data contain features and a credit risk target, so this analysis is a supervised learning problem. The data is used to test six different algorithmic models to determine which model is best and if that model is good enough to be used to assess credit card risk.

## Results

Data containing 115,679 records of 86 fields was obtained from LendinClub from Q1 of 2019. After preprocessing, the data contained xxx records of xxx feature fields, and one binany target field named loan_status with values of either low_risk or high_risk. This is a supervised learning problem, because all the features are identified by a target value.

Six algorithms, four using sampling and two using xxx, were used to classify unbalanced credit card risk data: naive random oversampling, SMOTE oversampling, cluster centroids undersampling, SMOTEENN combination over- and undersampling, balanced random forest classifier, and easy ensemble AdaBoost classifier.

An accuracy score is the fraction of test cases a model correctly classifies. The following balanced accuracy scores were obtained:

| Algorithmic Model | Balanced Accuracy Score |
| --- | :---: |
| Naive Random Oversampling | 0.6384 |
| SMOTE Oversampling | 0.6589 |
| Cluster Centroids Undersampling | 0.5447 |
| SMOTEENN Combination Over/Under Sampling | 0.6483 |
| Balanced Random Forest Classifier | 0.7885 |
| Easy Ensemble AdaBoost Classifier | 0.9317 |
Table. Balanced accuracy scores for the six models used.

### Resampling Techniques

- **Naive Random Oversampling.** The balanced accurancy score is 0.6384, the precision is 0.01, and the recall/specificity is 0.61.

![Naive Random Oversampling](./Resources/Naive_Random_Oversampling.png)
Fig. Imbalanced classification report for naive random oversampling.

- ***SMOTE Oversampling.** The balanced accurancy score is 0.6589, the precision is 0.01, and the recall/specificity is 0.62.

![SMOTE Oversampling](./Resources/SMOTE_Oversampling.png)
Fig. Imbalanced classification report for SMOTE oversampling.

- **Cluster Centroids Undersampling.** The balanced accurancy score is 0.5447, the precision is 0.01, and the recall/specificity is 0.69.

![Cluster Centroids Undersampling](./Resources/ClusterCentroids.png)
Fig. Imbalanced classification report for cluster centroids undersampling.

- **SMOTEENN Combination Over and Under Sampling.** The balanced accurancy score is 0.6483, the precision is 0.01, and the recall/specificity is 0.72.

![SMOTEENN Combination Over/Under Sampling](./Resources/SMOTEENN.png)
Fig. Imbalanced classification report for naive random oversampling.

### Ensemble Learners

- **Balanced Random Forest Classifier.** The balanced accurancy score is 0.7885, the precision is 0.03, and the recall/specificity is 0.70.

![Balanced Random Forest Classifier](./Resources/Balanced_Random_Forest_Classifier.png)
Fig. Imbalanced classification report for naive random oversampling.

- **Easy Ensemble AdaBoost Classifier.** The balanced accurancy score is 0.9317, the precision is 0.09, and the recall/specificity is 0.92.

![Easy Ensemble AdaBoost Classifier](./Resources/Easy_Ensemble_AdaBoost_Classifier.png)
Fig. Imbalanced classification report for naive random oversampling.


## Summary

