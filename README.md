# Credit_Risk_Analysis
Module 17 - Supervised Machine Learning 

## Project Overview

Overview of the analysis: Explain the purpose of this analysis.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.


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


## Resources 

- Software: Python 3.7.6, Visual Studio Code 1.58.1, Jupyter Notebook 6.3.0


## Results



<p align="center">
<kbd>
  <img src="https://github.com/GabrielaTuma/bikesharing/blob/7fed2962046b921c5f47bb515c9639a26fd7b630/Images%20/Trips%20by%20Weekday%20per%20Hour.png">
</kbd>  &nbsp;
</p>



Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.


