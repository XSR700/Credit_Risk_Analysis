# Credit_Risk_Analysis

a loan lending service company would like to better evaluate candidates by credit risk. Using maching learning through Python, this analysis include programs that train and predict load credit risk. The resampling models and predicting algorithms such as SMOTEEN and Ensamble Classifiers were executed with thier finalized reports. 

## Overview of the analysis: Explain the purpose of this analysis.

## Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

- Oversampling Results
Accuracy Score is higher than 50% but not high

![RANDOM OVERSAMPLING SCORE](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Naive%20Random%20Oversampling%20Accuracy%20Score.PNG)

The report shows a good recall score but a very low precision score thus a low f1 score. 

![RANDOM OVERSAMPLING REPORT](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Naive%20Random%20Oversampling%20Report.PNG)

SMOTE oversampling resulted in a moderate accuracy score.

![SMOTE OVERSAMPLING SCORE](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/SMOTE%20Oversampling%20Accuracy%20Score.PNG)

The report showsvery low precision for with low recall for high risk predicting. Low risk predicting has high precision and low recall. Overall f1 score is moderate.  

![SMOTE OVERSAMPLING REPORT](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/SMOTE%20Oversampling%20Report.PNG)


- Undersampling
The accuracy score is low for undersampling.

![UNDERSAMPLING SCORE](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Undersampling%20Accuracy%20Score.PNG)

recall and precision are low for both low and high risk predictability.

![UNDERSAMPLING REPORT](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Undersampling%20Report.PNG)


- Combination (Over and Under) Sampling
Accuracy score is moderate for combined over and under sampling.

![COMBO SCORE](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Combonation%20(Over%20and%20Under)%20Sampling%20Accuracy%20Score.PNG)

recall is moderate and precision is low for high risk predicting. precision is high and recall is low for low risk predicting. 

![COMBO REPORT](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Combination%20(Over%20and%20Under)%20Sampling%20Report.PNG)



- Ensemble Learners: Balanced Forest Classifer
With balanced random forest classifier of ensemble learning algorithm the accuracy score is moderate. 

![ENSEMBLE SCORE](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Balanced%20Random%20Forest%20Classifier%20Accuracy%20Score.PNG)

The precision is moderate and recall is low for high risk predicting.The precision and recall is 100% for low risk predicting. Overall F1 score is very high. 

![ENSEMBLE REPORT](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Balanced%20Random%20Forest%20Classifier%20Report.PNG)

- Easy Ensemble AdaBoost Classifer

With easy ensemble adaboost classifier algorithm, the accuracy score is high.  

![EASY SCORE](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Easy%20AdaBoost%20Classifier%20Report.PNG)

In the report the precision is very low for high risk predicting, but high on sensitivity/recall. The low risk predictability is high on precision and recall/sensitivity. Overall score is high. F1 score for high risk predicting is very low

![EASY REPORT](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Easy%20Ensemble%20AdaBoost%20Classifier%20Accuracy%20Score.PNG)


## Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.

In our case, when we are trying to screen candidates for a loan, we do not want too many high risk candidates labeled as low risk for our model. In other words we want less false negatives. Therefore a high precision predicting algorithm is more important. We will lose low risk candidates in the process but that will be better than let too many high risk candidates through.  

Out of all the algorithms performed, none showed a promosing robust result to confindently predict our results. Most of the models show very low precision scores and only easy ensemble adaboost classifier showed a high accuracy score. 

The highest precision score resulted in ensemble balanced forest classifer with 0.73 and is moderate but not high. The F1 score for this model was very high due to high precision and sensitivity of low risk predicting pushing this score to 1.0. This means that the ensemble balanced forest classifier detected all the low risk applicants correctly but was not sensitive or very precise at finding the high risk users. The accuracy score of this model was not strong but higher than fifty percent at 0.62. Ovverall this is a good model to use but does not show strong reliability. 

There are deeper trade-offs to take into consideration in this case. a low and high risk is vague and may have variance within its definition. An individual high risk applicant could have a criminal record while the other high risk applicant is high in debt. In this example, risks could be interpreted differently. For discussions like these, perhaps letting some high risk applicants is a sacrifice the loan lending company can afford to take in order to profit higher in the long term. Then the ensemble AdaBoost classifer is more exceptional to use because it has very high sensitivity numbers and a high accuracy score. 

