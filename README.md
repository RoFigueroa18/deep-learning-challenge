# deep-learning-challenge

Overview
Alphabet Soup, a nonprofit foundation, requested the development of a tool to help them select funding applicants with the best chance of success. The dataset provided contains over 34,000 records, including details such as:

EIN and NAME (Identification columns)
APPLICATION_TYPE
AFFILIATION
CLASSIFICATION
USE_CASE
ORGANIZATION
STATUS
INCOME_AMT
SPECIAL_CONSIDERATIONS
ASK_AMT
IS_SUCCESSFUL (target variable)
The goal was to predict whether an applicant would use the funding effectively.

Results
Data Preprocessing:

Target Variable: IS_SUCCESSFUL
Feature Variables: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
Removed Variables: EIN and NAME
Model Development:

Original Model:

Structure:
Input Layer: 8 units, ReLU activation
Hidden Layer: 5 units, ReLU activation
Output Layer: 1 unit, Sigmoid activation
Performance:
Accuracy: 72.51%
Loss: 0.556
Model Optimization Attempts:

Using keras_tuner, various configurations were tested to improve the model's accuracy. Despite not reaching the target accuracy of 75%, incremental improvements were observed:

First Attempt:

Structure: 3 layers, up to 10 units
Performance: Accuracy 72.73%
Second Attempt:

Structure: 5 layers, up to 50 units
Performance: Accuracy 72.91%
Third Attempt (Best Model):

Structure: 6 layers, up to 100 units
Performance: Accuracy 72.94%
Loss: 54.94%
Summary
By using keras_tuner and adjusting the number of layers and units, the model's accuracy improved, with the best model achieving 72.94%. However, this still fell short of the 75% target accuracy. A larger dataset might help achieve better results. Additionally, considering alternative models like Random Forests could be beneficial, as they are robust, provide excellent accuracy, are resistant to overfitting, more interpretable, and require less data preparation.
