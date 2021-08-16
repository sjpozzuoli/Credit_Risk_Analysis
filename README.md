# Credit Risk Analysis

### The purpose of this is to use the credit card credit dataset from LendingClub and over and under-sample the data and use two machine learning models that reduce bias to predict credit risk. Once that is completed, the performance of these models will be evaluated and a written recommendation will be made on whether they should be used to predict credit risk.

## Results

###  Naive RandomOverSampler model

![Naive_balanced_accuracy_score](https://user-images.githubusercontent.com/81929616/129495910-3b3e6159-f867-4c41-b027-a94540ebce01.PNG)
![Naive_confusion_matrix](https://user-images.githubusercontent.com/81929616/129495916-b6288163-f805-49b7-b384-d2b8fed2da16.PNG)
![Naive_balanced_classification_report](https://user-images.githubusercontent.com/81929616/129495917-18c69892-0362-446f-aefc-b106b09faccc.PNG)

- Accuracy score: 66.1%
- High Risk precision: 1%
- Low Risk precision: 100%
- High Risk recall: 66%
- Low Risk recall: 67%

### SMOTE model

![SMOTE_balanced_accuracy_score](https://user-images.githubusercontent.com/81929616/129495936-ccebee19-9dd6-4ed3-9485-e44355851ba3.PNG)
![SMOTE_confusion_matrix](https://user-images.githubusercontent.com/81929616/129495937-bb153b5a-904e-4328-9d77-82ef1992b534.PNG)
![SMOTE_imbalanced_classification_report](https://user-images.githubusercontent.com/81929616/129495939-5c4f8384-2904-4f47-a634-105baf204a4a.PNG)

- Accuracy score: 63%
- High Risk precision: 1%
- Low Risk precision: 100%
- High Risk recall: 62%
- Low Risk recall: 64%

### ClusterCentroids Undersample model

![ClusterCentroids_balanced_accuracy_score](https://user-images.githubusercontent.com/81929616/129495949-0e6e12eb-eb33-47e0-93cb-bc6caa70e998.PNG)
![ClusterCentroids_confusion_matrix](https://user-images.githubusercontent.com/81929616/129495950-4de6fdea-a03a-4374-88f4-88dc6f268f1b.PNG)
![ClusterCentroids_imbalanced_classification_report](https://user-images.githubusercontent.com/81929616/129495952-2bdc029e-e26c-49ac-b5eb-f4adefc315eb.PNG)

- Accuracy score: 63%
- High Risk precision: 1%
- Low Risk precision: 100%
- High Risk recall: 59%
- Low Risk recall: 43%

### SMOTEENN model

![SMOTEENN_balanced_accuracy_score](https://user-images.githubusercontent.com/81929616/129495974-470c9dca-d2f5-48bf-a290-bebed8fb4687.PNG)
![SMOTEENN_confusion_matrix](https://user-images.githubusercontent.com/81929616/129495976-cd18ad72-4b0b-4d78-85eb-96262eb3601e.PNG)
![SMOTEENN_imbalanced_classification_report](https://user-images.githubusercontent.com/81929616/129495977-17f16a81-dd7d-439b-8048-fa6b77a2ad86.PNG)

- Accuracy score: 51%
- High Risk precision: 1%
- Low Risk precision: 100%
- High Risk recall: 70%
- Low Risk recall: 57%

### Balanced Random Forest model

![RandomForest_balanced_accuracy_score](https://user-images.githubusercontent.com/81929616/129495985-70c0927a-89f1-4e72-b488-f3fe41968328.PNG)
![RandomForest_confusion_matrix](https://user-images.githubusercontent.com/81929616/129495987-5c3d4213-1334-4e2f-8a2f-a96b4589b05c.PNG)
![RandomForest_imbalanced_classification_report](https://user-images.githubusercontent.com/81929616/129495988-f9856763-4e52-4d32-8d0c-685d870047d5.PNG)

- Accuracy score: 80.1%
- High Risk precision: 3%
- Low Risk precision: 100%
- High Risk recall: 71%
- Low Risk recall: 89%

### Easy Ensemble model

![EasyEnsemble_balanced_accuracy_score](https://user-images.githubusercontent.com/81929616/129496005-ff4a2f31-49d9-4a8d-be9f-93b041dfdbf6.PNG)
![EasyEnsemble_confusion_matrix](https://user-images.githubusercontent.com/81929616/129496006-55270210-f335-443e-8b93-21768bedfca6.PNG)
![EasyEnsemble_imbalanced_classification_report](https://user-images.githubusercontent.com/81929616/129496011-2ffcd138-0fb1-428d-a8a4-43ebaf120b9d.PNG)

- Accuracy score: 92.5%
- High Risk precision: 7%
- Low Risk precision: 100%
- High Risk recall: 91%
- Low Risk recall: 94%

## Summary

### After analyzing all of the models, there does not seem to be one that is truly effective for the detection of high risk credit, due to the extremely low precision scores on the high risk side. Even though the Easy Ensemble model has a 92.5% accuracy score and 91% high risk recall, because the precision is so low at 7%, LendingClub can not even be confident that the full number of high risk creditors has been identified.
