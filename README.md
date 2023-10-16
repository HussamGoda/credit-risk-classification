# credit-risk-classification

**Report**
***Introduction and Overview**
The purpose of this analysis aims at producing a Machine Learning (ML) model that may help financial institutions to decide whether a loan is a healthy and “risk-free” or high-risk. The model uses input information (features) covering measures like loan size, interest rate, income of the borrower, debt-to-income ratio, number of accounts, derogatory marks and total debt. Such measures are used to decide whether a loan is healthy or not. A dataset that contains 77536 records is used. A binary system is used to define the status of the loan; 0 for a healthy loan and 1 for a high risk loan.
A few issues should be noted.
-	Input features may need to checked and confirmed. For example, the input feature debt_to_income) is dependent on two other input features (borrower_income and total_debt). One of the three features may need to be removed.
-	Transformation and normalization may need to be considered before developing the model.
-	Over 96% of the records given in the dataset are considered healthy loans. The dataset may need to be balanced to produce a more realistic ML model. The model may be “more: affected by the Healthy Loan status than High Risk Loan status Healthy loan status.

Logistic Regression Model is used for this exercise. 
-	The dataset was first checked to confirm that data types are all correct. 
-	The dataset is then split into two datasets: one for model training and one for testing the model performance. 
-	The Training dataset contains 58152 records (75% of the total records in the original dataset). The remining 19384 records (25%) are assigned to the Testing dataset.
-	The model is Instantiate and trained using the training dataset (features and label)
-	Once the training process is completed, the model is used to predict loan status (the label) using features (input parameters) in both training and testing datasets separately.
-	Confusion matrix and classification report are calculated for each dataset (training and testing) separately.

***Results***
Overall, the ML model using Logistic Regression demonstrates a high rate of success. The following may be described.
-	The model produces high accuracy predicting loan status for both training and testing datasets (0.99)
-	Almost all what the model predicted as healthy loans are correct. (precision = 1.0)
-	Only 85% (the precision value) of the model predicted as high-risk loans in the training dataset are correct. For the testing dataset, the precision value in 0.87
-	The recall values for health loan in the training and testing dataset are 0.99 and 1.00 respectively. That means that almost what is actually declared as healthy loans in the dataset is correctly classified. The recall values go down to 0.89 (training dataset) and 0.89 (testing dataset) when it comes to high risk loans
-	F1-score is the harmonic average (does not place heavy weight on large values) between the precision and the recall values. F1-score for training and testing dataset for healthy loan status are 1 and 1. For high risk loan status, f1-score shows 0.87 for the training dataset and 0.88 for the testing dataset.
