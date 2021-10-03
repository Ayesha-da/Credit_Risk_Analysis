# Credit_Risk_Analysis
## Overview of the analysis: 
To apply machine learning to solve a real-world challenge: credit card risk.To employ different techniques to train and evaluate models with unbalanced classes since credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans.to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

## Results:

### Oversampling

#### Naive Random Oversampling

In random oversampling, instances of the minority class are randomly selected and added to the training set until the majority and minority classes are balanced.

![naiveOversample](https://user-images.githubusercontent.com/84524153/135724813-16cd8a87-026e-4e37-bb8a-581a87c0a24d.png)

##### The accuracy score of this model is  around 66% 

##### The precision for high risk loans is very low around 1% that is to say model fails to predict risky loans but is very good at predicting low risk loans with precision of almost 100%.
##### Recall is around 74% for high risk loans that is to say model can identify almost 75 % of risky loans but it can only identify about 55% of good ones.

#### SMOTE Oversampling

In synthetic minority oversampling technique (SMOTE), new instances are interpolated and the size of the minority is increased.

![smoteOversample](https://user-images.githubusercontent.com/84524153/135724820-41969276-5665-413e-9d01-edc93c88ede1.png)

##### The accuracy score of this model is  around 66% 

##### The precision for high risk loans is very low around 1% that is to say model fails to predict risky loans but is very good at predicting low risk loans with precision of almost 100%.
##### Recall is around 63% for high risk loans that is to say model can identify almost 63 % of risky loans but it can only identify about 69% of good ones.
##### It is important to note that although SMOTE reduces the risk of oversampling but it does not always outperform random oversampling.

### Undersampling

Cluster centroid undersampling is akin to SMOTE. The algorithm identifies clusters of the majority class, then generates synthetic data points, called centroids, that are representative of the clusters.

![undersampling](https://user-images.githubusercontent.com/84524153/135724851-2c4c82d0-23f7-4a4f-b6b8-b777ce5964eb.png)

##### The accuracy score of this model is around 54% 

##### The precision for high risk loans is very low around 1% that is to say model fails to predict risky loans but is very good at predicting low risk loans with precision of almost 100%.
##### Recall is around 69 % for high risk loans that is to say model can identify almost 69 % of risky loans but it can only identify about 40% of good ones.
##### While resampling can attempt to address imbalance, it does not guarantee better results.

### Combination( Over and Under) sampling

SMOTEENN combines the SMOTE and Edited Nearest Neighbors (ENN) algorithms

![combination](https://user-images.githubusercontent.com/84524153/135724857-c2691487-ff24-4604-af70-874ac0f2813c.png)

##### The accuracy score of this model is  around 64% 

##### The precision for high risk loans is very low around 1% that is to say model fails to predict risky loans but is very good at predicting low risk loans with precision of almost 100%.
##### Recall is around 72% for high risk loans that is to say model can identify almost 72 % of risky loans but it can only identify about 57% of good ones.
##### Resampling with SMOTEENN did not work miracles, but some of the metrics show an improvement over undersampling.

### Balanced Random Forest Classifier

A balanced random forest randomly under-samples each boostrap sample.

![randomForest](https://user-images.githubusercontent.com/84524153/135724865-67ec8b0c-e386-45c9-9877-4afeec1e69b4.png)

##### The accuracy score of this model is  around 87% 

##### The precision for high risk loans is  low around 3% that is to say model fails to predict risky loans but is very good at predicting low good loans with precision of almost 100%.
##### Recall is around 70% for high risk loans that is to say model can identify almost 70 % of risky loans but  at 87% , it is better at identifying  good loans.

### Easy Ensemble AdaBoost Classifier

Ensemble learning is the process of combining multiple models, like decision tree algorithms, to help improve the accuracy and robustness, as well as decrease variance of the model
![easyEnsemble](https://user-images.githubusercontent.com/84524153/135724871-b5d2f404-d6a1-40b6-b431-5f494100f0b0.png)

##### The accuracy score of this model is  around 93% 

##### The precision for high risk loans is very low around 9% that is to say model can predict upto 9% risky loans but is very good at predicting good loans with precision of almost 100%.
##### Recall is around 92% for high risk loans that is to say model can identify almost 92 % of risky loans but it can only identify about 94% of good ones.


## Summary: 
### Recommendation:
