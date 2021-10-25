# Credit_Risk_Analysis
Module 17 - Supervised Machine Learning 

## Project Overview

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, this project is about employing different machine learning techniques to train and evaluate models with unbalanced classes.

- The data will be oversampled using the **RandomOverSampler** and **SMOTE** algorithms, and undersampled using the **ClusterCentroids** algorithm. Then, a combinatorial approach of over and undersampling using the **SMOTEENN** algorithm will be applied.

- Next, two new machine learning models that reduce bias, **BalancedRandomForestClassifier** and **EasyEnsembleClassifier**, will be applied in the same dataset.

The goal of this analysis  is to describe the balanced accuracy scores and the precision and recall scores of all six machine learning models and evaluate their performance to know whether they should be used to predict credit risk or not. 


#### Deliverable 1
RandomOverSampler, SMOTE and ClusterCentroids analysis:
- [x] 1. An accuracy score for the model is calculated
- [x] 2. A confusion matrix has been generated
- [x] 3. An imbalanced classification report has been generated


#### Deliverable 2
SMOTEENN analysis:
- [x] 1. An accuracy score for the model is calculated
- [x] 2. A confusion matrix has been generated
- [x] 3. An imbalanced classification report has been generated


[credit_risk_resampling.ipynb file](https://github.com/GabrielaTuma/Credit_Risk_Analysis/blob/bd1484514798965dbca0f0cb6cbc6435d5ec161b/credit_risk_resampling.ipynb) 


#### Deliverable 3
BalancedRandomForestClassifier:
- [x] 1. An accuracy score for the model is calculated
- [x] 2. A confusion matrix has been generated
- [x] 3. An imbalanced classification report has been generated
- [x] 4. The features are sorted in descending order by feature importance

EasyEnsembleClassifier:
- [x] 5. An accuracy score of the model is calculated
- [x] 6. A confusion matrix has been generated
- [x] 7. An imbalanced classification report has been generated

[credit_risk_ensemble.ipynb file](https://github.com/GabrielaTuma/Credit_Risk_Analysis/blob/bd1484514798965dbca0f0cb6cbc6435d5ec161b/credit_risk_ensemble.ipynb)


#### Deliverable 4
- [x] 1. There is a title, and there are multiple sections
- [x] 2. Each section has a heading and subheading
- [x] 3. Links to images are working, and code is formatted and displayed correctly
- [x] 4. The purpose of this analysis is well defined
- [x] 5. There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models
- [x] 6. There is a summary of the results
- [x] 7. There is a recommendation on which model to use, or there is no recommendation with a justification


## Outcomes

- Software: Python 3.7.6, Visual Studio Code 1.58.1, Jupyter Notebook 6.3.0


## Results

Before looking at the results it's important to understand 3 concepts: 

- Precision: Precision is the measure of how reliable a positive classification is.

- Recall: Recall is the ability of the classifier to find all the positive samples.

- F1 score: F1 score is a weighted average of the true positive rate (recall) and precision, where the best score is 1.0 and the worst is 0.0.

Our analysis is related to credit risk, in this case, positive values are high risk loans and **precision** will tell us the relationship between **correctly predicted high risk** loans and the **total amount of high risk predictions.** The **recall** score, in the other hand, uses correctly and **incorrectly** predicted high risk loans to be calculated.  


### Resampling

RandomOversampler:
<p align="center">
<kbd>
  <img src="https://github.com/GabrielaTuma/Credit_Risk_Analysis/blob/b71920dcb3594e6c59ea4aa1da88a1e7b898346d/Images/RandomOversampler.png">
</kbd>  &nbsp;
</p>

SMOTE:
<p align="center">
<kbd>
  <img src="https://github.com/GabrielaTuma/Credit_Risk_Analysis/blob/b71920dcb3594e6c59ea4aa1da88a1e7b898346d/Images/SMOTE.png">
</kbd>  &nbsp;
</p>

ClusterCentroids:
<p align="center">
<kbd>
  <img src="https://github.com/GabrielaTuma/Credit_Risk_Analysis/blob/b71920dcb3594e6c59ea4aa1da88a1e7b898346d/Images/ClusterCentroids.png">
</kbd>  &nbsp;
</p>

SMOTEENN:
<p align="center">
<kbd>
  <img src="https://github.com/GabrielaTuma/Credit_Risk_Analysis/blob/b71920dcb3594e6c59ea4aa1da88a1e7b898346d/Images/SMOTEEN.png">
</kbd>  &nbsp;
</p>


Oversampling and Undersamplig methods show similar performances, precision scores are around 0.7 and recall scores are around 0.01. We can see a slight improvement when the SMOTEENN method is applied combining both sampling techniques, but not enough to say the model is reliable. 

The very low precision scores from all methods tell us that a lot of the low risk loans were "accused" by the model of being high risk. The recall scores, all around 0.7, are saying that about 70% of the high risk loans are "caught". 

Most of the high risk loans will be detected by using RandomOverSampler, SMOTE, ClusterCentroids and SMOTEENN algorithms, but a lot of low risk loans will be incorrectly classified in the process. Therefore, they should not be used to predict credit risk independently. 


### Ensemble

BalancedRandomForestClassifier:
<p align="center">
<kbd>
  <img src="https://github.com/GabrielaTuma/Credit_Risk_Analysis/blob/b71920dcb3594e6c59ea4aa1da88a1e7b898346d/Images/BalancedRandomForestClassifier.png">
</kbd>  &nbsp;
</p>


EasyEnsembleClassifier:
<p align="center">
<kbd>
  <img src="https://github.com/GabrielaTuma/Credit_Risk_Analysis/blob/b71920dcb3594e6c59ea4aa1da88a1e7b898346d/Images/EasyEnsembleClassifier.png">
</kbd>  &nbsp;
</p>

Ensemble learning is the process of combining multiple models, like decision tree algorithms, to help improve the accuracy and robustness, as well as decrease variance of the model, and therefore increase the overall performance of the model. BalancedRandomForestClassifier and EasyEnsembleClassifier were employed in the analysis as well 

on whether they should be used to predict credit risk.

This methods can be used as a first filter, but it can't be used to determine reliably whether a loan is high or low risk 



Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.


<p align="center">
<kbd>
  <img src="https://github.com/GabrielaTuma/Credit_Risk_Analysis/blob/b71920dcb3594e6c59ea4aa1da88a1e7b898346d/Images/feature_importances_.png">
</kbd>  &nbsp;
</p>
