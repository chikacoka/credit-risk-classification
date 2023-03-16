# Module 21 Credit Risk Analysis Report

This work aims to employ various techniques to train and evaluate a model based on the credit risk of borrowers. Historical lending transactions (77,536 data entries) from a peer-to-peer lending services company were used as input into building a model that can predict the credit worthiness of borrowers with the below column headers:

Loan size
Interest rate on the loan
Borrower's income
Debt_to_Income ratio
Number of accounts held by the borrower
Derogatory remarks on the borrower's credit report
Total debt
Loan status (with 1 indicating credit default, and o representing a performing loan)

According to scikit-learn.org, the accuracy_score function computes the accuracy of correct predictions.The model's accuracy score of approximately 99.18% reveals its reliability in reasonably predicting the credit worthiness of potential borrowers. However, according to Klein (2022), the 'accuracy' measure is not always an adequate performance measure, and the confusion matrix helps make it easy for us to see what kind of confusions occur in our classification algorithms. 
Going by the confusion matrix, we see that the model predicted 18,663 performing loans ('0') correctly, in contrast with the actual of 18,765 (18663 + 102) performing loans, approximately 99% accurate predictions of '0' (performing loans), with a great precision score of 1. The model also predicted a total of 563 defaults('1') in contrast with the actual of 619 (563 + 56), approximately 91% accurate prediction of '1' (non-performing loans or defaults), with a 0.85 precision score.

Running the confusion matrix with the resampled data (random over sampling), the model's accuracy score went up to approximately 99.38% from the previous 99.18% (for the original data). Also, the model's predictive power for default loans rose to 99% from 91% (for original data) with a slightly low precision score of 0.84, but relatively remained at approximately 99% predictive power for the healthy (performing) loan, and with a precision score of 1.

# References:
https://scikit-learn.org/stable/modules/model_evaluation.html#:~:text=3.3.-,2.2.,function%20returns%20the%20subset%20accuracy.
Klein, B. (July 5, 2022), Confusion matrix in machine learning, retrieved from python-course.eu: https://python-course.eu/machine-learning/confusion-matrix-in-machine-learning.php