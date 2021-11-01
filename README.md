# Credit_Risk_Analysis
Credit Risk Analysis with Machine Learning

## Overview of Project

To help evaluate credit risk while dealing with inherently unbalanced data using different machine learning techniques and models to try and find the best one.

## Results

- Naive Random Oversampling

Balanced Accuracy
![NRO_Bal](https://github.com/DavidFGitH/Credit_Risk_Analysis/blob/main/Resources/P1_Naive_Over_BA.png)

Precision and Recall Scores
![NRO_PR](https://github.com/DavidFGitH/Credit_Risk_Analysis/blob/main/Resources/P1_Naive_Over_PR.png)

Naive random oversampling produces a balanced accuracy score of about .65 and .01 and 1 precision score and .73 and .57 recall score for high risk and low risk credit scores respectively. While the .01 precision score for high risk credit score is worrying, this is a good benchmark to start.

- SMOTE Oversampling

Balanced Accuracy
![SMOTE_BA](https://github.com/DavidFGitH/Credit_Risk_Analysis/blob/main/Resources/P2_SMOTE_Over_BA.png)

Precision and Recall Scores
![SMOTE_PR](https://github.com/DavidFGitH/Credit_Risk_Analysis/blob/main/Resources/P2_SMOTE_Over_PR.png)

SMOTE oversampling produces a balanced accuracy score of about .66 and .01 and 1 precision score and .63 and .68 recall score for high risk and low risk credit scores respectively. Values are relatively close to the Oversampling model but with worse high risk and better low risk recall scores.

- Undersampling

Balanced Accuracy
![Under_BA](https://github.com/DavidFGitH/Credit_Risk_Analysis/blob/main/Resources/P3_Under_BA.png)

Precision and Recall Scores
![Under_PR](https://github.com/DavidFGitH/Credit_Risk_Analysis/blob/main/Resources/P3_Under_PR.png)

Undersampling produces a balanced accuracy score of about .54 and .01 and 1 precision score and .69 and .4 recall score for high risk and low risk credit scores respectively. Overall a lower balance accuracy score and marginally better recall score for high risk with much lower credit score for low risk.

- Combination (Over and Under) Sampling

Balanced Accuracy
![Comb_BA](https://github.com/DavidFGitH/Credit_Risk_Analysis/blob/main/Resources/P4_Comb_BA.png)

Precision and Recall Scores
![Comb_PR](https://github.com/DavidFGitH/Credit_Risk_Analysis/blob/main/Resources/P4_Comb_PR.png)

Combination sampling produces a balanced accuracy score of about .65 and .01 and 1 precision score and .72 and .57 recall score for high risk and low risk credit scores respectively. The balanced accuracy model is about on par with oversampled models with better recall for high risk with slightly less for low risk.

- Balanced Random Forest Classifier

Balanced Accuracy
![Bal_For_BA](https://github.com/DavidFGitH/Credit_Risk_Analysis/blob/main/Resources/P5_BRForest_BA.png)

Precision and Recall Scores
![Bal_For_PR](https://github.com/DavidFGitH/Credit_Risk_Analysis/blob/main/Resources/P5_BRForest_PR.png)

Balanced random Forest classifier produces a balanced accuracy score of about .96 and .06 and 1 precision score and 1 and .91 recall score for high risk and low risk credit scores respectively. The balanced accuracy is much better than previous models with almost completely accurate recall scores for both low and high risk.

- Easy Ensemble AdaBoost Classifier

Balanced Accuracy
![Easy_Ens_BA](https://github.com/DavidFGitH/Credit_Risk_Analysis/blob/main/Resources/P6_EasyEns_BA.png)

Precision and Recall Scores
![Easy_Ens_PR](https://github.com/DavidFGitH/Credit_Risk_Analysis/blob/main/Resources/P6_EasyEns_PR.png)

Easy ensemble AdaBoost classifier produces a balanced accuracy score of about .93 and .09 and 1 precision score and .92 and .94 recall score for high risk and low risk credit scores respectively. This model is only slightly worse than the balanced random forest classifier model in terms of balanced accuracy while having slightly better precision scores for high risk credit scores and slightly worse high risk recall and slightly worse low risk recall.

## Summary

Ultimately, all the models provided were not precise at all in terms of predicting the high risk credit scores, with Easy Ensemble AdaBoost Classifier being that highest at .09 precision, which is still very low. However, despite the low precision scores for all models, I would still recommend the Balanced Random Forest Classifier with the Easy Ensemble AdaBoost Classifier, with a slight preference towards the Balanced Random Forest Classifier. The reason I would still recommend models despite the low precision is that going under the original premise that the data is very unbalanced, both of the preferred models have very high recall scores in terms of finding high risk credit scores, with 1 and .92. This means that they can help isolate the most problematic credit scores where more research can be done. It would obviously be more ideal to have models with higher precision, but ones that do a good job of doing most of the heavy lifting doesn't hurt either. It also helps that their recall scores for low risk credit scores are also a lot better than the other models, so there won't be as much noise in the low risk credit scores.
