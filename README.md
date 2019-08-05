# IEEE-Fraud
IEEE Fraud Detection was a competition on Kaggle. I was competing in it. This is how I went on to analyse the data. The data was highly imbalanced .

1. Initially, to get baseline model, I just filled Nans with -999, used LabelEncoding, used algorithm to reduce size of data and used XGB          model.

2. I started dropping some columns based on the number of unique values and number of Nans in it. 

3. Based on insights from discussion forum of the competition, it was clear that the minima of training data's TransactionDT refers to 1st        November 2017. Thanks to those people. I created hour,day,weekday and month columns and further engineered around 80 features by                caluculating relative TransactionAmt by dividing original TransactionAmt by the mean and max of TransactionAmt grouped by weekday, hour,        month and week. This was done because their might be some pattern as to when the Fraud's happen the most and basically after Fraud, unusual    amount of TransactionAmt may be seen.
