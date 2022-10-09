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

The accuracy in unbalanced classification is sometimes not a good measure of the quality of the model. With this data, if one classifies every application as low risk, the accuracy would be xxx. That being said, the accuracy of the ensemble methods is better than that of the sampling methods, and the best accuracy of 0.9317 is obtained by the easy ensemble AdaBoost classifier.

The high-risk precisions of the ensemble methods are higher than those of the sampling methods (all 0.01), but they are all low. The highest precision of 0.09 is obtained by the easy ensemble AdaBoost classifier. The interpretation is that if someone is classified as high-risk, then there is only a 9% chance that they actually are high risk (91% are actually low-risk).

The high-risk recalls of the first five models range between 0.62 and 0.72. The recall of the easy ensemble AdaBoost classifier outperforms them with a recall of 0.92. The interpretation is that if someone is actually high-risk, then the model will classify them as high-risk 92% of the time (only 8% of high-risk candidates will be classified as low-risk). That is quite good.

From a lender business perspective, all these models are conservative. Low precision tells us that many low-risk candidate borrowers are classified as high-risk. This conservatism is probably acceptable to lenders.

What lenders do not want to do is lend to high-risk candidate borrowers. A high recall informs us that a model correctly identifies high-risk candidates.

This study recommends the use of the easy ensemble AdaBoost classifier. It has the highest accuracy (93.17%), the highest precision (9%), and the highest recall (92%) of any of the six algorithmic models tested. Most importantly, the recall is high, identifying high-risk candidate borrowers 92% of the time. 