# Credit_Risk_Analysis

## Overview of the analysis: Explain the purpose of this analysis.

a loan lending service company would like to better evaluate candidates by credit risk. Using machine learning through Python, this analysis includes programs that train and predict load credit risk. The resampling models and predicting algorithms such as SMOTEEN and Ensemble Classifiers were executed with their finalized reports. 

## Results

- Oversampling Results
Accuracy Score is higher than 50% but not high

![RANDOM OVERSAMPLING SCORE](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Naive%20Random%20Oversampling%20Accuracy%20Score.PNG)

The report shows a good recall score but a very low precision score thus a low f1 score. 

![RANDOM OVERSAMPLING REPORT](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Naive%20Random%20Oversampling%20Report.PNG)

SMOTE oversampling resulted in a moderate accuracy score.

![SMOTE OVERSAMPLING SCORE](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/SMOTE%20Oversampling%20Accuracy%20Score.PNG)

The report shows very low precision with low recall for high-risk predicting. Low risk predicting has high precision and low recall. Overall f1 score is moderate.  

![SMOTE OVERSAMPLING REPORT](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/SMOTE%20Oversampling%20Report.PNG)


- Undersampling
The accuracy score is low for undersampling.

![UNDERSAMPLING SCORE](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Undersampling%20Accuracy%20Score.PNG)

recall and precision are low for both low and high-risk predictability.

![UNDERSAMPLING REPORT](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Undersampling%20Report.PNG)


- Combination (Over and Under) Sampling
The accuracy score is moderate for combined over and under-sampling.

![COMBO SCORE](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Combonation%20(Over%20and%20Under)%20Sampling%20Accuracy%20Score.PNG)

the recall is moderate and precision is low for high-risk predicting. precision is high and recall is low for low-risk predicting. 

![COMBO REPORT](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Combination%20(Over%20and%20Under)%20Sampling%20Report.PNG)



- Ensemble Learners: Balanced Forest Classifier
With a balanced random forest classifier of ensemble learning algorithm, the accuracy score is moderate. 

![ENSEMBLE SCORE](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Balanced%20Random%20Forest%20Classifier%20Accuracy%20Score.PNG)

The precision is moderate and recall is low for high-risk predicting. The precision and recall are 100% for low-risk predicting. Overall F1 score is very high. 

![ENSEMBLE REPORT](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Balanced%20Random%20Forest%20Classifier%20Report.PNG)

- Easy Ensemble AdaBoost Classifier

With Easy Ensemble AdaBoost Classifier algorithm, the accuracy score is high.  

![EASY SCORE](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Easy%20AdaBoost%20Classifier%20Report.PNG)

In the report, the precision is very low for high-risk predicting but high on sensitivity/recall. The low-risk predictability is high on precision and recall/sensitivity. Overall F1 score is high. F1 score for high-risk predicting is very low.

![EASY REPORT](https://github.com/XSR700/Credit_Risk_Analysis/blob/main/Screenshots/Easy%20Ensemble%20AdaBoost%20Classifier%20Accuracy%20Score.PNG)


## Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.

In our case, when we are trying to screen candidates for a loan, we do not want too many high-risk candidates labeled as low risk for our model. In other words, we want fewer false negatives. Therefore a high precision predicting algorithm is more important. We will lose low-risk candidates in the process but that will be better than letting too many high-risk candidates through.  

Out of all the algorithms performed, none showed a promising robust result to confidently predict our results. Most of the models show very low precision scores and only the Easy Ensemble AdaBoost Classifier showed a high accuracy score of 0.92. Some reasons that might be causing this are due to weak data and weak learners in the data. We just don't have enough high-risk applicant data to make our models predict better. 

The highest precision score resulted in an ensemble balanced forest classifier with 0.73 and is moderate but not high. The F1 score for this model was very high due to the high precision and sensitivity of low risk predicting pushing this score to 1.0. This means that the ensemble balanced forest classifier detected all the low-risk applicants correctly but was not sensitive or very precise at finding the high-risk applicants. The accuracy score of this model was not strong but higher than fifty percent at 0.62. Overall this is a good model to use but does not show strong reliability. 

There are deeper trade-offs to take into consideration in this case. a low and high risk is vague and may have variance within its definition. An individual high-risk applicant could have a criminal record while the other high-risk applicant is high in debt. In this example, risks could be interpreted differently. For discussions like these, perhaps letting some high-risk applicants is a sacrifice the loan lending company can afford to take to profit higher in the long term. Then the ensemble AdaBoost classifier is more exceptional to use because it has very high sensitivity numbers with a high accuracy score. 



