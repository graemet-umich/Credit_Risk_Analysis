# Credit Risk Analysis
Assess various models on their ability to predict credit risk

## Overview


This study uses data obtained from LendingClub, a peer to peer lending services company, 

## Results

### Resampling Techniques

- Naive Random Oversampling

![Naive Random Oversampling](./Resources/Naive_Random_Oversampling.png)
Fig. Imbalanced classification report for naive random oversampling.

- SMOTE Oversampling

![SMOTE Oversampling](./Resources/SMOTE_Oversampling.png)
Fig. Imbalanced classification report for SMOTE oversampling.

- Cluster Centroids Undersampling

![Cluster Centroids Undersampling](./Resources/ClusterCentroids.png)
Fig. Imbalanced classification report for cluster centroids undersampling.

- SMOTEENN Combination Over and Under Sampling

![SMOTEENN Combination Over/Under Sampling](./Resources/SMOTEENN.png)
Fig. Imbalanced classification report for naive random oversampling.

### Ensemble Learners

- Balanced Random Forest Classifier

![Balanced Random Forest Classifier](./Resources/Balanced_Random_Forest_Classifier.png)
Fig. Imbalanced classification report for naive random oversampling.

- Easy Ensemble AdaBoost Classifier

![Easy Ensemble AdaBoost Classifier](./Resources/Easy_Ensemble_AdaBoost_Classifier.png)
Fig. Imbalanced classification report for naive random oversampling.


## Summary


| Algorithmic Model | Balanced Accuracy Score |
| --- | :---: |
| Naive Random Oversampling | 0.6384 |
| SMOTE Oversampling | 0.6589 |
| Cluster Centroids Undersampling | 0.5447 |
| SMOTEENN Combination Over/Under Sampling | 0.6483 |
| Balanced Random Forest Classifier | 0.7885 |
| Easy Ensemble AdaBoost Classifier | 0.9317 |
Table. Balanced accuracy scores for the six models used.