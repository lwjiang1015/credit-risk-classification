# credit-risk-classification

## Overview of the Analysis

This project attempts to train a model based on a dataset of historical lending activity from a peer-to-peer lending services company in order to evaluate loan risk and identify the creditworthiness of borrowers. 

The features upon which the loan risk is to be predicted are: loan_size, interest_rate, borrower_income, detb_to_income ratio, number of accounts, total_debt and one binary feature for derogatory_marks which equals to 1 for YES. The target is the loan risk which equals to 1 for high-risk loans and equals to 0 for healthy loans. 

Firstly, the columns in the original dataset are separated into labels (y, the targer mentioned above) and features (as mentioned above).   The data is then split into training and testing sub-datasets respectively with 58152 samples (75%) in the training dataset and 19384 samples (25%) in the testing dataset, out of the 77536 samples in the original datasets. TO train the training data for predicting the loan risk, a logistic regression model is created to fit the training data before predictions are made using the testing data. 

## Results

To evaluate the model's performance, a confusion matrix is generated and the classification report is printed. The results from both both are discussed as below:

* Confusion Matrix shows, out of 19384 sample loans in the testing dataset:
    * 18663 loans are predicted as healthy correctly (True negative) while 56 loans predicted as healthy but actually of high risk (False negative). 
    * 563 loans are predicted as high-risk correctly (True positive) while 102 loans predicted as high-risk but actually healthy (False positive).

* The results from the classification report confirm the results from the confusion matrix, specifically:
    * when predicting healthy loans, the precision rate is 100% and recall rate is 99%, resulting in 100% overall f1-score.
    * when predicting loans of high-risk, the precision rate is 85% and recall rate is 91%, resulting in 88% overall f1-score.
    * the above taken together, the overall accuracy rate for predicting credit risk of the loans is 99%. 
    
## Summary

Summarise the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

In summary, the model built upon the history data appear to reflect the conservatism when evaluating loans. The model appears to better in predicting healthy loans. Recommendation: the evaluation may be reviewed by a senior manager before rejecting any seemingly high-risk loans so as not to lose the business opportunities to potentially good borrowers who will be able to pay after all. 