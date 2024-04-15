# Module 20 Report - Credit Risk Analysis 

### Overview of the Analysis

This analysis utilizes past lending activity data from a peer-to-peer lending company to develop a model that predicts the creditworthiness of future borrowers. The dependent variable (y) denotes loan status, distinguishing between healthy (0) and high-risk (1) loans. Independent variables (X) encompass loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The objective is to accurately forecast which loans will be high risk and which will be healthy, as the bank aims to avoid rejecting potentially repayable loans (false 1) or, worse yet, granting loans that won't be repaid (false 0).

Key stages in the machine learning model process:

1. **Data Loading:** Data is loaded from a CSV file into the 'df_lending_data' dataframe.
2. **Feature Engineering:** Labels (`y`) are created from the “loan_status” column, while features (`X`) are extracted from the remaining columns.
3. **Label Balance Check:** The balance of labels is assessed using the `value_counts` function.
4. **Data Splitting:** The data is divided into training and testing datasets.
5. **Model Creation:** A Logistic Regression Model is built with the original data. The model is fitted, predictions are saved, and performance is evaluated by printing a balanced accuracy score, confusion matrix, and classification report.

## Results

* Machine Learning Model 1:
  * **Accuracy:** The model achieves an accuracy score of 0.99, indicating correct classification of 99% of instances.
  * **Precision:**
    - For healthy loans ('0'): Precision is 1.00, indicating perfect identification of true positives with no false positives.
    - For high-risk loans ('1'): Precision is 0.87, denoting moderate effectiveness in identifying high-risk loans with some false positives.
  * **Recall:**
    - For healthy loans ('0'): Recall is 1.00, signifying perfect identification of all healthy loans instances with no false negatives.
    - For high-risk loans ('1'): Recall is 0.89, suggesting moderate effectiveness in identifying high-risk loans with some false negatives.

## Summary

This model isn't recommended for use. While it accurately predicts healthy loans with perfect precision, its ability to identify high-risk loans is less precise, which could pose a significant issue. False negatives in predicting high-risk loans mean that some risky loans might be approved before their unhealthy nature is recognised. Considering this, there are likely better models avaliable that would predict high-risk loan with a better level of acuracy.