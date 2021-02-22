# Credit Risk Analysis

## Overview
The purpose of this analysis is to examine a large dataset and construct a classifier to predict credit risk. A total of 6 approaches have been evaluated in order to maximize classifier efficiency.

## Results
A total of 6 machine learning models were created and evaluated:

* <b>Logistic Regression with Naive Random Oversampling</b>

![Capture election district name from .csv header](https://github.com/noble190/credit_risk_analysis/blob/main/img/Results_Over.png)
<hr>

* <b>Logistic Regression with SMOTE Oversampling</b>

![Capture election district name from .csv header](https://github.com/noble190/credit_risk_analysis/blob/main/img/Results_SMOTE.png)
<hr>

* <b>Logistic Regression with Cluster Centroids Undersampling</b>

![Capture election district name from .csv header](https://github.com/noble190/credit_risk_analysis/blob/main/img/Results_Under.png)
<hr>

* <b>Logistic Regression with SMOTEENN Over/Undersampling</b>

![Capture election district name from .csv header](https://github.com/noble190/credit_risk_analysis/blob/main/img/Results_Combination.png)
<hr>

* <b>Balanced Random Forest Classifier</b>

![Capture election district name from .csv header](https://github.com/noble190/credit_risk_analysis/blob/main/img/Results_Forest.png)
<hr>

* <b>AdaBoost Classifier</b>

![Capture election district name from .csv header](https://github.com/noble190/credit_risk_analysis/blob/main/img/Results_AdaBoost.png)
<hr>

### Comparison
* <b>Balanced Accuracy Scores: </b> It would appear that the first four models - Naive Oversampling, Cluster Centroid Undersampling, SMOTE, and SMOTEENN have similar, relatively low balanced accuracy scores. This score improves considerably for the Balanced Forest and AdaBoost models, with Adaboost returning an impressive score of 0.93.
* <b>Precision: </b> All examined models showed perfect precision for determining low-risk loans. However, this does not hold true for high-risk loans. Model performance was poor across the board in this category (with AdaBoost returning a relatively high 0.09).
* <b>Recall: </b> AdaBoost returned the most consistent recall values of 0.91 and 0.95 for high-risk and low-risk loans, respectively. The remaining models had signficantly lower and less consistent scores.

## Summary

In summary, it would appear that, for any evaluated machine learning model, it is quite trivial to predict low risk loans, but very difficult to predict high risk loans. Further evaluaton may be needed before deciding on an approach.

Given the low precision for high risk loans across the board, I would not recommend that any of these models be used. However, AdaBoost, while still inadequate, is considerably better than the other models evaluated.
